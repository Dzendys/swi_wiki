# 05. Návrh softwarových systémů

**Shrnutí**: Pátá přednáška pokrývá přechod od analýzy k návrhu, volbu technologií, mapování objektů do relační databáze a architektonický i třídní návrh systému.

**Zdroje**:

- `raw/lectures/05.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Přednáška definuje fázi návrhu (Design) jako proces hledání technické odpovědi na otázku "Jak?" bude systém realizován na základě analytických požadavků.

## Klíčová témata

### Od analýzy k návrhu
Přechod k návrhu znamená posun od popisu problémů k jejich řešení. Zahrnuje výběr programovacího jazyka a paradigmatu (v SWI dominantně objektově orientovaného) a definici celkového způsobu [[navrh-softwaru|návrhu softwaru]]. Analytika v této fázi střídá Solution Architekt.

### Návrh uložení dat
Klíčovým úkolem je návrh [[persistence-dat|persistence]]. Většina systémů využívá relační databáze, což vyžaduje vyřešení rozporu mezi objektovým světem a tabulkami (O/R mapping). Přednáška detailně představuje vzory pro **[[mapovani-dedicnosti|mapování dědičnosti]]** (Single, Concrete a Class Table Inheritance).

### Návrh architektury
[[softwarova-architektura|Softwarová architektura]] se zaměřuje na rozdělení systému do logických celků a izolaci částí, kde lze očekávat změny. Cílem je srozumitelnost a snadná údržba, čehož se dosahuje pomocí zapouzdření a jasně definovaných rozhraní.

### Návrhový model tříd
Na rozdíl od doménového modelu je [[navrhovy-model-trid|návrhový model tříd]] detailní a slouží jako podklad pro kódování. Obsahuje konkrétní datové typy, viditelnost a metody, do kterých jsou přiřazovány zodpovědnosti na základě principů **GRASP** (např. Informační expert).

## Související stránky
- [[navrh-softwaru]]
- [[softwarova-architektura]]
- [[mapovani-dedicnosti]]
- [[navrhovy-model-trid]]
- [[diagram-balicku]]

---
#swi #prednaska #navrh #architektura #BI-SWI
