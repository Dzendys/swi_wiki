# Doménový model

**Shrnutí**: Abstraktní model popisující klíčové entity problémové domény, jejich vlastnosti (atributy) a vzájemné vztahy. Slouží k pochopení datové struktury z pohledu business logiky.

**Zdroje**:
- `raw/lectures/01.prednaska.pdf`
- `raw/extra/Class Diagram Domain Model.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

**Doménový model** (Domain Model) je klíčovým výstupem analytika, který odpovídá na otázku, s jakými daty a entitami systém pracuje (zdroj: raw/lectures/01.prednaska.pdf). K jeho tvorbě se využívá **UML Diagram tříd** (Class Diagram), avšak na vyšší úrovni abstrakce než u návrhu softwaru (zdroj: raw/extra/Class Diagram Domain Model.pdf).

## Účel a charakteristika
- **Slovníček pojmů**: Slouží ke sjednocení terminologie mezi zákazníkem a vývojáři.
- **Abstrakce**: Neobsahuje implementační detaily (metody, programátorské datové typy).
- **Zasazení**: Entity v doménovém modelu reprezentují reálné objekty (např. Kniha, Čtenář, Výpůjčka), nikoliv tabulky v databázi (zdroj: raw/extra/Class Diagram Domain Model.pdf).

## Prvky modelu
- **Třída (Entity)**: Obdélník obsahující název entity. Lze doplnit **atributy** (vlastnosti entity) s jednoduchými typy (číslo, text, datum).
- **Asociace**: Propojení mezi entitami s definovanou **násobností** (např. 1..*), která určuje, kolik instancí jedné entity se může pojit s instancí entity druhé.
- **Generalizace (Dědičnost)**: Umožňuje modelovat hierarchii entit (potomek dědí vlastnosti rodiče) (zdroj: raw/extra/Class Diagram Domain Model.pdf).

## Časté chyby
- **Nevhodné použití dědičnosti**: Použití generalizace tam, kde by byl vhodnější atribut nebo vazba na jinou entitu (např. kategorie jako samostatné podtřídy vs. vazba na entitu Žánr).
- **Zachycení historie**: Snaha modelovat vývoj atributu v čase pomocí prázdné entity "Historie" místo vytvoření strukturované vazby s datem platnosti (zdroj: raw/extra/Class Diagram Domain Model.pdf).

## Související stránky
- [[role-analytika]]
- [[obchodni-procesy]]

---
#analyza #data #uml #class-diagram #modelovani #BI-SWI
