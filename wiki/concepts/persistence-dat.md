# Persistence dat

**Shrnutí**: Způsoby a vzory pro trvalé ukládání objektů z operační paměti do datového úložiště (typicky relační databáze).

**Zdroje**:
- `raw/lectures/06.prednaska.pdf`
- `raw/extra/Table Data Gateway.pdf`
- `raw/extra/Row Data Gateway.pdf`
- `raw/extra/Active Record.pdf`
- `raw/extra/Data Mapper.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Persistence dat v [[vrstvy-architektury|třívrstvé architektuře]] spadá do nejnižší (datové) vrstvy. Existuje několik osvědčených vzorů (dle Martina Fowlera) pro mapování objektů na databázové tabulky.

## Table Data Gateway (TDG)
Jedna instance této třídy spravuje všechny řádky v jedné tabulce.
- **Princip**: Zapouzdřuje všechny SQL dotazy pro danou tabulku (SELECT, INSERT, UPDATE, DELETE).
- **Použití**: Vhodné tam, kde doménová logika není složitá a stačí pracovat s RecordSety (zdroj: raw/extra/Table Data Gateway.pdf).

## Row Data Gateway (RDG)
Jeden objekt této třídy reprezentuje právě jeden řádek v databázi.
- **Princip**: Objekt obsahuje atributy odpovídající sloupcům tabulky a metody pro manipulaci s daným řádkem (`insert()`, `update()`, `delete()`). Pro vyhledávání instancí se obvykle používá samostatná třída (Finder).
- **Použití**: Odděluje datový přístup od business logiky (zdroj: raw/extra/Row Data Gateway.pdf).

## Active Record
Velmi oblíbený vzor, který vychází z Row Data Gateway, ale přidává k objektu **business logiku**.
- **Princip**: Datový objekt ví, jak se uložit, a zároveň obsahuje doménová pravidla a validace.
- **Nevýhoda**: Porušuje zásady čisté třívrstvé architektury (silná vazba business logiky na databázi).
- **Použití**: Často v PHP (Eloquent), Ruby on Rails (zdroj: raw/extra/Active Record.pdf).

## Data Mapper
Vrstva mapperů, která přenáší data mezi objekty a databází a přitom je udržuje navzájem nezávislé.
- **Princip**: Doménové objekty vůbec netuší, že existuje nějaká databáze. Mapování je definováno externě (anotace, XML).
- **Výhody**: Maximální decoupling (rozvolnění vazeb). Umožňuje mapovat složité hierarchie a kolekce.
- **Použití**: Základ moderních ORM frameworků jako Hibernate (Java), Entity Framework (.NET) nebo Doctrine (PHP) (zdroj: raw/extra/Data Mapper.pdf).

## Související stránky
- [[mapovani-dedicnosti]]
- [[vrstvy-architektury]]
- [[navrh-softwaru]]

---
#swi #persistence #databaze #orm #fowler #design-patterns #BI-SWI
