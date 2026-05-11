# Diagram aktivit (UML)

**Shrnutí**: Diagram chování v UML používaný k modelování procedurální logiky, obchodních procesů a algoritmů. Je založen na principu toku tokenů.

**Zdroje**:

- `raw/lectures/02.prednaska.pdf`
- `raw/extra/Activity Diagram.pdf`



---

[[diagram-aktivit|UML Diagram aktivit]] (Activity Diagram) patří do skupiny diagramů chování. Umožňuje srozumitelné zachycení procesů, rychlou kontrolu logiky a snazší odhady pracnosti.

![[imgs/02.prednaska-023.jpg|470]]

*Obrázek: Příklad základního procesu v diagramu aktivit se zónami zodpovědnosti.*


## Princip toku tokenů
Čtení diagramu je založeno na tzv. **hře s tokeny**. Token je virtuální značka, která se pohybuje po hranách diagramu a aktivuje jednotlivé uzly.

## Základní prvky
### Akční uzly (Action Nodes)

- **Akce**: Základní krok procesu (obdélník se zaoblenými rohy).
- **Volání aktivity (Call Behavior)**: Označeno symbolem "hrábí", reprezentuje spuštění jiného diagramu.
- Akce se spustí, jakmile obdrží tokeny na všech vstupních hranách. Po dokončení vygeneruje tokeny na všech výstupních hranách.

![[imgs/02.prednaska-028.jpg|82]]

*Obrázek: Různé typy akčních uzlů (základní akce, volání aktivity, odeslání/přijetí události).*

### Řídící uzly (Control Nodes)

- **Počáteční uzel (Initial Node)**: Plné kolečko. Nemá vstupní hrany, při spuštění generuje řídící token.
- **Koncový uzel aktivity (Activity Final Node)**: Terčík. Ukončuje celou instanci aktivity (všechny toky).
- **Konec toku (Flow Final Node)**: Kolečko s křížkem. Ukončuje pouze danou větev.
- **Rozhodovací uzel (Decision Node)**: Kosočtverec. Má jeden vstup a více výstupů s výlučnými podmínkami.
- **Slučovací uzel (Merge Node)**: Kosočtverec. Má více vstupů a jeden výstup. Přeposílá každý příchozí token.
- **Rozvětvení (Fork)**: Silná čára. Jeden vstup, více výstupů. Token se duplikuje do všech větví.
- **Spojení (Join)**: Silná čára. Více vstupů, jeden výstup. Čeká na tokeny ze všech větví.

![[imgs/02.prednaska-030.jpg|55]] ![[imgs/02.prednaska-032.jpg|228]]

*Obrázek: Legenda řídících uzlů a příklady větvení toku.*

### Zóny zodpovědnosti (Swimlanes)
Rozdělují diagram do sloupců nebo řádků podle rolí (např. Student, Učitel, Systém), které jsou za dané akce zodpovědné.

![[imgs/02.prednaska-034.jpg|671]]

*Obrázek: Ukázka rozdělení diagramu do zón zodpovědnosti (Swimlanes).*

### Objektové uzly (Object Nodes)
Reprezentují data nebo fyzické objekty předávané mezi akcemi (obdélník).

- **Tok objektů**: Zobrazení, jak jedna akce produkuje objekt a druhá jej přijímá. Lze využít buď samostatný obdélník mezi akcemi, nebo tzv. "piny" přímo na hraně akce.

    ![[imgs/02.prednaska-036.jpg|250]] ![[imgs/02.prednaska-037.jpg|250]]

- **Pojmenování a stavy**: U objektů lze specifikovat konkrétní název instance (`jméno:Třída`) nebo anonymní instanci (`:Třída`). V hranatých závorkách se uvádí **stav objektu** (např. `[Vytvořena]`).

    ![[imgs/02.prednaska-043.jpg|150]]


## Pokročilé konstrukce

- **Vícenásobné provedení (Expansion Region)**: Oblast, kde se akce provádí pro každý prvek vstupní kolekce.
    ![[imgs/02.prednaska-039.jpg|250]]

- **Region přerušení (Interruptible Region)**: Oblast, jejíž provádění může být přerušeno specifikovanou událostí.
    ![[imgs/02.prednaska-041.jpg|400]]


## Komplexní příklad
![[imgs/02.prednaska-045.jpg|488]]

*Obrázek: Komplexní model procesu rezervace knihy se všemi prvky.*

## Časté chyby

1.  **Chybné modelování cyklu**: Sloučení zpětné vazby přímo do akce namísto použití slučovacího uzlu (Merge). To způsobí "zaseknutí" (deadlock), protože akce čeká na token z obou vstupů.

    | Špatně | Dobře |
    | :---: | :---: |
    | ![[imgs/02.prednaska-049.jpg|150]] | ![[imgs/02.prednaska-051.jpg|150]] |

2.  **Míchání akcí a stavů**: Používání symbolu akce pro zachycení stavu objektu. Správně má být stav v hranatých závorkách uvnitř objektového uzlu.

    | Špatně | Dobře |
    | :---: | :---: |
    | ![[imgs/02.prednaska-053.jpg|150]] | ![[imgs/02.prednaska-055.jpg|150]] |

## Související stránky

- [[obchodni-procesy]]
- [[role-analytika]]

---
#uml #activity-diagram #procesy #tokeny #swi #BI-SWI
