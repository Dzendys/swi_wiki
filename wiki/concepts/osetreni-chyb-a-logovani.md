# Ošetření chyb a logování

**Shrnutí**: Mechanismy pro zajištění robustnosti aplikace prostřednictvivím validace vstupů, ošetření výjimečných stavů a sledování běhu programu.

**Zdroje**:
- `raw/lectures/08.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Robustní aplikace musí být připravena na nevalidní vstupy (uživatelé, soubory, externí API) i na chyby způsobené ostatními programátory.

## Ošetření chyb (Error Handling)
Existuje několik strategií, jak se vypořádat s chybovým stavem:
1.  **Vrácení neutrální hodnoty**: Např. prázdný řetězec, `0` nebo `null`. Pozor na "zamaskování chyby", kdy program pokračuje dál v nekonzistentním stavu.
2.  **Vrácení chybového kódu**: Tradiční přístup (např. v C), kde metoda vrací kód označující výsledek operace.
3.  **Vyvolání výjimky (Exception)**: Moderní přístup (Java, C#, Python, TS). Odděluje cestu "šťastného běhu" od cesty ošetření chyb.
4.  **Zobrazení chyby uživateli**: Informování uživatele o problému (pokud na něj může reagovat).
5.  **Ukončení programu**: Krajní řešení pro fatální chyby, které znemožňují bezpečný běh.

## Logování (Logging)
Logování slouží k záznamu důležitých událostí během běhu aplikace pro potřeby diagnostiky a auditu.

### Úrovně logování (Priority)
Běžně se používají tyto úrovně (od nejméně závažné):
-   **DEBUG**: Detailní informace pro vývojáře, v produkci obvykle vypnuté.
-   **INFO**: Obecné informace o běhu (např. "Server spuštěn", "Uživatel přihlášen").
-   **WARN**: Varování o neobvyklých stavech, které aplikaci nezastaví (např. "Doba odezvy externí služby je vysoká").
-   **ERROR**: Chyba, kterou se nepodařilo ošetřit a ovlivnila operaci.
-   **FATAL**: Kritická chyba vedoucí k pádu nebo znefunkčnění aplikace.

### Komponenty logování
-   **Logger**: Třída, kterou programátor používá k zápisu do logu (např. `log.info("...")`).
-   **Appender/Handler**: Komponenta zodpovědná za fyzický zápis zpráv (do souboru, na konzoli, do databáze, zaslání e-mailu).

### Existující řešení
Místo psaní vlastního logování se vždy používají prověřené knihovny:
-   **Java**: Java Logging API, LOG4J, SLF4J.
-   **C#**: NLog, Serilog.

## Související stránky
- [[implementace]]
- [[clean-code]]
- [[refaktoring]]

---
#error-handling #logging #robustness #software-quality #BI-SWI
