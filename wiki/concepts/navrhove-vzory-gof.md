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
- **[[softwarova-architektura#Využití návrhových vzorů|Stavitel (Builder)]]**: Odděluje konstrukci složitého objektu od jeho reprezentace. Stejný postup konstrukce může vytvořit různé reprezentace (např. SQL dotaz pro různé dialekty). Skládá se z *Directora* (řídí strukturu) a *Buildera* (staví části).

![Vzor Builder - Základní abstrakce](imgs/05.prednaska-073.jpg)
![Vzor Builder - Konkrétní stavitelé](imgs/05.prednaska-076.jpg)
![Vzor Builder - Využití abstraktního předka](imgs/05.prednaska-079.jpg)
*Obrázek: Implementace vzoru Builder pro generování SQL skriptů pro různé databáze.*

## 2. Vzory chování (Behavioral)
Zabývají se algoritmy a přiřazováním zodpovědností mezi objekty.
- **Stav (State)**: Umožňuje objektu měnit své chování při změně jeho vnitřního stavu. Vypadá to, jako by objekt změnil svou třídu. Odstraňuje složitá větvení (`switch`, `if-else`).

![Vzor State - Návrh implementace](imgs/05.prednaska-064.jpg)
![Vzor State - Korekce viditelnosti](imgs/05.prednaska-066.jpg)
*Obrázek: Návrh implementace životního cyklu pomocí vzoru State.*

- **Pozorovatel (Observer)**: Definuje závislost 1:N mezi objekty tak, že když jeden objekt změní stav, všechny závislé objekty jsou o tom informovány a automaticky aktualizovány. (Klíčový prvek vzoru [[mvc-mvp|MVC]]).

## 3. Strukturální vzory (Structural)
Zabývají se tím, jak jsou třídy a objekty skládány do větších celků.
- **Adaptér (Adapter)**: Převádí rozhraní jedné třídy na jiné rozhraní, které klient očekává. Umožňuje spolupráci tříd, které by jinak kvůli nekompatibilním rozhraním nespolupracovaly.

## Související stránky
- [[navrh-softwaru]]
- [[navrhovy-model-trid]]
- [[dependency-injection]]

---
#swi #navrhove-vzory #gof #oo-design #BI-SWI
