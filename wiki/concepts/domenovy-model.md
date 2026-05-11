# Doménový model

**Shrnutí**: Abstraktní model popisující klíčové entity problémové domény, jejich vlastnosti (atributy) a vzájemné vztahy. Slouží k pochopení datové struktury z pohledu business logiky a jako základ pro design.

**Zdroje**:

- `raw/lectures/01.prednaska.pdf`
- `raw/lectures/04.prednaska.pdf`
- `raw/extra/Class Diagram Domain Model.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

**Doménový model** (Domain Model) je klíčovým výstupem analytika, který odpovídá na otázku, s jakými daty a entitami systém pracuje (zdroj: raw/lectures/01.prednaska.pdf). K jeho tvorbě se využívá **UML Diagram tříd** (Class Diagram) na vysoké úrovni abstrakce (zdroj: raw/extra/Class Diagram Domain Model.pdf).

![[imgs/04.prednaska-037.jpg|520]]

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

    ![[imgs/04.prednaska-016.jpg|400]]


- **Atribut vs. Asociace**: Pro doménový model je názornější modelovat komplexní vlastnosti jako samostatné třídy spojené asociací.

    ![[imgs/04.prednaska-014.jpg|450]]


## Postup tvorby a refaktoring
Při tvorbě doménového modelu postupně zpřesňujeme strukturu entit tak, aby co nejlépe odpovídala realitě.

1.  **První návrh**: Často začínáme s atributy, které ale mají omezení (např. nemožnost více autorů).

    ![[imgs/04.prednaska-024.jpg|200]]


2.  **Vyčlenění entit**: Místo atributů (např. jméno autora) vytváříme samostatné entity (Autor).

    ![[imgs/04.prednaska-026.jpg|200]]


3.  **Sledování výpůjček (1. varianta)**: Přidání třídy Čtenář s přímou vazbou, což ale neumožňuje historii.

    ![[imgs/04.prednaska-028.jpg|200]]


4.  **Modelování historie**: Zavedení vazební entity (Výpůjčka), která umožňuje sledovat historii výpůjček.

    ![[imgs/04.prednaska-032.jpg|350]]


5.  **Rozlišení popisu a instance**: Oddělení obecné informace (Kniha) od fyzických exemplářů (Výtisk).

    ![[imgs/04.prednaska-035.jpg|350]]


6.  **Finální model**: Propojení všech entit včetně Rezervací.

    ![[imgs/04.prednaska-037.jpg|500]]


## Časté chyby

Při tvorbě doménového modelu je nutné se vyvarovat technických detailů a míchání různých úrovní abstrakce.

**1. Implementační detaily a softwarové třídy**
Doménový model nesmí obsahovat technické atributy (např. `rowid`) ani metody pro správu dat (např. `print()`, `backup()`). Rovněž sem nepatří čistě softwarové třídy jako `DatabazeKnih`.

![[imgs/04.prednaska-046.jpg|200]] ![[imgs/04.prednaska-048.jpg|200]]


**2. Cizí klíče místo asociací**
Objekty by měly být propojeny pomocí asociací, nikoliv pomocí ID nebo cizích klíčů (např. `cisloFaktury` v třídě `Kniha`).

![[imgs/04.prednaska-050.jpg|400]]


**3. Míchání instance a popisu**
Třída nesmí kombinovat atributy obecného popisu (např. `ISBN`) s atributy konkrétního fyzického kusu (např. `evidenční číslo`).

![[imgs/04.prednaska-052.jpg|350]]


**4. Nevhodná dědičnost pro kategorie**
Pokud se kategorie mohou měnit nebo objekt může patřit do více kategorií, je lepší použít asociaci na samostatnou třídu než dědičnost.

| Špatně | Dobře |
| :---: | :---: |
| ![[imgs/04.prednaska-054.jpg|200]] | ![[imgs/04.prednaska-056.jpg|200]] |

**5. Nevhodné modelování historie**
Historie není samostatná entita, ale záznam změn v čase. Správně se modeluje např. pomocí vazební entity s časovou platností.

| Špatně | Dobře |
| :---: | :---: |
| ![[imgs/04.prednaska-058.jpg|200]] | ![[imgs/04.prednaska-060.jpg|120]] |


## Související stránky

- [[role-analytika]]
- [[obchodni-procesy]]


---
#analyza #data #uml #class-diagram #modelovani #BI-SWI
