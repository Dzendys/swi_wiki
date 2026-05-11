# Implementace a zajištění kvality

**Shrnutí**: Tato sekce se věnuje fázi realizace softwaru, principům psaní kvalitního kódu a systematickému přístupu k zajištění kvality pomocí testování, verifikace a validace.

**Zdroje**:

- `wiki/lectures/08-implementace.md`

- `wiki/lectures/09-zajisteni-kvality.md`

**Naposledy aktualizováno**: 2026-05-18

---

## Implementace a Clean Code

[[implementace|Implementace]] převádí návrh do spustitelného kódu, primárně s využitím [[objektove-paradigma|objektového paradigmatu]] (zapouzdření, dědičnost, polymorfismus).

Klíčovým aspektem je udržovatelnost. Pravidla **[[clean-code|čistého kódu]]** zahrnují:

- **Čitelnost**: Kód se čte mnohem častěji, než píše. Názvy proměnných a metod musí vyjadřovat záměr (tzv. "Intention-Revealing Names").

- **SRP (Single Responsibility Principle)**: Třída/metoda by měla mít právě jeden důvod ke změně.

- **DRY (Don't Repeat Yourself)**: Eliminace duplicitního kódu.

- **LSP (Liskov Substitution Principle)**: Objekt nadtřídy by měl být vždy nahraditelný objektem podtřídy bez narušení funkčnosti.

## Refaktoring a Robustnost

Kód časem degraduje (vzniká tzv. technický dluh). Pravidelný **[[refaktoring|refaktoring]]** znamená úpravu vnitřní struktury kódu **bez změny jeho vnějšího chování**, aby se zlepšila jeho srozumitelnost a zlevnila údržba.

Aplikace musí být **robustní** proti chybám:

- Měla by správně reagovat na nestandardní stavy pomocí **[[osetreni-chyb-a-logovani|výjimek (Exceptions)]]**.

- Měla by využívat logování pro snadnější diagnostiku problémů v produkci.

## Zajištění kvality (QA)

[[zajisteni-kvality|Zajištění kvality (Quality Assurance)]] je systematický proces. Čím později je chyba v životním cyklu objevena, tím dražší je její oprava (exponenciální nárůst nákladů).

![[imgs/09.prednaska-012.jpg|1000]]

Základní rozdělení kontroly kvality:

- **[[verifikace-a-validace|Verifikace]]**: „Stavíme produkt správně?“ (Zda kód odpovídá specifikaci a návrhu).

- **[[verifikace-a-validace|Validace]]**: „Stavíme správný produkt?“ (Zda produkt řeší skutečný problém zákazníka).

## Testování softwaru

[[testovani|Testování]] je proces spouštění programu s cílem **najít chyby**. Úspěšný test je ten, který najde chybu.

### Úrovně testování:

1. **Jednotkové (Unit) testy**: Testují izolované části kódu (třídy/metody). Rychlé, levné, píší je vývojáři. K izolaci od závislostí (např. databáze) se používají Mocks/Stubs ve spojení s [[dependency-injection|Dependency Injection]].

2. **Integrační testy**: Testují spolupráci více komponent.

3. **Systémové testy**: Testují celou aplikaci (často přes uživatelské rozhraní).

### Metriky a principy kvality:

- **Code Coverage (Pokrytí kódu)**: Obecná metrika vyjadřující procento kódu pokrytého testy. I když se nejčastěji měří u White Box testů, slouží jako celkový indikátor kvality otestování systému.
- **Programování proti rozhraní**: Klíčový princip pro testovatelnost a rozšiřitelnost. Umožňuje Black Box testování proti kontraktu a snadné mockování závislostí v Unit testech.

### Přístupy k testování:

- **White Box**: Tester vidí do kódu a navrhuje testy na základě vnitřní struktury (např. průchod všemi větvemi kódu).
- **Black Box**: Tester nezná vnitřní implementaci. Testuje se chování navenek (vstup vs. výstup) pomocí hraničních hodnot a tříd ekvivalence.

- **Regresní testování**: Zajišťuje, že nová změna (nebo refaktoring) nerozbila již existující a fungující části systému.

![[imgs/09.prednaska-041.jpg|939]]

## Související stránky

- [[implementace]]

- [[clean-code]]

- [[refaktoring]]

- [[osetreni-chyb-a-logovani]]

- [[zajisteni-kvality]]

- [[testovani]]

- [[verifikace-a-validace]]

- [[dependency-injection]]

- [[objektove-paradigma]]

---
#implementace #qa #cleancode #testovani #refaktoring #kvalita #BI-SWI