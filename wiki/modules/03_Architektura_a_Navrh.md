# Architektura a návrh softwaru

**Shrnutí**: Tato sekce pokrývá fázi návrhu softwaru, od definice celkové architektury a vrstvení systému přes detailní návrh tříd až po využití návrhových vzorů a persistenci dat.

**Zdroje**:

- `wiki/lectures/05-navrh-softwarovych-systemu.md`
- `wiki/lectures/06-architektonicke-vzory.md`
- `wiki/lectures/07-navrhove-vzory-a-komponenty.md`

**Naposledy aktualizováno**: 2026-05-18

---

## Od analýzy k návrhu

Zatímco analýza odpovídá na otázku "Co má systém dělat?", [[navrh-softwaru|návrh (Design)]] hledá technickou odpověď na otázku **"Jak?"**. Zodpovědnost v této fázi přebírá Solution Architekt, který rozhoduje o výběru technologií, programovacího jazyka a paradigmatu (dominantně [[objektove-paradigma|objektového]]).

## Softwarová architektura

[[softwarova-architektura|Architektura]] se zaměřuje na rozdělení systému do udržovatelných a nezávislých částí.

- **Logická architektura**: Organizace kódu do balíčků a jmenných prostorů. Pro vizualizaci logických celků a jejich závislostí se používá [[diagram-balicku|diagram balíčků]].
- **Fyzická architektura**: Rozdělení systému na samostatně nasaditelné [[komponenty-a-rozhrani|komponenty]] a jejich rozmístění na hardware.

### Vícevrstvé architektury
Standardem pro podnikové systémy je rozdělení do [[vrstvy-architektury|logických vrstev]] (typicky Prezentační, Business a Datová). Závislosti by měly směřovat vždy shora dolů. 

V prezentační vrstvě se pro oddělení dat od jejich zobrazení využívají vzory **[[mvc-mvp|MVC]]** (Model-View-Controller) nebo **MVP** (Model-View-Presenter), který lépe izoluje pohled pro testování.

## Persistence dat a mapování

Většina systémů vyžaduje trvalé uložení dat v relačních databázích. Protože relační svět nepodporuje dědičnost, využívají se vzory pro **[[mapovani-dedicnosti|mapování dědičnosti]]**:

- **Single Table Inheritance**: Jedna tabulka pro celou hierarchii.
- **Concrete Table Inheritance**: Tabulka pro každou konkrétní třídu.
- **Class Table Inheritance**: Tabulka pro každou třídu v hierarchii spojená cizími klíči.

## Detailní návrh a spolupráce objektů

Na základě analýzy vzniká detailní **[[navrhovy-model-trid|návrhový model tříd]]**, který obsahuje konkrétní datové typy, viditelnost a metody. Při přiřazování zodpovědností se uplatňují principy **GRASP** (např. Informační expert, Nízká provázanost).

Dynamické chování systému a interakce mezi instancemi tříd v čase zachycuje **[[sekvencni-diagram|sekvenční diagram]]**. Pro vizualizaci aktuálního stavu dat v konkrétní okamžik slouží **[[objektovy-diagram|objektový diagram]]**.

## Komponenty a rozhraní

Modularita systému je zajištěna pomocí [[komponenty-a-rozhrani|rozhraní (Interface)]], která oddělují specifikaci od implementace. Pro flexibilní správu závislostí se využívá princip **[[dependency-injection|Dependency Injection]]**, kde objekty své spolupracovníky nevytvářejí, ale dostávají je zvenčí (vstřikování).

## Návrhové vzory (GoF)

Pro řešení opakujících se problémů v objektovém návrhu se využívají osvědčené **[[navrhove-vzory-gof|návrhové vzory GoF]]**:

- **Vytváření**: Abstract Factory, Builder.
- **Chování**: State (nahrazuje složitá větvení životním cyklem), Observer.
- **Struktura**: Adapter (propojení nekompatibilních rozhraní).

## Související stránky

- [[softwarova-architektura]]
- [[navrh-softwaru]]
- [[vrstvy-architektury]]
- [[navrhovy-model-trid]]
- [[komponenty-a-rozhrani]]
- [[navrhove-vzory-gof]]
- [[mvc-mvp]]
- [[sekvencni-diagram]]
- [[diagram-balicku]]
- [[mapovani-dedicnosti]]
- [[dependency-injection]]

---
#architektura #navrh #vzory #uml #komponenty #persistence #BI-SWI
