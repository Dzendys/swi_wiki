# Verifikace a validace

**Shrnutí**: Dva základní procesy kontroly kvality. Verifikace ověřuje shodu se specifikací, zatímco validace ověřuje shodu se skutečnými potřebami uživatele.

**Zdroje**:

- `raw/lectures/09.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Rozlišení mezi verifikací a validací je klíčové pro správné nastavení [[zajisteni-kvality|QA]] procesů (zdroj: raw/lectures/09.prednaska.pdf).

## Verifikace (Verification)
Odpovídá na otázku: **"Stavíme produkt správně?"** (*Are we building the product right?*)

- **Definice**: Proces hodnocení systému nebo komponenty, aby se zjistilo, zda výsledky dané fáze vývoje splňují podmínky stanovené na jejím začátku.
- **Základ**: Ověření probíhá vůči **modelu, specifikaci nebo dokumentaci**.
- **Příklad**: Jednotkové testy ověřující shodu s návrhem třídy, formální inspekce kódu.

## Validace (Validation)
Odpovídá na otázku: **"Stavíme správný produkt?"** (*Are we building the right product?*)

- **Definice**: Proces hodnocení systému nebo komponenty na konci vývojového procesu, aby se zjistilo, zda splňuje specifické požadavky uživatele.
- **Základ**: Ověření probíhá vůči **reálným výsledkům a očekáváním zákazníka**.
- **Příklad**: Akceptační testování se zákazníkem, beta testování, ověření, zda systém skutečně řeší obchodní problém.

## Rozdíly v kostce
| Charakteristika | Verifikace | Validace |
| :--- | :--- | :--- |
| **Zaměření** | Proces a specifikace | Výsledek a uživatel |
| **Kdy probíhá** | Průběžně během fází | Typicky na konci fází/projektu |
| **Vstupy** | Dokumentace, modely, kód | Provozuschopný software, uživatel |

## Související stránky

- [[zajisteni-kvality]]
- [[testovani]]
- [[pozadavky]]

---
#verification #validation #qa #software-engineering #BI-SWI
