Jasně, jdeme na to. Metoda **A** (Hybridní cesta) je v podstatě "oční operace" pro AI. Tím, že v prvním kroku pomocí ImageMagicku (matematicky) vytáhneš hrany a šipky do extrémního kontrastu, AI je v druhém kroku přestane ignorovat jako šum.

Tady je kompletní guide v Markdownu se vším všudy.

---

# Guide: Hybridní čištění diagramů (ImageMagick + BiRefNet Docker)

Tento postup je nejlepší, pokud AI sama o sobě šipky "požírá". Nejdříve je zvýrazníme a pak necháme AI odvést zbytek práce.

## 1. Příprava lokálně (Zvýraznění šipek)

Tento krok proběhne u tebe v terminálu. Uděláme z obrázku vysoce kontrastní černobílou verzi, kde šipky budou jasně vidět.

```bash
# Vytvoříme dočasný soubor se zvýrazněnými linkami
# -lat 20x20+5% najde čáry i v nekvalitním JPG
magick vstup.jpg \
    -colorspace gray \
    -negate -lat 20x20+5% -negate \
    -modulate 100,0 -contrast-stretch 1x1% \
    temp_prepped.jpg

```

## 2. Spuštění AI v Dockeru

Pokud ještě server neběží, pusť ho. Tento image si sám stáhne potřebné modely (BiRefNet), pokud je ještě nemáš.

```bash
docker run -d \
  --name bg-cleaner \
  -p 7000:7000 \
  danielgatis/rembg s --host 0.0.0.0 --port 7000

```

## 3. Finální vyčištění přes API

Teď pošleme ten "vypálený" obrázek do AI. Díky parametru `model=birefnet-general` použijeme tu nejpřesnější metodu.

```bash
curl -s -F file=@temp_prepped.jpg \
     "http://localhost:7000/api/remove?model=birefnet-general" \
     -o final_no_bg.png

```

---

## 4. Totální úklid (Deep Clean)

Až budeš hotový a budeš chtít mít systém jako nový, postupuj přesně takto. Docker image a modely zabírají hodně místa.

### Rychlý úklid (jen kontejner)

```bash
docker stop bg-cleaner
docker rm bg-cleaner

```

### Hloubkový úklid (vše pryč)

Spusť tyto příkazy, abys uvolnil gigabajty místa:

```bash
# 1. Smaž image (samotnou aplikaci)
docker rmi danielgatis/rembg

# 2. Smaž volumes (tady jsou schované ty AI modely!)
docker volume prune -a -f

# 3. Smazání dočasných souborů
rm temp_prepped.jpg

```

---

## Proč tohle funguje?

* **ImageMagick** se postará o to, aby šipky nebyly šedé, ale **černé**.
* **AI (BiRefNet)** díky tomu vidí jasnou hranu a "pochopí", že ta čára není šmouha na papíře, ale součást objektu, kterou má nechat.
* **Docker** zajistí, že nemusíš instalovat tuny Python knihoven, které by se ti v systému hádaly.

**Tip:** Pokud by ty šipky byly po kroku 1 pořád moc slabé, změň v tom magick příkazu `+5%` na `+2%`. Bude to ještě agresivnější.
