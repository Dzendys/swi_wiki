# Úvod do softwarového inženýrství a životní cyklus

**Shrnutí**: Přehled disciplíny softwarového inženýrství, modelů životního cyklu (SDLC) a konkrétních metodik od klasického Unified Process po agilní SCRUM.

**Zdroje**:
- `wiki/lectures/01-uvod-do-swi.md`
- `wiki/lectures/12-metodiky-a-agilni-vyvoj.md`

**Naposledy aktualizováno**: 2026-05-18

---

## Softwarové inženýrství (SWI)

[[softwarove-inzenyrstvi|Softwarové inženýrství]] je systematický, disciplinovaný a kvantifikovatelný přístup k vývoji, provozu a údržbě softwaru. Na rozdíl od pouhého programování řeší:
- **Rozsah**: Vývoj rozsáhlých systémů, které jednotlivec nepojme.
- **Kvalitu**: Spolehlivost, udržovatelnost a bezpečnost.
- **Ekonomiku**: Dodržení rozpočtu a termínů.

V týmovém prostředí je klíčová [[tymova-spoluprace|spolupráce]] a [[odhad-pracnosti|odhadování pracnosti]] (v člověkohodinách MH či člověkodnech MD). Důležitým pravidlem je, že přidání lidí do rozjetého projektu jej obvykle ještě více zpozdí kvůli režii na komunikaci.

## Životní cyklus vývoje softwaru (SDLC)

Způsob organizace vývojových činností definuje model životního cyklu. Volba modelu ovlivňuje, jakým způsobem se sbírají požadavky a jak se dodává výsledný produkt.

| Model | Charakteristika | Vhodnost |
| :--- | :--- | :--- |
| **Vodopád** | Lineární, sekvenční fáze. Změny jsou drahé. | Stabilní požadavky, kritické systémy. |
| **Iterativní** | Opakované cykly (iterace), postupné upřesňování. | Většina moderních projektů. |
| **Inkrementální** | Postupné přidávání funkčních celků. | Potřeba brzkého nasazení části systému. |
| **Agilní** | Extrémně krátké cykly, důraz na změnu a lidi. | Nejisté požadavky, dynamické prostředí. |

## Unified Process (UP)

[[unified-process|Unified Process (UP)]] je iterativní framework založený na UML. Stojí na třech pilířích:
1. **Řízený případy užití**: Funkcionalita je definována z pohledu uživatele ([[pripady-uziti|Use Cases]]).
2. **Zaměřený na architekturu**: Nejdříve se stabilizuje kostra systému ([[softwarova-architektura|architektura]]).
3. **Iterativní a inkrementální**: Rizika se řeší včasným prototypováním.

### Fáze UP
- **Inception (Zahájení)**: Definice vize, rozsahu a ekonomické proveditelnosti.
- **Elaboration (Rozpracování)**: Detailní analýza požadavků a stabilizace architektury (spustitelný prototyp).
- **Construction (Konstrukce)**: Masivní vývoj a testování všech zbývajících funkcí.
- **Transition (Dodání)**: Nasazení u zákazníka, beta testování a školení uživatelů.

![[imgs/12.prednaska-029.jpg|622]]

## Agilní vývoj a SCRUM

[[agilni-vyvoj|Agilní přístup]] se řídí Agilním manifestu, který definuje 4 základní hodnoty:
1. **Jednotlivci a interakce** nad procesy a nástroje.
2. **Fungující software** nad vyčerpávající dokumentaci.
3. **Spolupráce se zákazníkem** nad vyjednávání o smlouvách.
4. **Reagování na změnu** nad dodržování plánu.

### SCRUM Framework
Nejrozšířenější agilní metodika. Práce probíhá ve fixních cyklech – **sprinty** (typicky 2–4 týdny).

**Role**:
- **Product Owner (PO)**: Definuje vizi, spravuje priority (Product Backlog), maximalizuje hodnotu.
- **Scrum Master (SM)**: Pomáhá týmu chápat Scrum, odstraňuje překážky, facilituje.
- **Developers (Tým)**: Samo-organizující se skupina, která dodává inkrement (analýza, kód, test).

**Artefakty**:
- **Product Backlog**: Seznam všeho, co by mohlo být v produktu (seřazen dle priorit).
- **Sprint Backlog**: Výběr položek z PB pro aktuální sprint + plán jejich realizace.
- **Inkrement**: Hotová, otestovaná a potenciálně nasaditelná část produktu.

![[imgs/12.prednaska-047.jpg|593]]

## Související stránky

- [[softwarove-inzenyrstvi]]
- [[metodiky-vyvoje]]
- [[agilni-vyvoj]]
- [[scrum]]
- [[unified-process]]
- [[role-analytika]]
- [[odhad-pracnosti]]

---
#swi #metodiky #sdlc #agile #scrum #unified-process #BI-SWI
