# Inversion of Control a Dependency Injection

**Shrnutí**: Návrhové principy sloužící k uvolnění vazeb mezi komponentami. Dependency Injection (DI) je konkrétní formou Inversion of Control (IoC), kde jsou závislosti objektu "vstřikovány" zvenčí.

**Zdroje**:

- `raw/lectures/07.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Při manuálním propojování komponent v kódu (např. `new CtenarDAO()`) vzniká silná vazba na konkrétní implementaci, což ztěžuje testování a výměnu částí systému. **Inversion of Control (IoC)** tento přístup obrací – objekt si své závislosti nevytváří sám, ale dostává je od někoho jiného.

## Dependency Injection (DI)
DI je technika, kdy IoC kontejner (např. Spring) automaticky dosazuje (vstřikuje) závislosti do tříd. Třída pak pracuje pouze s rozhraním, nikoliv s konkrétní implementací.

### Způsoby vstřikování (DI types)

- **Constructor-based**: Závislosti jsou předávány jako parametry konstruktoru. Doporučeno pro povinné závislosti (umožňuje neměnnost - immutability).
- **Setter-based**: Závislosti jsou předávány pomocí setter metod. Vhodné pro volitelné závislosti.

## IoC Kontejnery
Softwarové rámce, které spravují životní cyklus objektů (beans) a jejich propojení:
- **Java**: Spring, EJB.
- **PHP**: Symfony (Service Configurator).

### Spring Bean Scopes
V frameworku Spring lze definovat, jak dlouho instance (bean) žije:
- **Singleton**: Jedna instance pro celý kontejner (výchozí).
- **Prototype**: Nová instance při každém vyžádání.
- **Request**: Instance žije po dobu jednoho HTTP požadavku (web).
- **Session**: Instance žije po dobu jedné uživatelské relace (web).

## Výhody
- **Snadná výměna implementace**: Např. výměna reálné databáze za testovací (mock) bez změny business logiky.
- **Deklarativní vazby**: Propojení je definováno v konfiguraci (anotace, XML), ne pevně v kódu.

## Související stránky
- [[komponenty-a-rozhrani]]
- [[vrstvy-architektury]]
- [[navrhove-vzory-gof]]

---
#swi #ioc #di #spring #navrh #loose-coupling #BI-SWI
