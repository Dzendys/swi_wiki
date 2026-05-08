# Diagram aktivit (UML)

**Shrnutí**: Diagram chování v UML používaný k modelování procedurální logiky, obchodních procesů a algoritmů. Je založen na principu toku tokenů.

**Zdroje**:
- `raw/lectures/02.prednaska.pdf`
- `raw/extra/Activity Diagram.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

[[diagram-aktivit|UML Diagram aktivit]] (Activity Diagram) patří do skupiny diagramů chování. Umožňuje srozumitelné zachycení procesů, rychlou kontrolu logiky a snazší odhady pracnosti (zdroj: raw/lectures/02.prednaska.pdf).

![[imgs/02.prednaska-023.jpg|352]]
*Obrázek: Příklad základního procesu v diagramu aktivit se zónami zodpovědnosti.*

## Princip toku tokenů
Čtení diagramu je založeno na tzv. **hře s tokeny**. Token je virtuální značka, která se pohybuje po hranách diagramu a aktivuje jednotlivé uzly (zdroj: raw/extra/Activity Diagram.pdf).

## Základní prvky
### Akční uzly (Action Nodes)
- **Akce**: Základní krok procesu (obdélník se zaoblenými rohy).
- **Volání aktivity (Call Behavior)**: Označeno symbolem "hrábí", reprezentuje spuštění jiného diagramu (zdroj: raw/extra/Activity Diagram.pdf).
- Akce se spustí, jakmile obdrží tokeny na všech vstupních hranách. Po dokončení vygeneruje tokeny na všech výstupních hranách (zdroj: raw/extra/Activity Diagram.pdf).

![[imgs/02.prednaska-028.jpg|66]]
*Obrázek: Různé typy akčních uzlů (základní akce, volání aktivity, odeslání/přijetí události).*

### Řídící uzly (Control Nodes)
- **Počáteční uzel (Initial Node)**: Plné kolečko. Nemá vstupní hrany, při spuštění generuje řídící token (zdroj: raw/extra/Activity Diagram.pdf).
- **Koncový uzel aktivity (Activity Final Node)**: Terčík. Ukončuje celou instanci aktivity (všechny toky) (zdroj: raw/lectures/02.prednaska.pdf).
- **Konec toku (Flow Final Node)**: Kolečko s křížkem. Ukončuje pouze danou větev (zdroj: raw/lectures/02.prednaska.pdf).
- **Rozhodovací uzel (Decision Node)**: Kosočtverec. Má jeden vstup a více výstupů s výlučnými podmínkami (zdroj: raw/extra/Activity Diagram.pdf).
- **Slučovací uzel (Merge Node)**: Kosočtverec. Má více vstupů a jeden výstup. Přeposílá každý příchozí token (zdroj: raw/extra/Activity Diagram.pdf).
- **Rozvětvení (Fork)**: Silná čára. Jeden vstup, více výstupů. Token se duplikuje do všech větví (zdroj: raw/extra/Activity Diagram.pdf).
- **Spojení (Join)**: Silná čára. Více vstupů, jeden výstup. Čeká na tokeny ze všech větví (zdroj: raw/extra/Activity Diagram.pdf).

![[imgs/02.prednaska-030.jpg|44]] ![[imgs/02.prednaska-032.jpg|182]]
*Obrázek: Legenda řídících uzlů a příklady větvení toku.*

### Zóny zodpovědnosti (Swimlanes)
Rozdělují diagram do sloupců nebo řádků podle rolí (např. Student, Učitel, Systém), které jsou za dané akce zodpovědné (zdroj: raw/lectures/02.prednaska.pdf).

![[imgs/02.prednaska-034.jpg|503]]
*Obrázek: Ukázka rozdělení diagramu do zón zodpovědnosti (Swimlanes).*

### Objektové uzly (Object Nodes)
Reprezentují data nebo fyzické objekty předávané mezi akcemi (obdélník). Lze u nich v hranatých závorkách uvést **stav objektu** (např. `:Objednávka [Vytvořena]`) (zdroj: raw/lectures/02.prednaska.pdf).

![[imgs/02.prednaska-036.jpg|1391]] ![[imgs/02.prednaska-037.jpg|1322]] ![[imgs/02.prednaska-043.jpg|135]]
*Obrázek: Různé způsoby zobrazení toku objektů a jejich stavů.*

## Pokročilé konstrukce
- **Vícenásobné provedení (Expansion Region)**: Oblast, kde se akce provádí pro každý prvek vstupní kolekce (zdroj: raw/lectures/02.prednaska.pdf).
- **Region přerušení (Interruptible Region)**: Oblast, jejíž provádění může být přerušeno specifikovanou událostí (zdroj: raw/lectures/02.prednaska.pdf).

![[imgs/02.prednaska-039.jpg|186]] ![[imgs/02.prednaska-041.jpg|425]]
*Obrázek: Ukázka vícenásobného provedení a přerušitelné oblasti.*

## Komplexní příklad
![[imgs/02.prednaska-045.jpg|366]]
*Obrázek: Komplexní model procesu rezervace knihy se všemi prvky.*

## Časté chyby
1.  **Chybné modelování cyklu**: Sloučení zpětné vazby přímo do akce namísto použití slučovacího uzlu (Merge). To způsobí "zaseknutí" (deadlock), protože akce čeká na token z obou vstupů (zdroj: raw/extra/Activity Diagram.pdf).
2.  **Míchání akcí a stavů**: Používání symbolu akce pro zachycení stavu objektu. Správně má být stav v hranatých závorkách uvnitř objektového uzlu (zdroj: raw/lectures/02.prednaska.pdf).

![[imgs/02.prednaska-049.jpg|127]] ![[imgs/02.prednaska-051.jpg|117]]
*Obrázek: Typická chyba při modelování cyklu a její správné řešení.*

![[imgs/02.prednaska-053.jpg|189]] ![[imgs/02.prednaska-055.jpg|153]]
*Obrázek: Ukázka nesprávného míchání stavů s akcemi a následná oprava pomocí objektových uzlů.*

## Související stránky
- [[obchodni-procesy]]
- [[role-analytika]]

---
#uml #activity-diagram #procesy #tokeny #swi #BI-SWI
