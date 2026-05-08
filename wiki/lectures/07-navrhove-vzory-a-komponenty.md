# 07. Návrhové vzory a komponenty

**Shrnutí**: Sedmá přednáška prohlubuje znalosti z oblasti návrhu softwaru se zaměřením na komponenty, rozhraní, mechanismy propojování (IoC/DI) a vybrané návrhové vzory GoF.

**Zdroje**:
- `raw/lectures/07.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Tato přednáška se věnuje pokročilým technikám pro zajištění nízké provázanosti (low coupling) a modularity v rozsáhlých systémech.

## Klíčová témata

### Rozhraní a komponenty
Základem modularity je oddělení specifikace od implementace pomocí [[komponenty-a-rozhrani|rozhraní]]. Přednáška definuje rozdíl mezi logickým rozhraním a fyzickou, samostatně nasaditelnou jednotkou (komponentou). Diagram komponent v UML slouží k vizualizaci nabízených a vyžadovaných služeb systému.

### Propojování a Dependency Injection
Pro flexibilní správu závislostí se využívají IoC kontejnery. Princip **[[dependency-injection|Dependency Injection]]** (vstřikování závislostí) umožňuje objektům získat své spolupracovníky zvenčí, místo aby si je samy vytvářely, což usnadňuje testování (mockování) a výměnu implementací.

### Návrhové vzory (GoF)
Přednáška představuje pět vybraných vzorů ze skupiny "Gang of Four" jako osvědčená řešení typických objektových problémů. Jedná se o vzory pro vytváření (Abstract Factory, Builder), chování (State, Observer) a strukturu (Adapter). Podrobnosti viz [[navrhove-vzory-gof]].

## Související stránky
- [[komponenty-a-rozhrani]]
- [[dependency-injection]]
- [[navrhove-vzory-gof]]
- [[navrh-softwaru]]
- [[softwarova-architektura]]

---
#swi #prednaska #navrhove-vzory #komponenty #di #ioc #BI-SWI
