# Úvod do softwarového inženýrství a životní cyklus

**Shrnutí**: Přehled disciplíny softwarového inženýrství, modelů životního cyklu (SDLC) a konkrétních metodik od klasického Unified Process po agilní SCRUM.

**Zdroje**:

- `wiki/lectures/01-uvod-do-swi.md`
- `wiki/lectures/12-metodiky-a-agilni-vyvoj.md`

**Naposledy aktualizováno**: 2026-05-18

---

## Softwarové inženýrství (SWI)

[[softwarove-inzenyrstvi|Softwarové inženýrství]] představuje systematický a kontrolovaný přístup k vývoji, který přesahuje pouhé programování. Zaměřuje se na vývoj rozsáhlých softwarových systémů na zakázku, přičemž klade důraz na efektivitu, kvalitu a celý životní cyklus produktu od analýzy potřeb až po nasazení a údržbu.

V profesionálním prostředí nese zodpovědnost za výsledek celý tým. [[tymova-spoluprace|Týmová spolupráce]] vyžaduje pravidelnou komunikaci a transparentní vykazování práce. Klíčovou dovedností je také [[odhad-pracnosti|odhad pracnosti]] (v člověkohodinách MH či člověkodnech MD), přičemž je nutné pamatovat na to, že čas projektu nelze zkrátit pouhým přidáním lidí kvůli rostoucí režii na komunikaci.

## Životní cyklus vývoje softwaru (SDLC)

Způsob, jakým jsou jednotlivé kroky vývoje uspořádány, definuje model životního cyklu. Mezi základní modely patří:

- **Vodopád (Waterfall)**: Lineární sekvence fází (analýza → návrh → implementace → testování). Každá fáze musí být hotová před začátkem další. Je vhodný pro projekty s fixními požadavky.
- **Iterativní model**: Projekt je rozdělen do menších celků (iterací), které fungují jako "malé vodopády". Umožňuje průběžné dodávky a rychlou zpětnou vazbu.
- **Agilní přístup**: Extrémně krátké iterace (týdny) s důrazem na spolupráci, fungující software a schopnost reagovat na změnu.

Standardní [[metodiky-vyvoje|metodiky]] pak tyto modely konkrétně realizují.

## Unified Process (UP)

[[unified-process|Unified Process (UP)]] je představitelem klasické, ale iterativní metodiky. Je řízený [[pripady-uziti|případy užití]], zaměřený na [[softwarova-architektura|architekturu]] a využívá notaci UML. Projekt v UP prochází čtyřmi fázemi:

1. **Inception (Zahájení)**: Definice rozsahu a proveditelnosti.
2. **Elaboration (Rozpracování)**: Detailní analýza a stabilizace architektury.
3. **Construction (Konstrukce)**: Implementace a testování produktu.
4. **Transition (Dodání)**: Nasazení u zákazníka a školení.

![[imgs/12.prednaska-029.jpg|622]]
*Obrázek: Vizualizace fází a intenzity jednotlivých disciplín v rámci metodiky UP.*

## Agilní vývoj a SCRUM

[[agilni-vyvoj|Agilní vývoj]] stojí na Agilním manifestu, který upřednostňuje jednotlivce a interakce před procesy, a fungující software před dokumentací. Nejrozšířenějším agilním frameworkem je **[[scrum|SCRUM]]**.

SCRUM definuje specifické role:
- **Product Owner**: Zástupce zákazníka, spravuje priority v Product Backlogu.
- **Scrum Master**: Ochraňuje proces a odstraňuje překážky.
- **Developers**: Tým realizující inkrementy softwaru.

Práce probíhá ve fixních cyklech zvaných **sprinty** (1 týden až 1 měsíc). Každý den probíhá krátký **Daily Scrum** pro synchronizaci týmu.

![[imgs/12.prednaska-047.jpg|593]]
*Obrázek: Vizualizace základního cyklu metodiky Scrum.*

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
