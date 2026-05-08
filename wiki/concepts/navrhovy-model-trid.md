# Návrhový model tříd

**Shrnutí**: Rozšířený model tříd, který kromě doménových entit zachycuje konkrétní softwarové třídy, jejich zodpovědnosti (metody), datové typy a viditelnost pro následnou implementaci.

**Zdroje**:
- `raw/lectures/05.prednaska.pdf`
- `raw/extra/GRASP.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Zatímco [[domenovy-model|doménový model]] popisuje entity reálného světa a jejich vztahy, návrhový model tříd (Design Class Diagram) dokumentuje architektonická a implementační rozhodnutí. Slouží jako přímý podklad pro generování zdrojových kódů.

## Prvky návrhového modelu
Návrhový model vychází z doménového, ale konkretizuje ho:
- **Atributy**: Upřesnění přesných datových typů (např. `String`, `Date`, `int`).
- **Asociace**: Určení směru navigovatelnosti asociace a názvů konců asociací, což v kódu často odpovídá referenčním atributům.
- **Metody**: Přiřazení zodpovědností jednotlivým třídám ve formě metod. Obsahují vstupní parametry, výstupní typy a specifikaci viditelnosti (`public +`, `private -`, `protected #`, `package ~`).
- **Nové třídy**: Zavedení specifických softwarových tříd, které v reálné doméně neexistují (např. controllery, repository, buildery).
- **Pokročilá UML notace**: Zobrazování statických (třídních) metod a atributů, abstraktních tříd, **[[komponenty-a-rozhrani|rozhraní (interface)]]** a generických typů (šablon, např. `List<T>`).

*Doporučení pro přehlednost*: Aby byl diagram čitelný, často se nezobrazují automaticky generované gettery a settery, a nemusí zachycovat úplně každou softwarovou třídu v systému. Důležité je zachytit principy a klíčové vzory (např. **[[navrhove-vzory-gof|GoF vzory]]**).

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
