# Analýza obrázků - Přednáška 3: Analýza a sběr požadavků

Tento dokument obsahuje popis obrázků s prefixem `03.prednaska` získaných z podkladů k přednášce. Popisy jsou doplněny o kontext z odpovídajících slidů PDF prezentace zaměřených primárně na Use Case modely (modely případů užití).

## Přehled diagramů a schémat

### 03.prednaska-016.jpg (Slide 11)
**Téma:** Diagram balíčků
**Popis:** Ukázka rozdělení systému do balíčků (packages). Zobrazeny jsou dva balíčky představující logické oblasti systému: "Evidence čtenářů" a "Správa výpůjček".

### 03.prednaska-018.jpg (Slide 12)
**Téma:** Vlastní profil (rozšíření UML)
**Popis:** Ukázka alternativní reprezentace požadavků, obdélníky představující konkrétní funkční požadavky, např. "F1 - Evidování knih" a "F2 - Správa výpůjček".

### 03.prednaska-030.jpg (Slide 23)
**Téma:** Specifický aktér (Čas)
**Popis:** Dva způsoby znázornění specifického aktéra "Čas", který reprezentuje automaticky spouštěné úlohy na základě časové události:
- Klasický symbol aktéra (panáček) s popiskem "Čas".
- Třída se stereotypem `«actor»` a názvem "Čas" (obdélník).

### 03.prednaska-032.jpg (Slide 24)
**Téma:** Účastníci / Aktéři
**Popis:** Zobrazení dvou hlavních lidských aktérů systému pomocí standardních UML symbolů (panáčků): "Knihovník" a "Čtenář".

### 03.prednaska-034.jpg (Slide 25)
**Téma:** Generalizace mezi účastníky
**Popis:** Hierarchie aktérů pomocí vztahu generalizace (dědičnosti). Aktér "Knihovník" dědí od aktéra "Čtenář" (šipka s prázdnou trojúhelníkovou hlavičkou směřuje od Knihovníka k Čtenáři). Znamená to, že Knihovník může spouštět i všechny případy užití určené pro Čtenáře.

### 03.prednaska-037.jpg (Slide 27)
**Téma:** Diagram případů užití (Use Case diagram) - Celek
**Popis:** Komplexní Use Case diagram zachycující hranice systému (obdélník "IS knihovny") a případy užití:
- **Knihovník** interaguje s: "Vložit novou knihu", "Zaznamenat výpůjčení a vrácení výtisků", "Registrovat čtenáře".
- **Čtenář** interaguje s: "Vyhledat knihu".

### 03.prednaska-043.jpg (Slide 32)
**Téma:** Grafické zachycení scénářů (Diagram aktivit)
**Popis:** Detailní diagram aktivit rozvádějící kroky případu užití "Vložit novou knihu". Zobrazuje složitý tok (např. větvení pro "ruční připojení fotografie" vs. "Vložení obalu ze skeneru"). Používá se v situacích, kdy je textový scénář příliš komplikovaný na pochopení všech možných průchodů.

### 03.prednaska-045.jpg (Slide 33)
**Téma:** Identifikace shodných částí scénářů
**Popis:** Výřez Use Case diagramu, kde aktér "Knihovník" komunikuje s případy užití "Upravit údaje o knize" a "Odstranit knihu". Tato část slouží jako základ pro demonstraci relace `«include»`.

### 03.prednaska-048.jpg (Slide 35)
**Téma:** Relace `«include»`
**Popis:** Diagram znázorňující vyčlenění společné funkčnosti. Případy užití "Upravit údaje o knize" a "Odstranit knihu" mají čárkovanou závislostní šipku se stereotypem `«include»` směřující k případu užití "Zobrazit seznam knih". Znamená to, že oba případy užití tento krok povinně obsahují/volají.

### 03.prednaska-051.jpg (Slide 37)
**Téma:** Relace `«extend»`
**Popis:** Diagram znázorňující volitelné rozšíření. Případ užití "Vyhledat knihu" může za určitých podmínek ("zobrazení seznamu") rozšířit jiný případ užití. Čárkovaná šipka se stereotypem `«extend»` směřuje od rozšiřujícího Use Case (Vyhledat knihu) k základnímu Use Case.

### 03.prednaska-061.jpg (Slide 46)
**Téma:** Typické chyby - Tok událostí v UC
**Popis:** Přeškrtnutý (chybný) Use Case diagram. Diagram se snaží znázornit sekvenci kroků ("Vyhledat knihu" -> "Upravit údaje o knize" -> "Uložit změny") pomocí vztahů mezi Use Casy. Pro modelování toku událostí se však UC diagram nehodí, k tomu slouží textové scénáře nebo diagramy aktivit.

### 03.prednaska-063.jpg (Slide 47)
**Téma:** Typické chyby - Datová úložiště v UC
**Popis:** Přeškrtnutý (chybný) Use Case diagram. Případ užití "Vložit novou knihu" má vztah k Use Case nazvanému "Databáze knih". Use Case diagram neznázorňuje datové paměti či úložiště.

### 03.prednaska-065.jpg (Slide 48)
**Téma:** Typické chyby - Chybějící aktér
**Popis:** Diagram ukazuje případ užití "Půjčit knihu" osamocený uvnitř hranic systému, bez jakéhokoliv napojeného aktéra (červeně zakroužkováno). Každý Use Case by měl mít smysl a být spouštěn nebo využíván nějakým aktérem.

### 03.prednaska-067.jpg (Slide 49)
**Téma:** Typické chyby - Činnosti mimo systém
**Popis:** Diagram zobrazuje aktéra "Čtenář" napojeného na případ užití "Přečíst knihu". Tato činnost (čtení fyzické knihy) se však odehrává zcela mimo informační systém a neměla by tak být v UC diagramu tohoto systému modelována.
