# 09. Zajištění kvality

**Shrnutí**: Tato přednáška definuje pojmy Quality Assurance (QA), verifikace a validace, a detailně se věnuje klasifikaci a technikám testování softwaru.

**Zdroje**:
- `raw/lectures/09.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Zajištění kvality není jen o hledání chyb, ale o systematickém přístupu k celému procesu vývoje, který vede k dodání kvalitního produktu při optimalizaci nákladů.

## Klíčová témata

### [[zajisteni-kvality|Zajištění kvality (QA)]]
- **Cíle**: Kvalitní řešení, měřitelnost kvality a úspora financí (oprava chyby v produkci je až 100x dražší než v návrhu).
- **Aktivity**: Plánování procesů, měření, vyhodnocování a řízení.
- **Vlastnosti kvality**: Rozdělení na externí (pro uživatele - korektnost, použitelnost) a interní (pro vývoj - udržovatelnost, čitelnost).

### [[verifikace-a-validace|Verifikace vs. Validace]]
- **Verifikace**: Ověření na základě modelu/specifikace ("Stavíme produkt správně?").
- **Validace**: Ověření na základě reálných výsledků a očekávání uživatele ("Stavíme správný produkt?").

### [[testovani|Testování softwaru]]
- **Klasifikace testů**:
    - Dle rozsahu: [[testovani#Jednotkové testy|jednotkové]], [[testovani#Integrační testy|integrační]], [[testovani#Systémové testy|systémové]].
    - Dle znalosti vnitřku: **White Box** (znalost kódu), **Black Box** (testování rozhraní), **Gray Box**.
    - Dle způsobu: **Statické** (inspekce, review) vs. **Dynamické** (spouštění kódu).
- **Techniky**: [[testovani#Hraniční testování|Hraniční testování (Boundary Testing)]], [[testovani#Analýza ekvivalence|analýza ekvivalence]], [[testovani#Regresní testy|regresní]] a [[testovani#Smoke testy|smoke testy]].
- **Metriky**: Pokrytí kódu (code coverage), cyklomatická složitost, počet nalezených chyb.

## Související stránky
- [[pozadavky]] (Model FURPS)
- [[implementace]]
- [[clean-code]]

---
#prednaska #qa #testing #kvalita #verifikace #validace #BI-SWI
