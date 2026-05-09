# Mapování dědičnosti

**Shrnutí**: Vzory pro reprezentaci objektově orientované dědičnosti (generalizace) v relačních databázích, které samy o sobě dědičnost nepodporují.

**Zdroje**:

- `raw/lectures/05.prednaska.pdf`
- `raw/extra/Single Table Inheritance.pdf`
- `raw/extra/Concrete Table Inheritance.pdf`
- `raw/extra/Class Table Inheritance.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Při ukládání objektů do relační databáze narážíme na tzv. *object-relational impedance mismatch*. Jedním z hlavních problémů je mapování hierarchie dědičnosti. Pro řešení tohoto problému definoval Martin Fowler tři základní návrhové vzory.

## 1. Single Table Inheritance (Jedna tabulka)
Všechny třídy v hierarchii dědičnosti jsou mapovány do jediné široké databázové tabulky. Tabulka obsahuje sloupce pro všechny atributy všech podtříd.
- **Výhody**: Snadná a rychlá implementace, nepotřebuje spojování tabulek (JOIN), rychlé dotazování.
- **Nevýhody**: Tabulka může být velmi rozsáhlá s mnoha `NULL` hodnotami u záznamů, které daný atribut nepoužívají. Může docházet k plýtvání místem (i když moderní DB to často umí optimalizovat). Vyžaduje sloupec rozlišující typ záznamu (discriminator).

## 2. Concrete Table Inheritance (Tabulky konkrétních tříd)
Pro každou *konkrétní* (neabstraktní) třídu v hierarchii se vytvoří samostatná tabulka. Každá tabulka obsahuje sloupce pro atributy dané podtřídy i všechny atributy zděděné od rodičů.
- **Výhody**: Žádné `NULL` hodnoty pro neexistující atributy. Rozdělení zátěže při přístupu k různým typům objektů.
- **Nevýhody**: Duplikace sloupců (struktury) z rodičovské třídy ve všech tabulkách potomků. Pokud se změní struktura rodiče, musí se změnit všechny tabulky. Získání polymorfní kolekce objektů (např. dotaz na nadtřídu) vyžaduje dotazování přes všechny tabulky a složité spojování (UNION). Nelze snadno uložit pouhou instanci rodičovské abstraktní třídy.

## 3. Class Table Inheritance (Tabulky pro každou třídu)
Každá třída v hierarchii (včetně abstraktních rodičů) má svou vlastní tabulku. Tabulka rodiče obsahuje pouze atributy rodiče. Tabulky potomků obsahují pouze specifické atributy potomka a cizí klíč (Foreign Key), který je typicky i primárním klíčem a odkazuje na odpovídající záznam v tabulce rodiče.
- **Výhody**: Čistý normalizovaný databázový návrh bez duplicit struktury a bez plýtvání místem (`NULL` hodnotami). Symetrické zobrazení hierarchie tříd do DB.
- **Nevýhody**: Složité a výkonnostně náročnější získávání dat. Pro načtení jednoho objektu z konce hierarchie je nutné spojit (JOIN) několik tabulek podle hloubky dědičnosti.

## Návrhová doporučení
Při používání dědičnosti je nutné dbát na to, aby byla použita správně i z pohledu softwarového návrhu, nejen databázového uložení. Klíčovým pravidlem je **[[clean-code#Liskov Substitution Principle (LSP)|Liskov Substitution Principle (LSP)]]**. Často se ukazuje, že je vhodnější upřednostnit **skládání (composition)** před dědičností, což se v databázi řeší pomocí asociací (cizích klíčů).

## Související stránky
- [[navrh-softwaru]]
- [[domenovy-model]]
- [[objektove-paradigma]]
- [[clean-code]]

---
#swi #databaze #orm #dedicnost #navrhove-vzory #BI-SWI
