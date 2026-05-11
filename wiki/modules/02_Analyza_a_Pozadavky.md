# Analýza a sběr požadavků

**Shrnutí**: Tato sekce se zabývá analytickou fází vývoje softwaru, od pochopení obchodních procesů zákazníka přes specifikaci požadavků až po vytvoření doménového modelu.

**Zdroje**:




---

## Role analytika a proces analýzy

Hlavním úkolem [[role-analytika|analytika]] je odpovědět na otázku: **„Co bude systém dělat?“**. Analytik funguje jako most mezi zákazníkem (business světem) a vývojovým týmem (technickým světem).

- **Cíl**: Minimalizovat riziko, že se postaví systém, který nikdo nepotřebuje.

- **Činnosti**: Sběr požadavků (interview, workshopy), analýza procesů, tvorba modelů a specifikace.

## Modelování obchodních procesů

Před samotným návrhem systému je nutné pochopit [[obchodni-procesy|obchodní procesy]] zákazníka.

- **AS IS (Současný stav)**: Popisuje realitu bez nového systému. Slouží k odhalení slabých míst.

- **TO BE (Budoucí stav)**: Návrh, jak budou procesy vypadat po nasazení systému.

### Diagram aktivit (UML)
Pro vizualizaci procesů se využívá [[diagram-aktivit|UML diagram aktivit]]. 

- **Princip toku tokenů**: Akce se spustí, když do ní dorazí "značka" (token).

- **Klíčové prvky**:
    - **Rozhodnutí (Decision)**: Větvení toku na základě podmínky.
    - **Fork / Join**: Paralelizace a následná synchronizace toku.
    - **Zóny zodpovědnosti (Swimlanes)**: Rozdělení aktivit podle aktérů, kteří je provádějí.

![[imgs/02.prednaska-023.jpg|470]]

## Specifikace požadavků

[[pozadavky|Požadavky]] definují vlastnosti a omezení systému. Musí být **jednoznačné**, **splnitelné** a především **ověřitelné** (aby šlo otestovat, zda byly splněny).

### Kategorizace FURPS+
| Kategorie | Popis |
| :--- | :--- |
| **F** (Functionality) | Co systém dělá (případy užití, bezpečnost, workflow). |
| **U** (Usability) | Snadnost ovládání, lidské faktory, nápověda, dokumentace. |
| **R** (Reliability) | Spolehlivost, četnost poruch, dostupnost systému (uptime). |
| **P** (Performance) | Rychlost odezvy, propustnost, využití prostředků. |
| **S** (Supportability) | Snadnost údržby, instalace, konfigurace, rozšiřitelnost. |

### Techniky zachycení požadavků

- **[[pripady-uziti|Případy užití (Use Cases)]]**: Formální popis interakce (Aktér -> Systém). Obsahují hlavní scénář a alternativní/chybové toky.

- **[[uzivatelske-pribehy|Uživatelské příběhy (User Stories)]]**: Agilní technika. Formát: „Jako **[role]** chci **[cíl]**, abych **[přínos]**.“ Doplňují se o akceptační kritéria.

## Analýza problémové domény

[[domenovy-model|Doménový model]] zachycuje klíčové pojmy (entity), jejich atributy a vztahy v reálném světě.

- **Asociace**: Vztah mezi dvěma třídami (včetně násobnosti).

- **Agregace / Kompozice**: Vztah "celek-část". U kompozice část zaniká s celkem (např. Budova-Místnost).

- **Generalizace**: Vztah nadřazenosti a podřazenosti (dědičnost).

**Důležité**: Doménový model se vyhýbá implementačním detailům (databáze, GUI). Pro zachycení stavů objektu v čase se využívá [[stavovy-diagram|stavový diagram]].

![[imgs/04.prednaska-037.jpg|520]]

*Obrázek: Celkový analytický doménový model knihovny.*

## Související stránky

- [[role-analytika]]

- [[obchodni-procesy]]

- [[pozadavky]]

- [[pripady-uziti]]

- [[uzivatelske-pribehy]]

- [[domenovy-model]]

- [[diagram-aktivit]]

- [[diagram-pripadu-uziti]]

---
#analyza #pozadavky #procesy #uml #domena #BI-SWI
