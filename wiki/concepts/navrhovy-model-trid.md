# Návrhový model tříd

**Shrnutí**: Rozšířený model tříd, který kromě doménových entit zachycuje konkrétní softwarové třídy, jejich zodpovědnosti (metody), datové typy a viditelnost pro následnou implementaci.

**Zdroje**:
- `raw/lectures/05.prednaska.pdf`
- `raw/extra/GRASP.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Zatímco [[domenovy-model|doménový model]] popisuje entity reálného světa a jejich vztahy, návrhový model tříd (Design Class Diagram) dokumentuje architektonická a implementační rozhodnutí. Slouží jako přímý podklad pro generování zdrojových kódů.

![|x250](imgs/05.prednaska-062.jpg)
*Obrázek: Ukázka trasování (stereotyp «trace») od doménových tříd k detailnímu návrhu pro implementaci v Javě/C#.*

## Prvky návrhového modelu
Návrhový model vychází z doménového, ale konkretizuje ho:

### Rozšířená notace tříd
V návrhovém modelu využíváme plnou sílu UML notace pro zachycení implementačních detailů:
- **Viditelnost**: public (`+`), protected (`#`), package (`~`), private (`-`).
- **Členové**: statické prvky (podtržené), abstraktní prvky (kurzíva), konstanty (`{readOnly}`).
- **Šablony (Templates)**: Modelování generických typů (např. `Seznam<T>`).

![|x200](imgs/05.prednaska-053.jpg) ![|x200](imgs/05.prednaska-055.jpg)
*Obrázek: Přehled prvků třídy v UML a ukázka použití šablon.*

### Reprezentace vztahů a rozhraní
Vztahy lze v UML znázornit buď graficky asociací, nebo textově pomocí atributu třídy. Důležitým prvkem je také realizace rozhraní.

- **Realizace rozhraní**: Přerušovaná čára s prázdnou šipkou.
- **Asociace**: Určení směru navigovatelnosti a násobností.

![|x250](imgs/05.prednaska-057.jpg) ![|x250](imgs/05.prednaska-058.jpg) ![|x200](imgs/05.prednaska-060.jpg)
*Obrázek: Různé způsoby zachycení vztahů a implementace rozhraní.*

## Přiřazování zodpovědností (GRASP)
Klíčovým úkolem při tvorbě návrhového modelu je správné rozdělení zodpovědností (převod scénářů z [[pripady-uziti|případů užití]] na metody konkrétních tříd). K tomu se využívají vzory GRASP (General Responsibility Assignment Software Patterns). Často se také využívá princip **[[dependency-injection|Dependency Injection]]** pro uvolnění vazeb mezi třídami.

- **Informační expert (Information Expert)**: Zodpovědnost by měla být přidělena třídě, která má informace potřebné k jejímu splnění.
- **Nízká provázanost (Low Coupling)**: Třídy by měly být navrženy tak, aby závislost mezi nimi byla co nejmenší. To usnadňuje údržbu a znovupoužitelnost.
- **Vysoká soudržnost (High Cohesion)**: Zodpovědnosti jedné třídy by měly spolu úzce souviset a tvořit logický celek. Třída by neměla dělat "příliš mnoho nesouvisejících věcí".

## Související stránky
- [[navrh-softwaru]]
- [[softwarova-architektura]]
- [[domenovy-model]]

---
#swi #uml #class-diagram #grasp #design #BI-SWI
