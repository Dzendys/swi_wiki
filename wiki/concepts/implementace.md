# Implementace

**Shrnutí**: Fáze softwarového inženýrství, ve které dochází k realizaci návrhu do spustitelného zdrojového kódu.

**Zdroje**:

- `raw/lectures/08.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Implementace je klíčovým krokem vývojového cyklu, který transformuje [[navrh-softwaru|návrh]] a scénáře [[pripady-uziti|případů užití]] do funkčního produktu. Je to jediná činnost, kterou nelze v projektu vynechat (zdroj: raw/lectures/08.prednaska.pdf).

## Cíle implementace
Hlavním cílem není pouze "napsat kód", ale dodat produkt, který:
1.  **Funguje dle požadavků**: Přesná realizace funkcionality definované v analýze.
2.  **Snadno se používá**: Závisí na cílové skupině a uživatelské úrovni (souvisí s oborem UI/UX, na FIT ČVUT předmět BI-TUR).
3.  **Neobsahuje chyby**: Důraz na stabilitu a korektnost.
4.  **Funguje na cílových prostředích**: Kompatibilita s hardwarem a operačními systémy.
5.  **Snadno se udržuje a rozšiřuje**: Kód musí být čitelný a připravený na budoucí změny.

## Činnosti při implementaci
-   **Přepis scénářů do kódu**: Implementace logiky z [[sekvencni-diagram|sekvenčních diagramů]] nebo jiných modelů chování.
-   **Návrh v malém**: Během psaní kódu je nutné činit mnoho drobných rozhodnutí, která nebyla v dokumentaci (např. výběr datové struktury). Tato rozhodnutí musí být v souladu s [[softwarova-architektura|architekturou]].
-   **Dodržování pravidel**: Aplikace [[clean-code|pravidel čistého kódu]] a konvencí týmu.
-   **Refaktoring**: Průběžné vylepšování struktury kódu (viz [[refaktoring]]).

## Související stránky
- [[navrh-softwaru]]
- [[navrhovy-model-trid]]
- [[objektove-paradigma]]
- [[clean-code]]

---
#swi #implementace #vyvoj #softwarove-inzenyrstvi #BI-SWI
