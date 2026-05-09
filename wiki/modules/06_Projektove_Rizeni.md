# Projektové řízení

**Shrnutí**: Tato sekce se věnuje disciplíně řízení softwarových projektů, plánování zdrojů a času, odhadování pracnosti a systematickému řízení rizik.

**Zdroje**:
- `wiki/lectures/11-projektove-rizeni.md`

**Naposledy aktualizováno**: 2026-05-18

---

## Základy projektového řízení

[[projektove-rizeni|Projektové řízení]] zajišťuje dodání softwarového produktu včas, v požadované kvalitě a v rámci stanoveného rozpočtu.

**Projektový trojúhelník (Trojimperativ)**:
Projektový manažer musí neustále vyvažovat tři základní omezení:
1. **Čas (Harmonogram)**: Kdy má být projekt hotov.
2. **Cena (Rozpočet/Zdroje)**: Kolik to bude stát.
3. **Rozsah (Scope)**: Co všechno se má udělat.
Změna jednoho parametru nutně ovlivní ostatní. Uprostřed trojúhelníku leží **Kvalita**, kterou nelze obětovat.

### Fáze projektu
Klasický projekt prochází fázemi:
- **Příprava (Initiation/Planning)**: Vytvoření Business Case, hrubý odhad, sestavení plánu.
- **Provádění (Execution/Monitoring)**: Samotný vývoj. Sledování postupu a nákladů (v čerpání MDs).
- **Uzavření (Closing)**: Předání díla, formální akceptace zákazníkem a vyhodnocení projektu (Lesson Learned).

## Plánování a odhady pracnosti

Schopnost udělat spolehlivý [[odhad-pracnosti|odhad pracnosti]] je klíčová. Vyjadřuje se v člověkohodinách (MH) nebo člověkodnech (MD).

**Nástroje pro plánování**:
- **WBS (Work Breakdown Structure)**: Hierarchický rozklad cíle projektu na menší, měřitelné dodávky a úkoly.
- **Ganttův diagram**: Časová osa úkolů. Zobrazuje závislosti mezi úkoly a identifikuje **Kritickou cestu** (sekvenci úkolů, jejichž zpoždění zpozdí celý projekt).

![[imgs/11.prednaska-032.jpg|643]]

**Metody odhadování**:
- **Expertní odhad**: Založeno na zkušenosti seniorů.
- **Historická data**: Porovnání s podobnými projekty z minulosti.
- **Use Case Points (Karnerova metoda)**: Algoritmický výpočet na základě počtu případů užití a aktérů.

## Řízení rizik

[[rizeni-rizik|Řízení rizik]] je systematický a preventivní proces. Riziko je událost, která, pokud nastane, bude mít negativní vliv na projekt.

**Vyhodnocení rizika**:
Každé riziko se hodnotí z hlediska:
1. **Pravděpodobnosti výskytu**.
2. **Dopadu (Impaktu)** na projekt (zpoždění, finanční ztráta).

**Strategie řešení (Mitigace)**:
- **Akceptace**: Riziko je příliš malé nebo by obrana stála více než případná škoda. Pouze se monitoruje.
- **Minimalizace**: Provedení kroků ke snížení pravděpodobnosti nebo dopadu.
- **Odstranění (Vyhnutí se)**: Změna plánu tak, aby riziko vůbec nevzniklo (např. volba jiné technologie).
- **Přenesení**: Přenesení následků na někoho jiného (např. pojištění, subdodávka).

## Týmová spolupráce

V softwarovém inženýrství je [[tymova-spoluprace|týmová spolupráce]] nezbytností. Tým sdílí odpovědnost za výsledek.
Klíčové je rozdělení rolí (Analytik, Architekt, Vývojář, Tester) a transparentní komunikace (nástroje pro evidenci úkolů, stand-upy, revize kódu).

## Související stránky

- [[projektove-rizeni]]
- [[odhad-pracnosti]]
- [[rizeni-rizik]]
- [[tymova-spoluprace]]
- [[softwarove-inzenyrstvi]]

---
#management #projekt #rizika #planovani #tym #BI-SWI