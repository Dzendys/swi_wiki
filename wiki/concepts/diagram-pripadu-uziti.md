# Diagram případů užití (UML)

**Shrnutí**: Grafické znázornění funkčních požadavků systému, aktérů a jejich vzájemných interakcí. Slouží k definici hranic systému a identifikaci rolí.

**Zdroje**:
- `raw/lectures/01.prednaska.pdf`
- `raw/lectures/03.prednaska.pdf`
- `raw/extra/Use Case Model.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

[[diagram-pripadu-uziti|UML Diagram případů užití]] (Use Case Diagram) patří do skupiny diagramů chování. Je doplňkem k textovému popisu [[pripady-uziti|případů užití]] a slouží pro rychlou orientaci v rozsahu systému (zdroj: raw/lectures/03.prednaska.pdf).

## Notace a prvky
- **Aktér (Actor)**: Panáček reprezentující roli externí entity (uživatel, jiný systém, čas). Aktér je vždy vně systému (zdroj: raw/extra/Use Case Model.pdf).
- **Případ užití (Use Case)**: Bublina (elipsa) reprezentující ucelenou jednotku funkcionality.
- **Hranice systému (Subject Boundary)**: Obdélník ohraničující případy užití, které systém realizuje.
- **Asociace**: Čára spojující aktéra s případem užití (zdroj: raw/lectures/03.prednaska.pdf).

## Vztahy mezi případy užití
Vztahy by se měly používat střídmě, aby diagram zůstal přehledný.
- **Include (zahrnutí)**: Směrovaná čárkovaná šipka se stereotypem `«include»`. Označuje povinné vyčlenění **sdílené logiky** (reusage). Nemá se používat pro pouhý rozklad (dekompozici) jednoho UC na kroky (zdroj: raw/extra/Use Case Model.pdf).
- **Extend (rozšíření)**: Směrovaná čárkovaná šipka se stereotypem `«extend»`. Označuje volitelné rozšíření základního UC za určitých podmínek. Opět platí, že by se nemělo jednat o pouhou dekompozici (zdroj: raw/extra/Use Case Model.pdf).

## Vztahy mezi aktéry
- **Generalizace (dědičnost)**: Plná čára s uzavřenou šipkou u rodiče. Potomek dědí všechny asociace k případům užití od svého rodiče, což zpřehledňuje diagram (zdroj: raw/lectures/03.prednaska.pdf).

## Související stránky
- [[pripady-uziti]]
- [[role-analytika]]
- [[pozadavky]]

---
#uml #use-case #diagram #analyza #poadavky #BI-SWI
