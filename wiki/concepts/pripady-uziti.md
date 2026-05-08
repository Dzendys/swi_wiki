# Případy užití (Use Case)

**Shrnutí**: Technika pro zachycení funkčních požadavků systému z pohledu uživatele. Popisuje interakce mezi aktéry a systémem za účelem dosažení určitého cíle.

**Zdroje**:
- `raw/lectures/01.prednaska.pdf`
- `raw/extra/Use Case Model.pdf`
- `raw/extra/Ukázka UC.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

**Model případů užití** (Use Case Model) slouží k nadefinování požadavků a specifikaci rozsahu (scope) projektu (zdroj: raw/lectures/01.prednaska.pdf).

## Základní pojmy
- **Use Case (případ užití)**: Specifický způsob využití systému aktérem k dosažení měřitelného cíle. Představuje ucelenou jednotku funkcionality (zdroj: raw/extra/Use Case Model.pdf).
- **Aktér (Actor)**: Role, kterou hraje externí entita (člověk, jiný systém, čas) vůči systému. Aktér je vždy vně systému (zdroj: raw/extra/Use Case Model.pdf).
- **Asociace**: Propojení mezi aktérem a případem užití, naznačující jejich vzájemnou interakci.

## Specifikace případu užití
Každý případ užití by měl být detailně popsán (typicky textově). Standardní specifikace obsahuje:
- **Název**: Jasné a výstižné pojmenování (např. "Vypůjčení knihy").
- **Stručný popis**: Účel případu užití.
- **Aktéři**: Seznam zapojených aktérů.
- **Scénáře**:
    - **Hlavní (úspěšný) scénář**: Ideální průběh bez chyb (tzv. "happy path").
    - **Alternativní scénáře**: Odchylky od hlavního toku, řešení chybových stavů.
- **Vstupní podmínky (Preconditions)**: Stavy, které musí být splněny před spuštěním (např. "Čtenář je přihlášen").
- **Výstupní podmínky (Postconditions)**: Stavy systému po úspěšném dokončení (např. "Výpůjčka je evidována") (zdroj: raw/extra/Ukázka UC.pdf).

## Vztahy mezi případy užití
- **Include (zahrnutí)**: Jeden případ užití povinně využívá funkcionalitu jiného (vhodné pro sdílené kroky).
- **Extend (rozšíření)**: Podmíněné rozšíření základního případu užití o doplňkovou funkcionalitu (zdroj: raw/extra/Use Case Model.pdf).

## Doporučení pro tvorbu scénářů
- **Popisujte „co“, nikoliv „jak“**: Zaměřte se na logické kroky, nikoliv na detaily uživatelského rozhraní (např. "kliknutí na tlačítko").
- **Detailně pouze „zajímavé“ UC**: Vyhněte se zbytečnému rozepisování triviálních operací.
- **Využijte grafiku**: Pokud je scénář složitý (mnoho alternativních toků), doplňte jej [[diagram-aktivit|diagramem aktivit]].
- **Wireframing**: Pochopení případu užití velmi usnadňuje nákres obrazovky (zdroj: raw/lectures/03.prednaska.pdf).

## Granularita a úrovně detailu
Správně zvolená granularita je zásadní pro odhady pracnosti. Doporučuje se:
- Jeden scénář má cca **10 kroků**.
- Provedení uživatelem trvá řádově **hodiny** (zdroj: raw/lectures/03.prednaska.pdf).

Model může být zpracován na různých úrovních:
- **Stručný**: Pouze výčet aktérů, UC a jejich cílů + diagram. Vhodné pro frameworky nebo pokud je vývojář součástí analytického týmu.
- **Detailní**: Obsahuje textové scénáře, alternativní toky a pre/post-podmínky. Nutné pro fixaci rozsahu u zakázkových systémů (zdroj: raw/lectures/03.prednaska.pdf).

## Časté chyby v UC modelu
- **Snaha znázornit tok událostí v diagramu**: K tomu slouží scénáře nebo diagramy aktivit.
- **Zobrazování datových úložišť**: Use Case diagram není datový model.
- **Případ užití bez aktéra**: UC, který nikdo nevyužívá, nemá v systému smysl.
- **Zahrnutí činností mimo systém**: Ty patří do [[obchodni-procesy|modelu obchodních procesů]] (zdroj: raw/lectures/03.prednaska.pdf).

## Související stránky
- [[role-analytika]]
- [[diagram-aktivit]]
- [[pozadavky]]
- [[uzivatelske-pribehy]]

---
#use-case #analyza #poadavky #uml #chyby #BI-SWI
