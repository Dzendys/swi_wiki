# Diagram balíčků (UML)

**Shrnutí**: Strukturální diagram v UML používaný k organizaci modelových elementů do logických skupin (balíčků). Slouží k rozdělení rozsáhlých systémů na přehledné oblasti.

**Zdroje**:

- `raw/lectures/03.prednaska.pdf`
- `raw/lectures/05.prednaska.pdf`



---

Diagram balíčků (Package Diagram) je klíčový pro zachycení struktury systému na vyšší úrovni abstrakce než [[domenovy-model|diagram tříd]]. Umožňuje seskupit třídy, případy užití nebo i jiné balíčky do logických celků – **balíčků**. V kontextu [[softwarova-architektura|softwarové architektury]] slouží k vizualizaci logické architektury (např. vrstev a podsystémů).

## Účel
Hlavním účelem je řídit složitost (komplexitu) velkých systémů. Balíčky by měly být navrženy tak, aby představovaly ucelené, relativně nezávislé moduly. Pomáhají při:

- **Logické organizaci modelu**: Seskupování souvisejících elementů (tříd, UC).
- **Zobrazení architektonických vrstev**: Vizualizace rozdělení systému (viz [[vrstvy-architektury]]).
- **Správě závislostí**: Identifikace a kontrola vazeb mezi moduly.

## Notace a Vztahy

- **Balíček (Package)**: Kreslí se jako ikona složky (obdélník s menším obdélníkem vlevo nahoře). Slouží jako kontejner pro logické seskupení souvisejících elementů, jako jsou třídy, rozhraní nebo případy užití.

![[imgs/05.prednaska-030.jpg|400]]

*Obrázek: Balíček "Evidence výpůjček" obsahující související entity (Ctenar, Vypujcka, Vytisk, Rezervace, Pokuta).*

- **Závislost (Dependency)**: Kreslí se jako přerušovaná čárkovaná šipka mezi balíčky. Znamená to, že **klientský** balíček využívá nebo potřebuje elementy z **dodavatelského** balíčku. Změna v dodavatelském balíčku může ovlivnit balíček klientský.

![[imgs/05.prednaska-039.jpg|107]]

*Obrázek: Základní jednosměrná závislost (Balíček A závisí na Balíčku B).*

### Seskupování a organizace
Balíčky se používají k logickému rozdělení systému na moduly (např. podle doménových oblastí nebo architektonických vrstev).

![[imgs/03.prednaska-016.jpg|188]]

*Obrázek: Rozdělení IS knihovny do modulů "Evidence čtenářů" a "Správa výpůjček".*

### Vnoření balíčků
Balíčky mohou obsahovat jiné balíčky. V UML existuje několik způsobů, jak vnoření (nesting) znázornit:

1.  **Pomocí ikon**: Vnitřní balíčky jsou reprezentovány ikonami složek uvnitř jmenného prostoru nadřazeného balíčku.
    ![[imgs/05.prednaska-045.jpg|200]]


2.  **Grafické vnoření**: Obdélníky vnitřních balíčků jsou nakresleny fyzicky uvnitř těla nadřazeného balíčku.
    ![[imgs/05.prednaska-046.jpg|250]]


3.  **Kompoziční vazba**: Explicitní definice členství pomocí čáry s křížkem v kroužku.
    ![[imgs/05.prednaska-047.jpg|200]]


## Cyklické závislosti
Velkým problémem v diagramu balíčků jsou **cyklické závislosti** (Balíček A závisí na B a B závisí zpět na A). Cykly ztěžují lokalizaci dopadů změn a komplikují rozšiřitelnost.

![[imgs/05.prednaska-041.jpg|147]]

*Obrázek: Problematická obousměrná závislost, která vytváří cyklus.*

Řešením cyklických závislostí je:

- Přesun problémové třídy.
- Vyčlenění tříd tvořících cyklus do nového balíčku (všichni pak závisí na tomto novém společném balíčku).
- Vytvoření rozhraní a uplatnění principu inverze závislostí (Dependency Inversion).

![[imgs/05.prednaska-043.jpg|552]]

*Obrázek: Odstranění cyklu vyčleněním společné logiky do Balíčku C.*

## Související stránky

- [[softwarova-architektura]]
- [[domenovy-model]]
- [[navrh-softwaru]]

---
#uml #package-diagram #analyza #architektura #organizace #swi #BI-SWI
