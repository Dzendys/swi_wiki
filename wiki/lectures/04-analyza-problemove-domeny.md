# Analýza problémové domény

**Shrnutí**: Tato přednáška se zaměřuje na tvorbu analytického doménového modelu, hledání entit v systému a zachycení jejich stavů pomocí stavových diagramů.

**Zdroje**:
- `raw/lectures/04.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Cílem analýzy problémové domény je vytvořit [[domenovy-model|doménový model]], který slouží jako základ pro následný design systému (databázový model, model tříd) (zdroj: raw/lectures/04.prednaska.pdf).

## Analytický doménový model
Doménový model zachycuje:
- Popis dat a jejich význam.
- Vazby mezi entitami.
- Atributy a stavy entit (zdroj: raw/lectures/04.prednaska.pdf).

Pro jeho tvorbu se využívá **UML Diagram tříd** na vysoké úrovni abstrakce. Více detailů naleznete na stránce [[domenovy-model]].

## Modelování stavů
Pro entity s významným životním cyklem se vytváří [[stavovy-diagram|stavový diagram (UML State Machine)]]. Ten pomáhá vyjasnit:
- Stavy, ve kterých se entita může nacházet.
- Události a podmínky vyvolávající přechody mezi stavy (zdroj: raw/lectures/04.prednaska.pdf).

## Hledání entit
Entity (třídy) se hledají jako podstatná jména v:
- Business procesních modelech.
- [[pripady-uziti|Modelech případů užití]].
- Slovníčku pojmů (zdroj: raw/lectures/04.prednaska.pdf).

## Související stránky
- [[domenovy-model]]
- [[stavovy-diagram]]
- [[role-analytika]]
- [[obchodni-procesy]]

---
#analyza #domena #entity #stavovy-diagram #BI-SWI
