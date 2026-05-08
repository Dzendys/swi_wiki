# Log změn

## [2026-05-08] - Konsolidace Single Source of Truth (refactor/ssot-consolidation)
- Rozsáhlá refaktorizace celé wiki pro zajištění principu Single Source of Truth.
- Všech 12 stránek přednášek (`wiki/lectures/`) bylo zredukováno na popisné souhrny s odkazy na příslušné koncepty.
- Každé klíčové téma v přednášce je nově stručně vysvětleno několika větami, které uvádějí do kontextu a odkazují na detailní koncepční stránku.
- Technické detaily, pravidla a definice byly definitivně konsolidovány v koncepčních stránkách (`wiki/concepts/`).
- Zajištěno, že každý technický pojem nebo postup je detailně vysvětlen právě na jednom místě.
- Přednášky nyní slouží jako informativní průvodci a rozcestníky pro přípravu na zkoušku.
- Kontrola a prolinkování všech souvisejících stránek.

## [2026-05-08] - Ingest 12. přednášky (ingest/prednaska-12)
- Zpracování přednášky `12.prednaska.pdf`.
- Vytvoření souhrnné stránky [[12-metodiky-a-agilni-vyvoj]].
- Vytvoření konceptu [[metodiky-vyvoje]] (klasické vs. agilní, přínosy, výběr).
- Vytvoření konceptu [[unified-process]] (fáze Inception, Elaboration, Construction, Transition).
- Vytvoření konceptu [[agilni-vyvoj]] (Agilní manifest, principy, výhody a rizika).
- Vytvoření konceptu [[scrum]] (role Scrum Master/PO, artefakty, události, fáze projektu).
- Aktualizace [[softwarove-inzenyrstvi]] (propojení na metodiky).
- Aktualizace [[index]].

## [2026-05-08] - Ingest 11. přednášky (ingest/prednaska-11)
- Zpracování přednášky `11.prednaska.pdf`.
- Vytvoření souhrnné stránky [[11-projektove-rizeni]].
- Vytvoření konceptu [[projektove-rizeni]] (fáze projektu, role manažera, cíle).
- Vytvoření konceptu [[rizeni-rizik]] (evidence, strategie řešení).
- Aktualizace [[odhad-pracnosti]] (metody UCP a COCOMO, historická data, pravidla odhadování).
- Aktualizace [[index]].

## [2026-05-08] - Ingest 10. přednášky (ingest/prednaska-10)
- Zpracování přednášky `10.prednaska.pdf`.
- Vytvoření souhrnné stránky [[10-nasazeni-udrzba-a-integrace]].
- Vytvoření konceptu [[nasazeni-aplikace]] (build nástroje, způsoby nasazení, automatizace).
- Vytvoření konceptu [[podpora-a-udrzba]] (úrovně podpory, SLA, typy údržby, testovací data).
- Vytvoření konceptu [[integrace-aplikaci]] (důvody, problémy, integrační styly).
- Vytvoření konceptu [[webove-sluzby-rest-soap]] (porovnání SOAP vs. REST, JSON vs. XML).
- Aktualizace [[index]].

## [2026-05-08] - Ingest 9. přednášky (ingest/prednaska-09)
- Zpracování přednášky `09.prednaska.pdf`.
- Vytvoření souhrnné stránky [[09-zajisteni-kvality]].
- Vytvoření konceptu [[zajisteni-kvality]] (QA cíle, charakteristiky FURPS, aktivity).
- Vytvoření konceptu [[verifikace-a-validace]] (rozdíly, příklady).
- Vytvoření konceptu [[testovani]] (klasifikace, techniky - Boundary, Equivalence, metriky).
- Aktualizace [[pozadavky]] (propojení s ověřitelností a QA).
- Aktualizace [[index]].

## [2026-05-08] - Ingest 8. přednášky (ingest/prednaska-08)
- Zpracování přednášky `08.prednaska.pdf`.
- Vytvoření souhrnné stránky [[08-implementace]].
- Vytvoření konceptu [[implementace]] (cíle, proces, "návrh v malém").
- Vytvoření konceptu [[objektove-paradigma]] (zapouzdření, dědičnost, polymorfismus).
- Vytvoření konceptu [[objektovy-diagram]] (UML snapshot stavu systému).
- Vytvoření konceptu [[clean-code]] (SRP, DRY, Law of Demeter, LSP, čitelnost).
- Vytvoření konceptu [[refaktoring]] (příznaky, techniky, nutnost testů).
- Vytvoření konceptu [[osetreni-chyb-a-logovani]] (strategie, úrovně logování).
- Aktualizace [[mapovani-dedicnosti]] (doplnění LSP a skládání).
- Aktualizace [[index]].

