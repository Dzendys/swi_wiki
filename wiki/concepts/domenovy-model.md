# Doménový model

**Shrnutí**: Abstraktní model popisující klíčové entity problémové domény, jejich vlastnosti (atributy) a vzájemné vztahy. Slouží k pochopení datové struktury z pohledu business logiky a jako základ pro design.

**Zdroje**:

- `raw/lectures/01.prednaska.pdf`
- `raw/lectures/04.prednaska.pdf`
- `raw/extra/Class Diagram Domain Model.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

**Doménový model** (Domain Model) je klíčovým výstupem analytika, který odpovídá na otázku, s jakými daty a entitami systém pracuje (zdroj: raw/lectures/01.prednaska.pdf). K jeho tvorbě se využívá **UML Diagram tříd** (Class Diagram) na vysoké úrovni abstrakce (zdroj: raw/extra/Class Diagram Domain Model.pdf).

![[imgs/04.prednaska-032.jpg|520]]

*Obrázek: Celkový pohled na analytický model knihovny zahrnující klíčové entity a jejich vazby.*

## Účel a charakteristika

- **Slovníček pojmů**: Sjednocení terminologie mezi zákazníkem a vývojáři.
- **Abstrakce**: Neobsahuje implementační detaily (metody, cizí klíče).
- **Zasazení**: Entity reprezentují reálné objekty problémové domény (zdroj: raw/lectures/04.prednaska.pdf).

## Prvky modelu
### Třída (Entity)

- **Atributy**: Vlastnosti entity (název:typ). Používají se pouze základní typy (int, text, date) (zdroj: raw/lectures/04.prednaska.pdf).
- **Metody**: V doménovém modelu se typicky nepoužívají, ledaže popisují doménovou logiku (nikoliv implementaci jako `print()` nebo `backup()`) (zdroj: raw/lectures/04.prednaska.pdf).

![[imgs/04.prednaska-010.jpg|516]]

*Obrázek: Detailní notace třídy v UML (název, atributy s viditelností, metody).*

### Vztahy

- **Asociace**: Propojení mezi entitami s definovanou **násobností** (např. `0..*`, `1..1`). Násobnost je nutné kontrolovat v obou směrech (zdroj: raw/lectures/04.prednaska.pdf).
- **Kompozice**: Silná vazba typu "celek-část", kde část nemůže existovat bez celku.
- **Agregace**: Slabší vazba "celek-část". Doporučuje se spíše nepoužívat a nahradit asociací (zdroj: raw/lectures/04.prednaska.pdf).
- **Generalizace (Dědičnost)**: Modelování hierarchie entit (potomek dědí od rodiče).

![[imgs/04.prednaska-012.jpg|214]]

*Obrázek: Přehled základních typů vazeb mezi třídami.*

#### Speciální vazby

- **Asociační třída**: Používá se pro zachycení informací, které patří k samotné vazbě mezi dvěma třídami.
- **Atribut vs. Asociace**: Pro doménový model je názornější modelovat komplexní vlastnosti jako samostatné třídy spojené asociací.

![[imgs/04.prednaska-016.jpg|646]] ![[imgs/04.prednaska-014.jpg|768]]

*Obrázek: Znázornění asociační třídy a porovnání modelování pomocí atributu vs. asociace.*

## Postup tvorby a refaktoring
Při tvorbě doménového modelu postupně zpřesňujeme strukturu entit tak, aby co nejlépe odpovídala realitě.

1.  **Vyčlenění entit**: Místo atributů (např. jméno autora v třídě Kniha) vytváříme samostatné entity (Autor).
2.  **Modelování historie**: Místo přímé vazby (např. Čtenář "má půjčeno" Knihu) zavádíme vazební entity (Výpůjčka), které umožňují sledovat historii a doplňkové údaje (datum od-do).
3.  **Rozlišení popisu a instance**: Oddělení obecné informace (Kniha - název, ISBN) od fyzických exemplářů (Výtisk - evidenční číslo, stav).

![[imgs/04.prednaska-022.jpg|226]] ![[imgs/04.prednaska-028.jpg|498]] ![[imgs/04.prednaska-030.jpg|498]]

*Obrázek: Ukázky postupného zpřesňování doménového modelu (Kniha a Autor, zavedení Výpůjčky, Kniha vs. Výtisk).*

## Časté chyby

- **Implementační detaily**: Zahrnutí atributů typu `rowid` nebo metod pro údržbu databáze.
- **Softwarové třídy**: Zahrnutí technických tříd (např. `DatabazeKnih`), které nepatří do reálného světa.
- **Cizí klíče**: Snaha identifikovat objekt pomocí atributu (např. `cisloFaktury` v třídě `Kniha`) místo použití asociace (zdroj: raw/lectures/04.prednaska.pdf).
- **Nevhodná dědičnost**: Použití generalizace pro kategorie (např. Žánry), které se mohou měnit. Vhodnější je asociace na samostatnu třídu.
- **Modelování historie jako entity**: Historie sama o sobě není entita, ale vlastnost dat v čase (správně se modeluje např. pomocí entity Cena s platností od-do).
- **Pletení instance a popisu**: Třída by neměla obsahovat atributy instance i obecného popisu dohady.

![[imgs/04.prednaska-042.jpg|216]] ![[imgs/04.prednaska-046.jpg|203]]
![[imgs/04.prednaska-048.jpg|555]] ![[imgs/04.prednaska-052.jpg|411]]
![[imgs/04.prednaska-054.jpg|497]] ![[imgs/04.prednaska-056.jpg|501]]
![[imgs/04.prednaska-058.jpg|131]] ![[imgs/04.prednaska-050.jpg|438]]

*Obrázek: Příklady nejčastějších chyb v doménovém modelu (implementační detaily, softwarové třídy, cizí klíče, nevhodná dědičnost, míchání instance a popisu).*

## Související stránky

- [[role-analytika]]
- [[obchodni-procesy]]
- [[stavovy-diagram]]

---
#analyza #data #uml #class-diagram #modelovani #BI-SWI
