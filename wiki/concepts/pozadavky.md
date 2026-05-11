# Požadavky

**Shrnutí**: Specifikace toho, co má systém dělat a jaká omezení musí splňovat. Jsou základem pro odhady pracnosti, návrh architektury a akceptační testování.

**Zdroje**:

- `raw/lectures/03.prednaska.pdf`



---

[[pozadavky|Požadavek]] definuje vlastnost nebo schopnost systému, kterou potřebuje uživatel k vyřešení problému nebo dosažení cíle.

## Vlastnosti správného požadavku
Každý požadavek by měl být:

- **Jednoznačný**: Nepřipouští více výkladů.
- **Splnitelný**: Lze jej realizovat v rámci projektu.
- **Ověřitelný**: Lze prokázat, že byl splněn (např. v rámci akceptačního testování). Ověřitelnost je základním předpokladem pro [[zajisteni-kvality|zajištění kvality]].

## Kategorizace požadavků
### 1. Projektové požadavky
Týkají se procesu vývoje (např. cena, termíny dodání, školení uživatelů).

### 2. Produktové požadavky
Týkají se vlastností samotného produktu a dělí se na:

- **Funkční požadavky**: Popisují chování systému (co má dělat).
- **Nefunkční (obecné) požadavky**: Určují omezení a kvality systému (jak má fungovat). Mají zásadní dopad na návrh architektury.

#### Model FURPS
Pro systematickou kategorizaci produktových požadavků se používá model **FURPS**:

- **F** (Functionality): Funkčnost, vlastnosti, bezpečnost.
- **U** (Usability): Použitelnost, lidské faktory, nápověda.
- **R** (Reliability): Spolehlivost, četnost poruch, zotavení.
- **P** (Performance): Výkon, propustnost, doba odezvy.
- **S** (Supportability): Podporovatelnost, rozšiřitelnost, instalovatelnost.

## Zdroje požadavků

- Komunikace se zákazníkem a budoucími uživateli.
- [[obchodni-procesy|Modelování obchodních procesů]].
- Zadávací dokumentace a reportované chyby starého systému.
- Pozorování uživatelů při práci.

## Reprezentace požadavků
Kromě textové formy lze požadavky v UML reprezentovat i graficky, například pomocí balíčků nebo vlastních profilů (stereotypů), které umožňují sledovat vazby mezi požadavky a dalšími elementy modelu.

![[imgs/03.prednaska-018.jpg|350]]

*Obrázek: Ukázka alternativní reprezentace funkčních požadavků (F1, F2) pomocí UML profilu.*


## Související stránky

- [[pripady-uziti]]
- [[uzivatelske-pribehy]]
- [[odhad-pracnosti]]

---
#pozadavky #analyza #furps #management #BI-SWI
