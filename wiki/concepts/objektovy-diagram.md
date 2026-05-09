# Objektový diagram

**Shrnutí**: Strukturální diagram UML, který zobrazuje instance tříd, jejich aktuální stav (hodnoty atributů) a vazby v konkrétním časovém okamžiku.

**Zdroje**:

- `raw/lectures/08.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Objektový diagram (Object Diagram) patří v UML do skupiny **diagramů struktur**. Na rozdíl od [[navrhovy-model-trid|diagramu tříd]], který popisuje obecnou strukturu (šablony), objektový diagram poskytuje "snímek" (snapshot) aktuálního stavu systému v daný časový okamžik (zdroj: raw/lectures/08.prednaska.pdf).

## Význam a použití

- **Usnadňuje pochopení složitých diagramů tříd**: Pomáhá vizualizovat, jak reálná data v systému vypadají.
- **Validace modelu**: Ověření, zda diagram tříd umožňuje vytvořit požadované konfigurace objektů.
- **Příklady**: Často se používá pro dokumentaci konkrétních scénářů nebo testovacích dat.

## Prvky diagramu

1.  **Objekt (Instance třídy)**: Zobrazuje se jako obdélník s názvem instance a třídy podtrženým (formát `názevInstance : NázevTřídy`). Pokud je název instance vynechán, jde o anonymní objekt.
2.  **Stav objektu**: V bloku pod názvem jsou uvedeny konkrétní **hodnoty atributů** v daném okamžiku (např. `rokVydani = 2005`).
3.  **Spojení (Link)**: Instance asociace mezi objekty. Zobrazuje se jako čára propojující objekty. Na rozdíl od asociací v diagramu tříd nemají spojení násobnost (multiplicity).

![[imgs/08.prednaska-020.jpg|209]]

*Obrázek: Ukázka instancí tříd s konkrétními hodnotami atributů a vazbami.*

## Příklad komplexního diagramu
Objektový diagram pomáhá vizualizovat multiplicity v praxi – například že jeden konkrétní autor napsal několik konkrétních knih, z nichž každá má několik fyzických výtisků v různých stavech.

![[imgs/08.prednaska-022.jpg|676]]

*Obrázek: Modelování konkrétních dat v systému knihovny.*

## Příklad (EA: UML Structural - Object)
V nástrojích jako Enterprise Architect se objektový diagram využívá k modelování konkrétních instancí entit, např. konkrétní kniha `Babička` od autorky `Boženy Němcové` s konkrétním evidenčním číslem.

## Související stránky

- [[navrhovy-model-trid]]
- [[objektove-paradigma]]
- [[sekvencni-diagram]]

---
#uml #objektovy-diagram #snapshot #softwarove-inzenyrstvi #BI-SWI
