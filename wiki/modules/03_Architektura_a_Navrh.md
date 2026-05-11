# Architektura a návrh softwaru

**Shrnutí**: Tato sekce pokrývá fázi návrhu softwaru, od definice celkové architektury a vrstvení systému přes detailní návrh tříd až po využití návrhových vzorů a persistenci dat.

**Zdroje**:




---

## Od analýzy k návrhu

Zatímco analýza odpovídá na otázku "Co má systém dělat?", [[navrh-softwaru|návrh (Design)]] hledá technickou odpověď na otázku **"Jak?"**. Zodpovědnost v této fázi přebírá Architekt, který rozhoduje o výběru technologií a rozdělení systému na komponenty. Většina moderních systémů využívá [[objektove-paradigma|objektové paradigma]].

## Softwarová architektura

[[softwarova-architektura|Architektura]] představuje základní organizaci systému. Dělí se na:

- **Logická architektura**: Organizace kódu do jmenných prostorů a vrstev. Pro vizualizaci se používá [[diagram-balicku|diagram balíčků]].

- **Fyzická architektura**: Fyzické rozdělení systému na nasaditelné uzly (servery, zařízení). Modeluje se pomocí diagramu nasazení a diagramu [[komponenty-a-rozhrani|komponent]].

### Architektonické vzory a vrstvení
Standardem pro podnikové aplikace je rozdělení do [[vrstvy-architektury|logických vrstev]]:

1. **Prezentační vrstva**: Zajišťuje interakci s uživatelem.

2. **Business (Aplikační) vrstva**: Obsahuje hlavní logiku aplikace.

3. **Datová vrstva**: Komunikuje s databází nebo externími API.
Závislosti vždy směřují shora dolů (Prezentační -> Business -> Datová).

Pro oddělení prezentační vrstvy se často využívají vzory jako **[[mvc-mvp|MVC]]** (Model-View-Controller) nebo **MVP** (Model-View-Presenter), které umožňují snazší testování uživatelského rozhraní.

## Detailní návrh a model tříd

Z analytického doménového modelu vzniká detailní **[[navrhovy-model-trid|návrhový model tříd]]**, který již obsahuje implementační detaily (typy atributů, metody, viditelnost public/private).

Při navrhování tříd a přiřazování zodpovědností se architekti řídí principy **GRASP**:

- **Informační expert**: Třída by měla dělat to, na co má data.

- **Nízká provázanost (Low Coupling)**: Změna v jedné třídě by neměla ovlivnit ostatní.

- **Vysoká soudržnost (High Cohesion)**: Třída by měla mít jasně vymezený účel.

Chování systému v čase a komunikaci mezi objekty zachycuje **[[sekvencni-diagram|sekvenční diagram]]**. Pillířem nezávislých komponent je používání rozhraní a principu **[[dependency-injection|Dependency Injection]]**, kdy třída nedostává volnost vytvářet si své závislosti sama, ale jsou jí předány.

## Návrhové vzory (GoF)

[[navrhove-vzory-gof|Návrhové vzory (Design Patterns)]] podle skupiny Gang of Four představují standardizovaná řešení opakujících se problémů. Dělí se na:

- **Vytvářecí**: Řeší inicializaci objektů (např. *Abstract Factory*, *Builder*, *Singleton*).

- **Strukturální**: Řeší skládání tříd do větších celků (např. *Adapter*, *Composite*, *Facade*).

- **Chování**: Řeší komunikaci mezi objekty a distribuci zodpovědnosti (např. *Observer*, *State*, *Strategy*).

## Persistence dat a mapování

Relační databáze neumí pracovat s objektovými koncepty (např. dědičností). Pro řešení tohoto "Impedance Mismatch" se využívají vzory pro **[[mapovani-dedicnosti|mapování dědičnosti]]**:

- **Single Table Inheritance**: Celá hierarchie tříd se uloží do jedné velké tabulky. Rychlé, ale obsahuje mnoho NULL hodnot.

- **Concrete Table Inheritance**: Každá konkrétní třída má vlastní tabulku obsahující i zděděné atributy.

- **Class Table Inheritance**: Každá třída v hierarchii má tabulku jen pro své atributy, spojují se pomocí JOIN (cizí klíče).

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