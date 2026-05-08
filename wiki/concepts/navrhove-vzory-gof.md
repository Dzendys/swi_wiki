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

![|x350](imgs/07.prednaska-031.jpg)
*Obrázek: UML diagram vzoru Abstract Factory (Klient závisí pouze na abstraktních rozhraních).*

- **[[softwarova-architektura#Využití návrhových vzorů|Stavitel (Builder)]]**: Odděluje konstrukci složitého objektu od jeho reprezentace. Stejný postup konstrukce může vytvořit různé reprezentace (např. SQL dotaz pro různé dialekty). Skládá se z *Directora* (řídí strukturu) a *Buildera* (staví části).

![|450](imgs/05.prednaska-073.jpg) ![|300](imgs/05.prednaska-076.jpg) ![|250](imgs/05.prednaska-079.jpg)
*Obrázek: Implementace vzoru Builder pro generování SQL skriptů pro různé databáze.*

## 2. Vzory chování (Behavioral)
Zabývají se algoritmy a přiřazováním zodpovědností mezi objekty.
- **Stav (State)**: Umožňuje objektu měnit své chování při změně jeho vnitřního stavu. Vypadá to, jako by objekt změnil svou třídu. Odstraňuje složitá větvení (`switch`, `if-else`).

![|250](imgs/07.prednaska-038.jpg) ![|350](imgs/07.prednaska-040.jpg)
*Obrázek: Struktura vzoru State a jeho konkrétní aplikace na životní cyklus výtisku.*

Využití vzoru State v praxi lze ilustrovat pomocí [[sekvencni-diagram|sekvenčních diagramů]], které ukazují, jak objekt deleguje chování na aktuální instanci stavu.

![|300](imgs/07.prednaska-042.jpg) ![|350](imgs/07.prednaska-044.jpg)
*Obrázek: Spolupráce objektů při změně stavu výtisku.*

- **Pozorovatel (Observer)**: Definuje závislost 1:N mezi objekty tak, že když jeden objekt změní stav, všechny závislé objekty jsou o tom informovány a automaticky aktualizovány. (Klíčový prvek vzoru [[mvc-mvp|MVC]]).

## 3. Strukturální vzory (Structural)
Zabývají se tím, jak jsou třídy a objekty skládány do větších celků.
- **Adaptér (Adapter)**: Převádí rozhraní jedné třídy na jiné rozhraní, které klient očekává. Umožňuje spolupráci tříd, které by jinak kvůli nekompatibilním rozhraním nespolupracovaly.

![|x300](imgs/07.prednaska-048.jpg)
*Obrázek: UML diagram vzoru Adaptér pro propojení nekompatibilních rozhraní.*

## Související stránky
- [[navrh-softwaru]]
- [[navrhovy-model-trid]]
- [[dependency-injection]]

---
#swi #navrhove-vzory #gof #oo-design #BI-SWI
