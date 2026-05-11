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

    ![[imgs/03.prednaska-032.jpg|70]] ![[imgs/03.prednaska-030.jpg|147]]

- **Případ užití (Use Case)**: Bublina (elipsa) reprezentující ucelenou jednotku funkcionality.
- **Hranice systému (Subject Boundary)**: Obdélník ohraničující případy užití, které systém realizuje.
- **Asociace**: Čára spojující aktéra s případem užití (zdroj: raw/lectures/03.prednaska.pdf).

![[imgs/03.prednaska-037.jpg|750]]

*Obrázek: Komplexní Use Case diagram zachycující hranice systému (IS knihovny), aktéry a jejich interakce.*

## Vztahy mezi aktéry

- **Generalizace (dědičnost)**: Plná čára s uzavřenou šipkou u rodiče. Potomek dědí všechny asociace k případům užití od svého rodiče, což zpřehledňuje diagram (zdroj: raw/lectures/03.prednaska.pdf).

![[imgs/03.prednaska-034.jpg|65]]

*Obrázek: Hierarchie aktérů (Knihovník dědí od Čtenáře).*

## Vztahy mezi případy užití
Vztahy by se měly používat střídmě, aby diagram zůstal přehledný.

- **Include (zahrnutí)**: Směrovaná čárkovaná šipka se stereotypem `«include»`. Označuje povinné vyčlenění **sdílené logiky** (reusage). Nemá se používat pro pouhý rozklad (dekompozici) jednoho UC na kroky (zdroj: raw/extra/Use Case Model.pdf).

    ![[imgs/03.prednaska-048.jpg|350]]

- **Extend (rozšíření)**: Směrovaná čárkovaná šipka se stereotypem `«extend»`. Označuje volitelné rozšíření základního UC za určitých podmínek. Opět platí, že by se nemělo jednat o pouhou dekompozici (zdroj: raw/extra/Use Case Model.pdf).

    ![[imgs/03.prednaska-051.jpg|350]]


## Typické chyby v UC diagramech

1.  **Modelování toku (sekvence)**: UC diagram není určen pro zobrazení pořadí kroků. K tomu slouží scénáře nebo diagramy aktivit.

| Špatně | Dobře |
| :---: | :---: |
| ![[imgs/03.prednaska-061.jpg|200]] | Pro modelování toku použijte **textové scénáře** nebo **[[diagram-aktivit\|diagramy aktivit]]**. |

2.  **Datová úložiště**: Databáze nebo soubory nejsou aktéři ani případy užití.

| Špatně | Dobře |
| :---: | :---: |
| ![[imgs/03.prednaska-063.jpg|200]] | Datová úložiště do UC diagramu nepatří. Pokud je potřeba, zachyťte je v **[[domenovy-model\|doménovém modelu]]**. |

3.  **Chybějící aktér**: Každý UC musí být iniciován nebo využíván nějakým aktérem.

| Špatně | Dobře |
| :---: | :---: |
| ![[imgs/03.prednaska-065.jpg|200]] | Každý případ užití musí být propojen s alespoň jedním **aktérem**. |

4.  **Činnosti mimo systém**: Modelovat by se měly pouze interakce se systémem, nikoliv fyzické činnosti uživatele (např. "přečíst knihu").

| Špatně | Dobře |
| :---: | :---: |
| ![[imgs/03.prednaska-067.jpg|200]] | Modelujte pouze akce, které probíhají **v interakci se systémem**. |

## Související stránky

- [[pripady-uziti]]
- [[role-analytika]]
- [[pozadavky]]

---
#uml #use-case #diagram #analyza #poadavky #BI-SWI