## [2026-05-08] - Ingest 7. přednášky (ingest/prednaska-07)
- Zpracování přednášky `07.prednaska.pdf`.
- Vytvoření souhrnné stránky [[07-navrhove-vzory-a-komponenty]].
- Vytvoření konceptu [[komponenty-a-rozhrani]] (fyzické komponenty, nabízená/vyžadovaná rozhraní, diagram komponent).
- Vytvoření konceptu [[dependency-injection]] (IoC, DI typy, Spring scopes).
- Vytvoření konceptu [[navrhove-vzory-gof]] (Abstract Factory, Builder, State, Observer, Adapter).
- Aktualizace [[softwarova-architektura]] a [[navrhovy-model-trid]].
- Aktualizace [[index]].

## [2026-05-08] - Ingest 6. přednášky (ingest/prednaska-06)
- Zpracování přednášky `06.prednaska.pdf`.
- Vytvoření souhrnné stránky [[06-architektonicke-vzory]].
- Vytvoření konceptu [[vrstvy-architektury]] (Monolit, 2-vrstvá, 3-vrstvá, striktní/relaxovaná).
- Vytvoření konceptu [[persistence-dat]] s detaily z doplňkových materiálů (Active Record, Data Mapper, atd.).
- Vytvoření konceptu [[sekvencni-diagram]] (UML notace pro spolupráci objektů).
- Vytvoření konceptu [[mvc-mvp]] (vzory prezentační vrstvy).
- Aktualizace [[index]].

## [2026-05-08] - Oprava vztahů v Use Case (fix: clarify UC relationships)
- Revize [[pripady-uziti]] a [[diagram-pripadu-uziti]] na základě `Use Case Model.pdf`.
- Doplněno varování před funkční dekompozicí a upřesnění významu `include` a `extend`.

## [2026-05-08] - Ingest 5. přednášky (ingest/prednaska-05)
- Zpracování přednášky `05.prednaska.pdf`.
- Vytvoření souhrnné stránky [[05-navrh-softwarovych-systemu]].
- Vytvoření konceptu [[navrh-softwaru]].
- Vytvoření konceptu [[softwarova-architektura]].
- Vytvoření konceptu [[navrhovy-model-trid]] s využitím informací z `GRASP.pdf`.
- Vytvoření konceptu [[mapovani-dedicnosti]] s detailním popisem Single, Concrete a Class Table Inheritance na základě doplňkových materiálů.
- Aktualizace [[diagram-balicku]] o sekci o cyklických závislostech a vnořování.
- Aktualizace [[index]].

## [2026-05-08] - Ingest 4. přednášky (ingest/04-objektova-analyza)
- Zpracování přednášky `04.prednaska.pdf`.
- Vytvoření souhrnné stránky [[04-analyza-problemove-domeny]].
- Vytvoření konceptu [[stavovy-diagram]].
- Výrazné rozšíření konceptu [[domenovy-model]] (notace tříd, vztahy, multiplicity, kompozice, agregace, hledání entit a časté chyby).
- Aktualizace [[index]].

## [2026-05-08] - Specializované koncepty pro diagramy (feat/diagram-concepts)
- Vytvoření samostatných stránek pro notaci a strukturu: [[diagram-pripadu-uziti]], [[diagram-balicku]] a [[domenovy-model]].
- Integrace detailů z `raw/extra/Class Diagram Domain Model.pdf`.
- Refaktoring [[pripady-uziti]] (oddělení notace od techniky).
- Aktualizace [[role-analytika]] a [[index]].

## [2026-05-08] - Ingest 3. přednášky (ingest/03-analyza-pozadavku)
- Zpracování přednášky `03.prednaska.pdf`.
- Vytvoření souhrnné stránky [[03-analyza-a-sber-pozadavku]].
- Vytvoření konceptů [[pozadavky]] (včetně modelu FURPS) a [[uzivatelske-pribehy]].
- Rozšíření a aktualizace [[pripady-uziti]] o doporučení k tvorbě scénářů, granularitu a časté chyby.
- Aktualizace [[index]].

## [2026-05-08] - Refaktoring Use Case (feat/use-case-concept)
- Vytvoření samostatného konceptu [[pripady-uziti]].
- Přesun a rozšíření informací o UC z `role-analytika`.
- Aktualizace [[role-analytika]] a [[index]].

## [2026-05-08] - Ingest 2. přednášky (ingest/02-procesni-modelovani)
- Zpracování přednášky `02.prednaska.pdf`.
- Vytvoření souhrnné stránky [[02-modelovani-obchodnich-procesu]].
- Vytvoření konceptů [[obchodni-procesy]] a [[diagram-aktivit]].
- Integrace detailních informací o UML z `raw/extra/Activity Diagram.pdf`.
- Aktualizace [[role-analytika]] o vazby na procesní modelování.
- Aktualizace [[index]].

## [2026-05-08] - Ingest 1. přednášky (ingest/01-prednaska)
- Zpracování přednášky `01.prednaska.pdf`.
- Vytvoření souhrnné stránky [[01-uvod-do-swi]].
- Vytvoření základních konceptů: [[softwarove-inzenyrstvi]], [[tymova-spoluprace]], [[odhad-pracnosti]], [[role-analytika]].
- Integrace informací o Use Case z `raw/extra/`.
- Inicializace `wiki/index.md` a `wiki/log.md`.