# BI-SWI (Softwarové inženýrství) Wiki

Osobní znalostní báze pro přípravu na zkoušku, spravovaná LLM. 
Základní struktura a pravidla vycházejí ze vzoru LLM Wiki od Jana Matějky, rozšířená o Git-like workflow.

## Účel

Tato wiki je strukturovaná, vzájemně propojená znalostní báze, která má připravit studenta na zkoušku z předmětu BI-SWI na FIT ČVUT. LLM spravuje wiki, zatímco člověk dodává materiály, klade otázky a usměrňuje analýzu.

## Git Workflow (Správa změn)

K celé wiki přistupuj metaforicky jako ke Git repozitáři. Hlavní stabilní a ověřená větev se jmenuje `master`. Tvá komunikace a provádění změn se řídí těmito pravidly:

- **Drobné změny** (např. oprava překlepu, odpověď na jednoduchou otázku s drobným doplněním, přidání jednoho odkazu): Komunikuj jako přímý commit do `master`. (Ohlásíš například: `fix: oprava skloňování u odkazu na autorské právo`).
- **Velké změny** (např. zpracování nového PDF, generování nových konceptů, rozsáhlá refaktorizace existujících stránek):
  1. Vždy nejprve založ novou pracovní větev ve formátu `prefix/nazev` (např. `feat/novy-koncept`, `update/licence`, `ingest/prednaska-03`).
  2. Během práce v této větvi ukládej logické celky jako samostatné commity s jasnou zprávou ve formátu `typ: zprava` (např. `feat: vytvoření stránky p03`, `update: rozšíření konceptu o informace z extra`).
  3. Jakmile je celá sada změn hotová a ověřená, ohlas merge do větve `master` a počkej na schválení.
  4. Teprve po výslovném schválení zapiš provedené změny do `wiki/log.md`.

## Struktura složek

Základní struktura projektu:

```text
raw/             -- zdrojové dokumenty (neměnné -- nikdy je neupravuj)
  lectures/      -- pdf soubory z přednášek
  seminars/      -- aplikace informací a příklady ze cvičení
  extra/         -- stažená a oficiální PDF (skripta, weby, doplňkové materiály)
wiki/            -- markdown stránky spravované LLM
  lectures/      -- souhrnné stránky jednotlivých přednášek
  modules/       -- souhrnná skripta
  concepts/      -- koncepční stránky pro probírané pojmy a entity
  index.md       -- obsah pro celou wiki
  log.md         -- záznam o všech operacích (nové záznamy se vkládají vždy na začátek souboru)
```

## Pracovní postup zpracování (Ingest workflow)

Když uživatel přidá nový zdroj do složky `raw/` (např. přednášku) a požádá tě o jeho zpracování:

1. **Založení větve**: Ohlas vytvoření nové pracovní větve (např. `ingest/novy-zdroj`).
2. **Analýza kontextu**: Přečti si celý zdrojový dokument. Zároveň prohledej složku `raw/extra/` a stávající `wiki/concepts/`, zda neobsahují související informace k tématům v novém dokumentu.
3. **Integrace znalostí**: Pokud v `raw/extra/` najdeš doplňující informace, které ještě nejsou zpracovány jako koncept ve wiki, zahrň je do aktuálního kontextu. Pokud již koncept existuje ve `wiki/concepts/`, pracuj s ním jako s výchozím bodem pro rozšíření.
4. **Konzultace**: Než cokoliv finálně zapíšeš, prober s uživatelem klíčové poznatky a to, jaké informace z doplňkových materiálů jsi našel a plánuješ zapracovat.
5. **Tvorba/Aktualizace (Commity)**: Vytvoř nebo aktualizuj souhrnnou stránku v příslušné podsložce `wiki/` a prováděj commity do své aktuální větve:
   - Přednášky do `wiki/lectures/`.
   - Koncepční stránky do `wiki/concepts/`.
   - Informace z `extra/` prioritně zapracuj do příslušných konceptů nebo přednášek.
6. **Propojení a skloňování**: Přidej wiki-odkazy (`[[název-stránky]]`) pro propojení souvisejících stránek. **Pokud potřebuješ termín sklonit, aby pasoval do věty, použij formát `[[název-stránky|skloněný tvar]]`** (např. `[[autorske-pravo|autorského práva]]`).
7. **Merge a Log**: Jakmile vše dokončíš, ohlas merge. Po schválení uživatelem proveď pomyslný merge do `master`, aktualizuj `wiki/index.md` a na **úplný začátek** souboru `wiki/log.md` (jako první informaci pod nadpis) přidej záznam ve stylu merge commitu (datum, název větve/zdroje a shrnutí schválených změn). Nikdy nepřidávej záznamy na konec logu.

## Formát stránky

Každá wiki stránka by měla dodržovat tuto strukturu:

```markdown
# Název stránky

**Shrnutí**: Jedna až dvě věty popisující tuto stránku.

**Zdroje**:
- `raw/lectures/soubor.pdf`
- `raw/extra/souvisejici-material.pdf`

**Naposledy aktualizováno**: Datum poslední aktualizace.

---

Zde patří hlavní obsah. Používej jasné nadpisy a krátké odstavce. 
V textu přirozeně odkazuj na [[souvisejici-koncept|související koncepty]] pomocí skloněných wiki-odkazů.

Všechny relevantní poznatky z přednášek i doplňkových materiálů (extra) musí být logicky syntetizovány.

## Související stránky
- [[souvisejici-koncept-1]]
- [[souvisejici-koncept-2]]

---
#tag1 #tag2 #kod-predmetu
```

## Pravidla citací a tagování

- **Citace**: Každé faktické tvrzení musí odkazovat na svůj zdrojový soubor formátem `(zdroj: podsložka/nazev_souboru.pdf)`.
- **Rozpory**: Pokud si materiály z přednášek a složky `extra` odporují, výslovně na tento rozpor upozorni.
- **Ověření**: Pokud je tvrzení bez přímého zdroje (tvoje dedukce), označ ho jako vyžadující ověření.
- **Obsidian Tagy**: Na úplný konec každé stránky pod čáru (`---`) přidej relevantní tagy začínající křížkem. Vždy zahrň tag `#kod-predmetu`.

## Zodpovídání dotazů

1. Přečti si nejprve `wiki/index.md`, abys našel relevantní stránky ve větvi `master`.
2. Přečti si tyto stránky a syntetizuj odpověď.
3. Ve své odpovědi cituj konkrétní wiki stránky.
4. Pokud odpověď ve wiki není, prohledej `raw/extra/`, zda tam není odpověď schovaná.

## Obecná pravidla

- Nikdy neupravuj nic ve složce `raw/`.
- Po provedení změn vždy aktualizuj `wiki/index.md` a `wiki/log.md`.
- Názvy stránek udržuj psané malými písmeny a oddělené pomlčkami.
- Piš jasným, prostým jazykem vhodným pro studenty informatiky.
- **Při odkazování vždy preferuj gramaticky správné skloňování pomocí `[[odkaz|tvar]]`.**
