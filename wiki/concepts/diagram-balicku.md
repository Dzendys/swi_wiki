# Diagram balíčků (UML)

**Shrnutí**: Strukturální diagram v UML používaný k organizaci modelových elementů do logických skupin (balíčků). Slouží k rozdělení rozsáhlých systémů na přehledné oblasti.

**Zdroje**:
- `raw/lectures/03.prednaska.pdf`
- `raw/lectures/05.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Diagram balíčků (Package Diagram) je klíčový pro zachycení struktury systému na vyšší úrovni abstrakce než [[domenovy-model|diagram tříd]]. Umožňuje seskupit třídy, případy užití nebo i jiné balíčky do logických celků – **balíčků**. V kontextu [[softwarova-architektura|softwarové architektury]] slouží k vizualizaci logické architektury (např. vrstev a podsystémů).

## Účel
Hlavním účelem je řídil složitost (komplexitu) velkých systémů. Balíčky by měly být navrženy tak, aby představovaly ucelené, relativně nezávislé moduly. Pomáhají při:

![[imgs/03.prednaska-016.jpg|188]] ![[imgs/05.prednaska-030.jpg|815]]
*Obrázek: Rozdělení systému do logických balíčků (Evidence čtenářů, Evidence knih, Evidence výpůjček).*

Pomáhají při:
- Logické organizaci modelu.
- Zobrazení architektonických vrstev nebo subsystémů.
- Zobrazení závislostí mezi moduly.

## Notace a Vztahy
- **Balíček (Package)**: Kreslí se jako složka (obdélník s menším obdélníkem vlevo nahoře). Jméno balíčku je buď uvnitř velkého obdélníku, nebo v malém "oušku".
- **Závislost (Dependency)**: Kreslí se jako přerušovaná čárkovaná šipka mezi balíčky, značící, že jeden balíček využívá elementy jiného balíčku.

![[imgs/05.prednaska-039.jpg|107]]
*Obrázek: Základní jednosměrná závislost (Balíček A závisí na Balíčku B).*

### Vnoření balíčků
Balíčky mohou obsahovat jiné balíčky. V UML existuje několik způsobů, jak vnoření (nesting) znázornit:
1.  **Pomocí ikon**: Vnitřní balíčky jsou reprezentovány ikonami složek uvnitř jmenného prostoru nadřazeného balíčku.
2.  **Grafické vnoření**: Obdélníky vnitřních balíčků jsou nakresleny fyzicky uvnitř těla nadřazeného balíčku.
3.  **Kompoziční vazba**: Explicitní definice členství pomocí čáry s křížkem v kroužku.

![[imgs/05.prednaska-045.jpg|610]] ![[imgs/05.prednaska-046.jpg|842]] ![[imgs/05.prednaska-047.jpg|560]]
*Obrázek: Různé notace pro zobrazení hierarchie a vnořování balíčků.*

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
