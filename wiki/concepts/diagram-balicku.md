# Diagram balíčků (UML)

**Shrnutí**: Strukturální diagram v UML používaný k organizaci modelových elementů do logických skupin (balíčků). Slouží k rozdělení rozsáhlých systémů na přehledné oblasti.

**Zdroje**:
- `raw/lectures/03.prednaska.pdf`
- `raw/lectures/05.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Diagram balíčků (Package Diagram) je klíčový pro zachycení struktury systému na vyšší úrovni abstrakce než [[domenovy-model|diagram tříd]]. Umožňuje seskupit třídy, případy užití nebo i jiné balíčky do logických celků – **balíčků**. V kontextu [[softwarova-architektura|softwarové architektury]] slouží k vizualizaci logické architektury (např. vrstev a podsystémů).

## Účel
Hlavním účelem je řídit složitost (komplexitu) velkých systémů. Balíčky by měly být navrženy tak, aby představovaly ucelené, relativně nezávislé moduly. Pomáhají při:
- Logické organizaci modelu.
- Zobrazení architektonických vrstev nebo subsystémů.
- Zobrazení závislostí mezi moduly.

## Notace a Vztahy
- **Balíček (Package)**: Kreslí se jako složka (obdélník s menším obdélníkem vlevo nahoře). Jméno balíčku je buď uvnitř velkého obdélníku, nebo v malém "oušku".
- **Závislost (Dependency)**: Kreslí se jako přerušovaná čárkovaná šipka mezi balíčky, značící, že jeden balíček využívá elementy jiného balíčku.
- **Vnoření**: Balíčky mohou obsahovat jiné balíčky. Kreslí se buď fyzickým vnořením symbolu složky dovnitř jiné, nebo pomocí textového zápisu `BalíčekA::BalíčekB`.

## Cyklické závislosti
Velkým problémem v diagramu balíčků jsou **cyklické závislosti** (Balíček A závisí na B a B závisí zpět na A). Cykly ztěžují lokalizaci dopadů změn a komplikují rozšiřitelnost. 
Řešením cyklických závislostí je:
- Přesun problémové třídy.
- Vyčlenění tříd tvořících cyklus do nového balíčku.
- Vytvoření rozhraní a uplatnění principu inverze závislostí (Dependency Inversion).

## Související stránky
- [[softwarova-architektura]]
- [[domenovy-model]]
- [[navrh-softwaru]]

---
#uml #package-diagram #analyza #architektura #organizace #swi #BI-SWI