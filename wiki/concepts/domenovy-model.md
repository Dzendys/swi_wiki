# Doménový model

**Shrnutí**: Abstraktní model popisující klíčové entity problémové domény, jejich vlastnosti (atributy) a vzájemné vztahy. Slouží k pochopení datové struktury z pohledu business logiky a jako základ pro design.

**Zdroje**:
- `raw/lectures/01.prednaska.pdf`
- `raw/lectures/04.prednaska.pdf`
- `raw/extra/Class Diagram Domain Model.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

**Doménový model** (Domain Model) je klíčovým výstupem analytika, který odpovídá na otázku, s jakými daty a entitami systém pracuje (zdroj: raw/lectures/01.prednaska.pdf). K jeho tvorbě se využívá **UML Diagram tříd** (Class Diagram) na vysoké úrovni abstrakce (zdroj: raw/extra/Class Diagram Domain Model.pdf).

## Účel a charakteristika
- **Slovníček pojmů**: Sjednocení terminologie mezi zákazníkem a vývojáři.
- **Abstrakce**: Neobsahuje implementační detaily (metody, cizí klíče).
- **Zasazení**: Entity reprezentují reálné objekty problémové domény (zdroj: raw/lectures/04.prednaska.pdf).

## Prvky modelu
### Třída (Entity)
- **Atributy**: Vlastnosti entity (název:typ). Používají se pouze základní typy (int, text, date) (zdroj: raw/lectures/04.prednaska.pdf).
- **Metody**: V doménovém modelu se typicky nepoužívají, ledaže popisují doménovou logiku (nikoliv implementaci jako `print()` nebo `backup()`) (zdroj: raw/lectures/04.prednaska.pdf).
- **Viditelnost**: private (`-`), protected (`#`), public (`+`).

### Vztahy
- **Asociace**: Propojení mezi entitami s definovanou **násobností** (např. `0..*`, `1..1`). Násobnost je nutné kontrolovat v obou směrech (zdroj: raw/lectures/04.prednaska.pdf).
- **Kompozice**: Silná vazba typu "celek-část", kde část nemůže existovat bez celku.
- **Agregace**: Slabší vazba "celek-část". Doporučuje se spíše nepoužívat a nahradit asociací (zdroj: raw/lectures/04.prednaska.pdf).
- **Generalizace (Dědičnost)**: Modelování hierarchie entit (potomek dědí od rodiče).

## Hledání entit
Entity se hledají jako podstatná jména v:
- Business procesních modelech.
- [[pripady-uziti|Modelech případů užití]].
- Slovníčku pojmů (zdroj: raw/lectures/04.prednaska.pdf).

## Časté chyby
- **Implementační detaily**: Zahrnutí atributů typu `rowid` nebo metod pro údržbu databáze.
- **Cizí klíče**: Snaha identifikovat objekt pomocí atributu (např. `cisloFaktury` v třídě `Kniha`) místo použití asociace (zdroj: raw/lectures/04.prednaska.pdf).
- **Nevhodná dědičnost**: Použití generalizace pro kategorie, které se mohou překrývat nebo měnit (vhodnější je vazba na entitu `Typ` nebo `Žánr`).
- **Pletení instance a popisu**: Třída by neměla obsahovat atributy instance (evidenční číslo) i obecného popisu (název, autor) dohromady, pokud může existovat více instancí jednoho popisu (zdroj: raw/lectures/04.prednaska.pdf).

## Související stránky
- [[role-analytika]]
- [[obchodni-procesy]]
- [[stavovy-diagram]]

---
#analyza #data #uml #class-diagram #modelovani #BI-SWI
