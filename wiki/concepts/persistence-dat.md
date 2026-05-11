# Persistence dat

**Shrnutí**: Způsoby a vzory pro trvalé ukládání objektů z operační paměti do datového úložiště (typicky relační databáze).

**Zdroje**:

- `raw/lectures/05.prednaska.pdf`
- `raw/lectures/06.prednaska.pdf`
- `raw/extra/Table Data Gateway.pdf`
- `raw/extra/Row Data Gateway.pdf`
- `raw/extra/Active Record.pdf`
- `raw/extra/Data Mapper.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Persistence dat v [[vrstvy-architektury|třívrstvé architektuře]] spadá do nejnižší (datové) vrstvy. Existuje několik osvědčených vzorů (dle Martina Fowlera) pro mapování objektů na databázové tabulky.

## Návrh datového schématu
V návrhové fázi vytváříme detailní UML datový model, který specifikuje datové typy, primární a cizí klíče a unikátní indexy.

- **Trasovatelnost (Traceability)**: Sledujeme vztah mezi konceptuálním modelem (např. Autor, Kniha) a jeho fyzickou realizací v databázi. To zahrnuje i zavedení asociačních tabulek (např. `jeNapsana`) pro řešení vztahů M:N.

    ![[imgs/05.prednaska-027.jpg|500]]

- **Detailní mapování entit**: Návrh tabulek (např. `Ctenar`, `Vypujcka`, `Vytisk`) s definicí všech atributů, datových typů (VARCHAR, NUMERIC) a integritních omezení.

    ![[imgs/05.prednaska-023.jpg|150]] ![[imgs/05.prednaska-032.jpg|500]]


## Table Data Gateway (TDG)
Jedna instance této třídy spravuje všechny řádky v jedné tabulce.

- **Princip**: Zapouzdřuje všechny SQL dotazy pro danou tabulku (SELECT, INSERT, UPDATE, DELETE).
- **Použití**: Vhodné tam, kde doménová logika není složitá a stačí pracovat s RecordSety (zdroj: raw/extra/Table Data Gateway.pdf).

    ![[imgs/06.prednaska-033.jpg|400]]

    *Obrázek: Třída `Kniha Gateway` zapouzdřující CRUD operace (`najdi`, `vytvoř`, `uprav`, `smaz`) nad celou tabulkou.*


## Row Data Gateway (RDG)
Jeden objekt této třídy reprezentuje právě jeden řádek v databázi.

- **Princip**: Objekt obsahuje atributy odpovídající sloupcům tabulky. Pro vyhledávání se používá samostatná třída (Finder).
- **Varianty**:
    - **S vyhledávačem**: Čisté řešení, kde vyhledávání (`najdiPodleISBN`) řeší externí třída `Vyhledávač knih`.
    - **Se statickými metodami**: Méně vhodné pro testování, vyhledávací metody jsou přímo v doménové třídě.

    ![[imgs/06.prednaska-035.jpg|400]] ![[imgs/06.prednaska-037.jpg|250]]

    *Obrázek: Vlevo standardní RDG s Finderem, vpravo varianta se statickými metodami v doménové třídě.*


## Active Record
Velmi oblíbený vzor, který vychází z Row Data Gateway, ale přidává k objektu **business logiku**.

- **Princip**: Datový objekt ví, jak se uložit (`insert`, `update`), a zároveň obsahuje doménová pravidla (např. `zjistiPopularitu`).
- **Nevýhoda**: Porušuje zásady čisté třívrstvé architektury (silná vazba business logiky na databázi).

    ![[imgs/06.prednaska-039.jpg|400]]

    *Obrázek: Třída `Kniha` integrující data, persistenci i specifickou business logiku.*


## Data Mapper
Vrstva mapperů, která přenáší data mezi objekty a databází a přitom je udržuje navzájem nezávislé.

- **Princip**: Doménové objekty vůbec netuší, že existuje nějaká databáze. Mapování zajišťuje externí třída Mapper.
- **Výhody**: Maximální rozvolnění vazeb (decoupling). Umožňuje mapovat složité hierarchie (dědičnost) a kolekce.

    ![[imgs/06.prednaska-041.jpg|450]]

    *Obrázek: Třída `Kniha Mapper` zajišťující transparentní přenos dat mezi business objektem a databází.*


## Související stránky

- [[mapovani-dedicnosti]]
- [[vrstvy-architektury]]
- [[navrh-softwaru]]

---
#swi #persistence #databaze #orm #fowler #design-patterns #BI-SWI
