# 08. Implementace

**Shrnutí**: Tato přednáška se věnuje fázi implementace, objektovému paradigmatu, pravidlům pro psaní čistého kódu a technikám refaktoringu.

**Zdroje**:
- `raw/lectures/08.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Implementace je hlavní pracovní postup u softwarových projektů a jediná činnost, která nemůže být vynechána. Cílem je dodat produkt, který funguje dle požadavků, snadno se používá, neobsahuje chyby, funguje v cílových prostředích a je snadno udržovatelný.

## Klíčová témata

### [[implementace|Proces implementace]]
- Přepis scénářů [[pripady-uziti|případů užití]] do kódu.
- Dodržování architektury a návrhových rozhodnutí.
- "Návrh v malém" – rozhodování o detailech v souladu s celkovou koncepcí.

### [[objektove-paradigma|Objektové paradigma]]
- Systém jako soubor komunikujících objektů.
- Základní pilíře: [[objektove-paradigma#Zapouzdření|zapouzdření]], [[objektove-paradigma#Dědičnost|dědičnost]], [[objektove-paradigma#Polymorfismus|polymorfismus]], abstraktní třídy.
- Sledování stavu pomocí [[objektovy-diagram|objektových diagramů]].

### [[clean-code|Základní pravidla (Clean Code)]]
- **SRP (Single Responsibility Principle)**: Jedna metoda = jedna zodpovědnost.
- **Law of Demeter**: "Don't talk to strangers" – omezení volání metod na známé objekty.
- **DRY (Don't Repeat Yourself)**: Eliminace duplicit kódu i dat.
- **Programování proti rozhraní**: Používání [[komponenty-a-rozhrani|rozhraní]] tam, kde se očekávají změny.
- **Liskov Substitution Principle (LSP)**: Správné použití dědičnosti (náhrada nadtřídy podtřídou nesmí rozbít kód). Upřednostnění skládání před dědičností.

### [[osetreni-chyb-a-logovani|Ošetření chyb a logování]]
- Strategie ošetření: vracení neutrálních hodnot, chybových kódů nebo vyvolání výjimek.
- Logování jako nástroj pro sledování běhu a diagnostiku (úrovně: DEBUG, INFO, WARN, ERROR, FATAL).

### [[refaktoring|Refaktoring]]
- Změna vnitřní struktury kódu bez změny vnějšího chování.
- Nutnost existence testů před začátkem refaktoringu.
- Odstraňování "code smells" (duplicity, dlouhé metody, velké třídy).

## Související stránky
- [[navrh-softwaru]]
- [[navrhovy-model-trid]]
- [[softwarova-architektura]]

---
#prednaska #implementace #clean-code #objektove-orientovane-programování #refaktoring #BI-SWI
