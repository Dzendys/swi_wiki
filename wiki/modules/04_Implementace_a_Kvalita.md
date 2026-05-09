# Implementace a zajištění kvality

**Shrnutí**: Tato sekce se věnuje fázi realizace softwaru, principům psaní kvalitního kódu a systematickému přístupu k zajištění kvality pomocí testování, verifikace a validace.

**Zdroje**:
- `wiki/lectures/08-implementace.md`
- `wiki/lectures/09-zajisteni-kvality.md`

**Naposledy aktualizováno**: 2026-05-18

---

## Implementace

[[implementace|Implementace]] je fáze, která transformuje návrh do spustitelného zdrojového kódu. V moderním softwarovém inženýrství stojí na **[[objektove-paradigma|objektovém paradigmatu]]**, které využívá zapouzdření, dědičnost a polymorfismus k budování komplexních systémů.

### Clean Code (Čistý kód)
Kvalita implementace je přímo úměrná její udržovatelnosti. Dodržování pravidel **[[clean-code|čistého kódu]]** zahrnuje:
- **SRP (Single Responsibility)**: Každá třída či metoda má mít jednu zodpovědnost.
- **DRY (Don't Repeat Yourself)**: Zákaz duplicity kódu.
- **Law of Demeter**: Objekt by měl komunikovat pouze se svými "přímými známými".
- **LSP (Liskov Substitution)**: Podtřída musí být zaměnitelná za svou nadtřídu.

Pro uvolnění vazeb mezi komponentami a snadnější testování se využívá princip **[[dependency-injection|Dependency Injection (DI)]]**, kde jsou závislosti objektům "vstřikovány" zvenčí.

### Robustnost a udržovatelnost
Robustní aplikace musí obsahovat správné **[[osetreni-chyb-a-logovani|ošetření chyb]]** (využití výjimek) a **logování** pro diagnostiku provozu. Průběžné vylepšování vnitřní struktury kódu bez změny jeho chování se nazývá **[[refaktoring|refaktoring]]**. Ten pomáhá odstraňovat "code smells" (duplicity, dlouhé metody) a snižovat technický dluh.

## Zajištění kvality (QA)

[[zajisteni-kvality|Zajištění kvality]] není pouze testování na konci projektu, ale systematický proces prostupující celým cyklem. Kvalitu měříme pomocí externích (korektnost, spolehlivost) a interních (čitelnost, testovatelnost) charakteristik.

![[imgs/09.prednaska-012.jpg|1000]]
*Obrázek: Exponenciální nárůst nákladů na opravu chyby v čase.*

### Verifikace vs. Validace
Procesy kontroly kvality dělíme na:
- **[[verifikace-a-validace|Verifikace]]**: „Stavíme produkt správně?“ (shoda se specifikací a modely).
- **Validace**: „Stavíme správný produkt?“ (shoda s potřebami uživatele).

### Testování softwaru
[[testovani|Testování]] je proces hledání chyb. Rozlišujeme:
- **Dle rozsahu**: Jednotkové (Unit), Integrační a Systémové testy.
- **Dle znalosti kódu**: **White Box** (vidíme kód) a **Black Box** (testujeme přes rozhraní).
- **Techniky**: Analýza hraničních hodnot, třídy ekvivalence, regresní testování (ověření, že změna nerozbila stávající funkce).

Kvalitu testování lze měřit pomocí metrik, jako je **pokrytí kódu (Code Coverage)**.

![[imgs/09.prednaska-041.jpg|939]]
*Obrázek: Vizualizace trendů v úspěšnosti testů v čase.*

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
