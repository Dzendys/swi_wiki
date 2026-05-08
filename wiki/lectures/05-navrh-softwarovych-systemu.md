# 05. Návrh softwarových systémů

**Shrnutí**: Pátá přednáška pokrývá přechod od analýzy k návrhu, volbu technologií, mapování objektů do relační databáze a architektonický i třídní návrh systému.

**Zdroje**:
- `raw/lectures/05.prednaska.pdf`
- `raw/extra/Single Table Inheritance.pdf`
- `raw/extra/Concrete Table Inheritance.pdf`
- `raw/extra/Class Table Inheritance.pdf`
- `raw/extra/GRASP.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Tato přednáška vysvětluje posun v procesu vývoje softwaru od fáze analýzy k fázi [[navrh-softwaru|návrhu]]. Analytika, který odpovídal na otázku "Co?", střídá Solution Architekt, který řeší "Jak?" se to provede. 

## Klíčová témata přednášky

### 1. Od analýzy k návrhu
Zatímco analytický doménový model a případy užití definují požadavky, návrh se zabývá jejich realizací. To zahrnuje volbu programovacího jazyka (dnes převážně OO), volbu a popis uložení dat a definici [[softwarova-architektura|softwarové architektury]].

### 2. Návrh uložení dat
Probírá se reprezentace databázového modelu. Relační databáze jsou stále nejběžnější, což ale u OO jazyků vede na nutnost mapování objektů do tabulek (O/R mapping). 
Speciální pozornost se věnuje **[[mapovani-dedicnosti|mapování dědičnosti]]** do relační DB, pro které existují 3 základní vzory od Martina Fowlera:
- Single Table Inheritance
- Concrete Table Inheritance
- Class Table Inheritance

U samotného diagramu databázového modelu je pro srozumitelnost vhodné skrývat popisky konců asociací a dělit rozsáhlé tabulky do vnořených [[diagram-balicku|diagramů balíčků]].

### 3. Návrh architektury
[[softwarova-architektura|Softwarová architektura]] se dělí na logickou (organizace kódu, vrstvy) a fyzickou (nasazení, výpočetní uzly). Cílem architektury je srozumitelnost, rozšiřitelnost a udržovatelnost. Architektura izoluje místa budoucích změn (např. integraci na externí systém) pomocí zapouzdření a rozhraní, čímž minimalizuje dopad změn. Bylo zmíněno použití návrhových vzorů, jako je *Stavitel (Builder)*, pro řešení opakujících se problémů v návrhu.

### 4. Návrhový model tříd
Slouží pro zdokumentování architektonických rozhodnutí a generování kódů. Na rozdíl od [[domenovy-model|doménového modelu]] obsahuje [[navrhovy-model-trid|návrhový model tříd]] konkrétní datové typy, viditelnost, směry asociací a metody, do kterých jsou přidělovány zodpovědnosti. 
K přidělování zodpovědností se využívají principy **GRASP** (Informační expert, Nízká provázanost, Vysoká soudržnost). Diagram tříd v návrhu se nezabývá každou třídou (např. generovanými gettery), ale zdůrazňuje klíčová architektonická pravidla.

## Související stránky
- [[navrh-softwaru]]
- [[softwarova-architektura]]
- [[mapovani-dedicnosti]]
- [[navrhovy-model-trid]]
- [[diagram-balicku]]

---
#swi #prednaska #navrh #architektura #BI-SWI
