# Návrhové vzory GoF

**Shrnutí**: Klasické objektově orientované návrhové vzory publikované skupinou "Gang of Four" (E. Gamma, R. Helm, R. Johnson, J. Vlissides). Pomáhají řešit typické problémy v návrhu tříd a objektů.

**Zdroje**:

- `raw/lectures/05.prednaska.pdf`
- `raw/lectures/07.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Vzory se dělí do tří základních kategorií podle svého účelu:

## 1. Vzory pro vytváření objektů (Creational)
Zaměřují se na proces vytváření objektů tak, aby byl systém nezávislý na způsobu jejich vzniku.

- **Abstraktní továrna (Abstract Factory)**: Poskytuje rozhraní pro vytváření rodin souvisejících nebo závislých objektů, aniž by specifikovala jejich konkrétní třídy. Klient pracuje pouze s rozhraním továrny a produktů.

![[imgs/07.prednaska-031.jpg|617]]

*Obrázek: UML diagram vzoru Abstract Factory (Klient závisí pouze na abstraktních rozhraních).*

- **[[softwarova-architektura#Využití návrhových vzorů|Stavitel (Builder)]]**: Odděluje konstrukci složitého objektu od jeho reprezentace. Stejný postup konstrukce může vytvořit různé reprezentace (např. SQL dotaz pro různé dialekty).

    **Vývoj implementace (iterace):**

    1. **Základní abstrakce**: Definice rozhraní `SqlBuilder`, které určuje kroky stavby (např. `createTable`, `insertData`). Klient je odstíněn od konkrétní realizace.

        ![[imgs/05.prednaska-073.jpg|400]]

    2. **Konkrétní realizace**: Vytvoření konkrétních stavitelů pro jednotlivé databáze (např. `OracleBuilder`, `PostgresBuilder`), které implementují kroky podle specifik daného dialektu.

        ![[imgs/05.prednaska-076.jpg|500]]

    3. **Optimalizace (Abstraktní předek)**: Zavedení třídy `AbstractSqlBuilder`, která obsahuje sdílenou logiku společnou pro všechny (nebo většinu) databází, čímž se zamezuje duplicitě kódu v konkrétních stavitelích.

        ![[imgs/05.prednaska-079.jpg|500]]


## 2. Vzory chování (Behavioral)
Zabývají se algoritmy a přiřazováním zodpovědností mezi objekty.

- **Stav (State)**: Umožňuje objektu měnit své chování při změně jeho vnitřního stavu. Vypadá to, jako by objekt změnil svou třídu. Odstraňuje složitá větvení (`switch`, `if-else`).

![[imgs/07.prednaska-038.jpg|635]] ![[imgs/07.prednaska-040.jpg|807]]

*Obrázek: Struktura vzoru State a jeho konkrétní aplikace na životní cyklus výtisku.*

Využití vzoru State v praxi lze ilustrovat pomocí [[sekvencni-diagram|sekvenčních diagramů]], které ukazují, jak objekt deleguje chování na aktuální instanci stavu.

- **Pozorovatel (Observer)**: Definuje závislost 1:N mezi objekty tak, že když jeden objekt změní stav, všechny závislé objekty jsou o tom informovány a automaticky aktualizovány. (Klíčový prvek vzoru [[mvc-mvp|MVC]]).

## 3. Strukturální vzory (Structural)
Zabývají se tím, jak jsou třídy a objekty skládány do větších celků.

- **Adaptér (Adapter)**: Převádí rozhraní jedné třídy na jiné rozhraní, které klient očekává. Umožňuje spolupráci tříd, které by jinak kvůli nekompatibilním rozhraním nespolupracovaly.

![[imgs/07.prednaska-048.jpg|872]]

*Obrázek: UML diagram vzoru Adaptér pro propojení nekompatibilních rozhraní.*

## Související stránky

- [[navrh-softwaru]]
- [[navrhovy-model-trid]]
- [[dependency-injection]]

---
#swi #navrhove-vzory #gof #oo-design #BI-SWI
