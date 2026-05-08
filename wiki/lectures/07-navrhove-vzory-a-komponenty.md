# 07. Návrhové vzory a komponenty

**Shrnutí**: Sedmá přednáška prohlubuje znalosti z oblasti návrhu softwaru se zaměřením na komponenty, rozhraní, mechanismy propojování (IoC/DI) a vybrané návrhové vzory GoF.

**Zdroje**:
- `raw/lectures/07.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Tato přednáška se věnuje technikám, jak zajistit nízkou provázanost (low coupling) v rozsáhlých systémech.

## Klíčová témata přednášky

### 1. Rozhraní a komponenty
Byl definován rozdíl mezi logickým rozhraním a fyzickou komponentou. Rozhraní je klíčovým nástrojem pro oddělení specifikace od implementace.
- **Komponenta**: Fyzická, samostatně nasaditelná jednotka.
- **Diagram komponent**: UML diagram pro zobrazení nabízených a vyžadovaných rozhraní.
Podrobnosti viz [[komponenty-a-rozhrani]].

### 2. Propojování a Inversion of Control
Vysvětlení, proč je manuální vytváření instancí nevhodné pro velké systémy a jak tento problém řeší **IoC kontejnery** (např. Spring). 
- **Dependency Injection**: Vstřikování závislostí přes konstruktor nebo settery.
- **Bean Scopes**: Definice životního cyklu objektů ve Springu (Singleton, Prototype atd.).
Podrobnosti viz [[dependency-injection]].

### 3. Vybrané GoF vzory
Přednáška představila pět základních návrhových vzorů rozdělených do tří kategorií:
- **Creational**: Abstract Factory (vytváření rodin produktů), Builder (konstrukce složitých objektů).
- **Behavioral**: State (chování závislé na stavu), Observer (upozorňování na změny).
- **Structural**: Adapter (konverze rozhraní).
Podrobnosti viz [[navrhove-vzory-gof]].

## Související stránky
- [[komponenty-a-rozhrani]]
- [[dependency-injection]]
- [[navrhove-vzory-gof]]
- [[navrh-softwaru]]
- [[softwarova-architektura]]

---
#swi #prednaska #navrhove-vzory #komponenty #di #ioc #BI-SWI
