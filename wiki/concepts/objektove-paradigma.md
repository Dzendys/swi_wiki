# Objektové paradigma

**Shrnutí**: Programovací a návrhové paradigma založené na dekompozici systému na spolupracující objekty, které zapouzdřují data a metody.

**Zdroje**:

- `raw/lectures/08.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Objektově orientované paradigma (OOP) je v současnosti dominantním přístupem k vývoji softwaru. Systém je v něm chápán jako síť **objektů**, které spolu komunikují zasíláním zpráv (voláním metod).

## Základní pojmy

### Třída vs. Objekt

- **Třída**: Šablona (metadata), která definuje strukturu atributů, signatury a implementace metod a konstruktory pro inicializaci (zdroj: raw/lectures/08.prednaska.pdf).
- **Objekt (Instance)**: Konkrétní "výrobek" podle šablony. Každý objekt má své vlastní hodnoty atributů (stav), ale metody jsou společné pro všechny instance dané třídy.

### Zapouzdření (Encapsulation)
Objekt funguje jako "černá skříňka" (black box). Drží svůj vnitřní stav uvnitř sebe a implementační detaily jsou schovány za množinou veřejných metod. Tím se chrání data před nepřípustnou modifikací zvenčí.

### Dědičnost (Inheritance)
Umožňuje vytvořit novou třídu (podtřídu), která přebírá vlastnosti a metody jiné třídy (nadtřídy).

- Atributy a metody nadtřídy jsou vloženy do podtřídy.
- Metody podtřídy mohou **překrýt** (override) metody nadtřídy.
- *Pozor*: Dědičnost by měla být používána obezřetně a splňovat [[clean-code#Liskov Substitution Principle (LSP)|Liskov Substitution Principle]]. Často je vhodnější použít skládání.

### Abstraktní třída
Třída, ze které nelze vytvářet instance. Slouží jako předpis pro podtřídy.

- Může obsahovat abstraktní metody (bez implementace), které musí podtřídy definovat.
- Může obsahovat i implementované metody a atributy.

### Polymorfismus
Schopnost objektů různých tříd reagovat na stejné volání metody různým způsobem. Při volání metody je konkrétní implementace určena skutečným typem objektu, nikoliv typem proměnné, ve které je objekt uložen.

## Sledování stavu
Pro vizualizaci aktuálního stavu systému (instancí a jejich vazeb) v konkrétní časový okamžik se používá **[[objektovy-diagram|objektový diagram]]**.

## Související stránky

- [[navrhovy-model-trid]]
- [[implementace]]
- [[objektovy-diagram]]
- [[clean-code]]

---
#oop #objektove-paradigma #software-engineering #design #BI-SWI
