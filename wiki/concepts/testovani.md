# Testování softwaru

**Shrnutí**: Technický proces provádění programu se záměrem najít chyby a změřit kvalitu produktu.

**Zdroje**:
- `raw/lectures/09.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Testování je jednou z klíčových forem [[verifikace-a-validace|validace a verifikace]]. Výsledek testování může prokázat existenci chyb, ale nemůže nikdy prokázat, že software žádné chyby neobsahuje (zdroj: raw/lectures/09.prednaska.pdf).

## Klasifikace testů

### Podle rozsahu
1.  **Jednotkové testy (Unit Tests)**: Testují nejmenší testovatelné části (metody, třídy) izolovaně od zbytku systému.
2.  **Integrační testy**: Ověřují správnou spolupráci mezi více komponentami nebo moduly.
3.  **Systémové testy**: Testují celý systém jako celek vůči specifikovaným požadavkům.

### Podle způsobu provádění
-   **Statické testy**: Nevyžadují spuštění programu (např. code review, inspekce, statická analýza kódu).
-   **Dynamické testy**: Vyžadují spustitelný kód (klasické testy se vstupními a výstupními daty).

### Podle znalosti vnitřní struktury
-   **White Box (skleněná skříňka)**: Tester zná zdrojový kód. Testy jsou citlivé na změnu implementace.
-   **Black Box (černá skříňka)**: Tester kód nevidí, ověřuje pouze chování na rozhraní (vstup vs. výstup).
-   **Gray Box**: Tester má částečnou znalost (např. zná použité algoritmy, ale ne konkrétní kód).

## Techniky a typy testů

### Návrh testovacích případů
-   **Hraniční testování (Boundary Testing)**: Testování hodnot na hranicích intervalů (např. 0, 1, max, max+1), kde je nejvyšší pravděpodobnost výskytu chyby.
-   **Analýza ekvivalence (Equivalence Analysis)**: Rozdělení vstupních dat do tříd ekvivalence, ze kterých se vybere jeden zástupce. Předpokládá se, že pokud projde zástupce, prošli by i ostatní členové třídy.

### Speciální typy testů
-   **Regresní testy**: Opětovné spuštění testů po změně kódu k ověření, že nové funkce "nerozbily" ty stávající. Ideální pro automatizaci.
-   **Smoke testy**: Rychlá sada testů k ověření základní stability aplikace (např. "lze se přihlásit?") po nasazení.

## Testovací artefakty
-   **Testovací plán**: Dokument definující *co, jak, kdo a kdy* bude testovat.
-   **Testovací případ (Test Case)**: Konkrétní postup, vstupní data, očekávaná výstupní data a výsledek.
-   **Test suite**: Kolekce testovacích případů.

## Metriky testování
Sledování metrik v čase umožňuje vyhodnotit stabilitu systému a efektivitu testování.

![|x250](imgs/09.prednaska-041.jpg) ![|x250](imgs/09.prednaska-042.jpg)
*Obrázek: Vizualizace trendů v úspěšnosti testů a procentuálním pokrytí kódu v čase.*

- **Pokrytí kódu (Code Coverage)**: Procento řádků, tříd nebo metod pokrytých testy (typicky u White Box testů).
- **Cyklomatická složitost**: Počet nezávislých cest kódem.

![|x200](imgs/09.prednaska-044.jpg) ![|x250](imgs/09.prednaska-045.jpg)
*Obrázek: Detailní přehled pokrytí (Line vs Condition Coverage) a analýza vztahu mezi složitostí kódu a jeho otestováním.*

- **Počet nalezených chyb** vs. počet chyb nalezených v produkci.

## Vlastnosti dobrého testu
Dobrý test by měl mít vysokou schopnost odhalit chybu (**Power**), být snadno udržovatelný (**Maintainable**), odpovídat chování uživatele (**Credible**), být opakovatelný (**Repeatable**) a mít přidanou hodnotu (**Value**).

## Související stránky
- [[zajisteni-kvality]]
- [[verifikace-a-validace]]
- [[implementace]]
- [[refaktoring]] (vyžaduje existenci testů)

---
#testing #qa #unit-tests #regression #black-box #white-box #BI-SWI
