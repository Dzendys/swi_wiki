# Analýza a sběr požadavků

**Shrnutí**: Tato sekce se zabývá analytickou fází vývoje softwaru, od pochopení obchodních procesů zákazníka přes specifikaci požadavků až po vytvoření doménového modelu.

**Zdroje**:

- `wiki/lectures/02-modelovani-obchodnich-procesu.md`
- `wiki/lectures/03-analyza-a-sber-pozadavku.md`
- `wiki/lectures/04-analyza-problemove-domeny.md`

**Naposledy aktualizováno**: 2026-05-18

---

## Role analytika a proces analýzy

Hlavním úkolem [[role-analytika|analytika]] je odpovědět na otázku: **„Co bude systém dělat?“**. Analytik funguje jako most mezi zákazníkem a vývojovým týmem. Musí pochopit prostředí zákazníka, popsat jeho procesy, vymezit rozsah (scope) projektu a specifikovat požadavky tak, aby byly srozumitelné pro vývojáře a ověřitelné pro zákazníka.

## Modelování obchodních procesů

Před samotným návrhem systému je nutné pochopit [[obchodni-procesy|obchodní procesy]] zákazníka. Rozlišujeme dva základní pohledy:
- **AS IS (Současný stav)**: Popisuje, jak procesy fungují dnes. Slouží k identifikaci neefektivit a problémových míst.
- **TO BE (Budoucí stav)**: Návrh procesů po nasazení systému. Definuje, jak bude systém uživatele podporovat.

### Diagram aktivit (UML)
Pro vizualizaci procesů se nejčastěji využívá [[diagram-aktivit|UML diagram aktivit]]. Je založen na **principu toku tokenů**, kde virtuální značky procházejí hranami a aktivují akce. Diagram umožňuje rozdělení do **zón zodpovědnosti (swimlanes)** podle rolí a zachycení paralelních i podmíněných toků.

![[imgs/02.prednaska-023.jpg|470]]

*Obrázek: Příklad procesu v diagramu aktivit se zónami zodpovědnosti.*

## Specifikace požadavků

[[pozadavky|Požadavky]] jsou základem pro odhad pracnosti i akceptační testování. Musí být jednoznačné, splnitelné a především **ověřitelné**.

Kategorizace pomocí modelu **FURPS**:
- **F** (Functionality): Funkční požadavky (co má systém dělat).
- **U** (Usability): Použitelnost a lidské faktory.
- **R** (Reliability): Spolehlivost a dostupnost.
- **P** (Performance): Výkon a doba odezvy.
- **S** (Supportability): Podporovatelnost a rozšiřitelnost.

### Techniky zachycení požadavků

- **[[pripady-uziti|Případy užití (Use Cases)]]**: Formální popis interakcí mezi aktéry a systémem k dosažení cíle. Jsou typické pro klasické metodiky (UP). Skládají se z [[diagram-pripadu-uziti|diagramu]] a textových scénářů.
- **[[uzivatelske-pribehy|Uživatelské příběhy (User Stories)]]**: Méně formální zápis („Jako [role] chci [cíl], abych [přínos]“), typický pro [[agilni-vyvoj|agilní vývoj]] a frameworky jako [[scrum]].

## Analýza problémové domény

Výsledkem hloubkové analýzy dat a entit je [[domenovy-model|doménový model]]. Tento model zachycuje klíčové pojmy reálného světa, jejich atributy a vztahy (asociace, kompozice, generalizace). 

Při tvorbě modelu se analytik vyhýbá implementačním detailům (např. cizím klíčům) a soustředí se na správnou dekompozici (např. rozlišení mezi popisem a instancí – Kniha vs. Výtisk). Pro zachycení složitého chování entit v čase se využívá [[stavovy-diagram|stavový diagram]].

![[imgs/04.prednaska-032.jpg|520]]

*Obrázek: Celkový pohled na analytický doménový model knihovny.*

## Související stránky
- [[role-analytika]]
- [[obchodni-procesy]]
- [[pozadavky]]
- [[pripady-uziti]]
- [[uzivatelske-pribehy]]
- [[domenovy-model]]
- [[diagram-aktivit]]
- [[diagram-pripadu-uziti]]
- [[objektove-paradigma]]

---
#analyza #pozadavky #procesy #uml #domena #BI-SWI
