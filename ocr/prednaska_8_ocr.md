# Analýza obrázků - Přednáška 8: Implementace

Tento dokument obsahuje popis obrázků s prefixem `08.prednaska` získaných z podkladů k přednášce. Popisy se zaměřují na objektové paradigma, diagramy objektů a základní pravidla čistého návrhu (clean code).

## Přehled diagramů a schémat

### 08.prednaska-020.jpg (Slide 15)
**Téma:** Základy objektového diagramu
**Popis:** Ukázka jednoduchého objektového diagramu v UML. Zobrazuje instance konkrétních tříd:
- Dvě instance třídy `Vytisk` (jedna ve stavu `[Volný]`, druhá ve stavu `[Vypůjčený]` s konkrétními hodnotami atributů jako `datumVyrazeni`, `rokNakupu`, `evidencniCislo` a `porizovaciCena`).
- Instance tříd `Autor` a `Kniha`, které jsou propojeny asociací (linkou), představující konkrétní spojení v daný okamžik.

### 08.prednaska-022.jpg (Slide 16)
**Téma:** Komplexní diagram objektů s daty
**Popis:** Detailní příklad objektového diagramu modelujícího konkrétní data v systému knihovny:
- Instance `Autor` (Božena Němcová).
- Dvě instance `Kniha` (Babička, V zámku a v podzámčí).
- Tři instance `Vytisk` s různými stavy (Volný, Vypůjčený) a různými roky nákupu.
- Diagram jasně ukazuje multiplicity v praxi (jeden autor napsal více knih, jedna kniha má více konkrétních výtisků).

### 08.prednaska-032.jpg (Slide 25)
**Téma:** Nevhodné použití dědičnosti (Liskov Substitution Principle)
**Popis:** Klasický příklad porušení principu zastupitelnosti (LSP) pomocí dědičnosti mezi třídami `Obdelník` a `Čtverec`. 
- `Obdelník` má nezávislé atributy `vyska` a `sirka`.
- `Čtverec` dědí z Obdélníku, ale v metodách `setVyska` a `setSirka` musí vynucovat rovnost obou rozměrů.
- Toto vede k neočekávanému chování, pokud klient očekává obecný Obdélník a dostane instanci Čtverce (např. nastavení šířky neočekávaně změní i výšku).
