# Návrhový model tříd

**Shrnutí**: Rozšířený model tříd, který kromě doménových entit zachycuje konkrétní softwarové třídy, jejich zodpovědnosti (metody), datové typy a viditelnost pro následnou implementaci.

**Zdroje**:

- `raw/lectures/05.prednaska.pdf`
- `raw/extra/GRASP.pdf`



---

Zatímco [[domenovy-model|doménový model]] popisuje entity reálného světa a jejich vztahy, návrhový model tříd (Design Class Diagram) dokumentuje architektonická a implementační rozhodnutí. Slouží jako přímý podklad pro generování zdrojových kódů.

## Prvky návrhového modelu
Návrhový model vychází z doménového, ale konkretizuje ho:

### Rozšířená notace tříd
V návrhovém modelu využíváme plnou sílu UML notace pro zachycení implementačních detailů:

- **Viditelnost**: public (`+`), protected (`#`), package (`~`), private (`-`).
- **Členové**: statické prvky (podtržené), abstraktní prvky (kurzíva), konstanty (`{readOnly}`).
- **Šablony (Templates)**: Modelování generických typů (např. `Seznam<T>`).

![[imgs/05.prednaska-053.jpg|237]] ![[imgs/05.prednaska-055.jpg|153]]

*Obrázek: Přehled prvků třídy v UML a ukázka použití šablon.*

### Reprezentace vztahů a rozhraní
V návrhové fázi se rozhodujeme, jak budou vztahy z doménového modelu realizovány v kódu. UML nabízí několik ekvivalentních notací:

1. **Vztah pomocí atributu**: Vztah je zapsán přímo formou atributu třídy (např. `vyplnil: Student`). Je to kompaktní zápis často používaný v detailních diagramech.

    ![[imgs/05.prednaska-057.jpg|350]]

2. **Grafická asociace**: Klasické znázornění pomocí čáry/šipky mezi třídami. Umožňuje přehledně zobrazit násobnosti (multiplicity) a směry závislostí.

    ![[imgs/05.prednaska-058.jpg|400]]

3. **Realizace rozhraní**: Třída implementuje sadu metod definovanou v rozhraní. V UML se značí přerušovanou čarou s prázdnou šipkou směrem k rozhraní.

    ![[imgs/05.prednaska-060.jpg|150]]


## Přiřazování zodpovědností (GRASP)
Klíčovým úkolem při tvorbě návrhového modelu je správné rozdělení zodpovědností (převod scénářů z [[pripady-uziti|případů užití]] na metody konkrétních tříd). K tomu se využívají vzory GRASP (General Responsibility Assignment Software Patterns). Často se také využívá princip **[[dependency-injection|Dependency Injection]]** pro uvolnění vazeb mezi třídami.

- **Informační expert (Information Expert)**: Zodpovědnost by měla být přidělena třídě, která má informace potřebné k jejímu splnění.
- **Nízká provázanost (Low Coupling)**: Třídy by měly být navrženy tak, aby závislost mezi nimi byla co nejmenší. To usnadňuje údržbu a znovupoužitelnost.
- **Vysoká soudržnost (High Cohesion)**: Zodpovědnosti jedné třídy by měly spolu úzce souviset a tvořit logický celek. Třída by neměla dělat "příliš mnoho nesouvisejících věcí".

## Realizace v kódu
Návrhový model slouží jako přímý podklad pro implementaci. Pomocí trasování lze sledovat vztah mezi původní doménovou entitou a její konkrétní softwarovou realizací.

![[imgs/05.prednaska-062.jpg|432]]

*Obrázek: Ukázka trasování (stereotyp «trace») od doménových tříd k detailnímu návrhu pro implementaci v Javě/C#.*


## Související stránky

- [[navrh-softwaru]]
- [[softwarova-architektura]]
- [[domenovy-model]]

---
#swi #uml #class-diagram #grasp #design #BI-SWI
