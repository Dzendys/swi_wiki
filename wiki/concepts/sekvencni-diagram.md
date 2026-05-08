# Sekvenční diagram (UML)

**Shrnutí**: Interakční diagram v UML, který zobrazuje spolupráci objektů v čase. Slouží k modelování realizace scénářů případů užití.

**Zdroje**:
- `raw/lectures/06.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Sekvenční diagram (Sequence Diagram) patří mezi diagramy chování a je klíčový pro fázi [[navrh-softwaru|návrhu]]. Zatímco [[navrhovy-model-trid|diagram tříd]] zachycuje statickou strukturu, sekvenční diagram ukazuje, jak si objekty v čase vyměňují zprávy, aby splnily konkrétní úkol (scénář z [[pripady-uziti|případu užití]]).

## Základní notace
- **Životní čára (Lifeline)**: Svislá čárkovaná čára pod objektem.
- **Objekt**: Obdélník na vrcholu čáry. Zápis: `názevObjektu : Třída` (pojmenovaný) nebo `: Třída` (anonymní).
- **Zpráva (Message)**: Vodorovná šipka mezi životními čárami.
    - **Synchronní**: Plná šipka s vyplněným hrotem. Volající čeká na dokončení.
    - **Asynchronní**: Šipka s otevřeným hrotem. Volající pokračuje v práci.
    - **Návratová hodnota**: Přerušovaná šipka směrem zpět.

![[imgs/06.prednaska-051.jpg|x250]] ![[imgs/06.prednaska-053.jpg|x250]]
*Obrázek: Základní notace zpráv a způsoby zápisu návratových hodnot.*

- **Aktivace (Execution Specification)**: Úzký svislý obdélník na životní čáře značící, že objekt právě vykonává nějakou metodu.

## Pokročilé prvky
- **Vytvoření/Zrušení objektu**: Zpráva `«create»` končí u nového objektu. Zrušení se značí křížkem `X` na konci životní čáry (zpráva `«destroy»`).
- **Nalezená a vlastní zpráva**:
    - **Nalezená zpráva (Found Message)**: Šipka vycházející z černého bodu (vstup do systému zvenčí).
    - **Zaslání zprávy sám sobě (Self Message)**: Smyčka zpět na stejnou životní čáru (volání vnitřní metody).

![[imgs/06.prednaska-055.jpg|x200]] ![[imgs/06.prednaska-057.jpg|x200]]
*Obrázek: Modelování životního cyklu objektů a specifických typů zpráv.*

- **Fragmenty (Kombinované fragmenty)**: Rámečky pro řízení toku:
    - `alt`: Větvení (if-then-else).
    - `loop`: Cyklus (pro iteraci přes prvky kolekce).
    - `opt`: Volitelná část.
    - `par`: Paralelní běh.

![[imgs/06.prednaska-059.jpg|x200]]
*Obrázek: Ukázka fragmentů pro větvení (alt) a cykly (loop).*

## Komplexní příklad
Sekvenční diagramy se využívají k detailnímu návrhu realizace konkrétních scénářů, kde je vidět spolupráce mezi business objekty a změny jejich stavů.

![[imgs/06.prednaska-061.jpg|x250]]
*Obrázek: Realizace scénáře vypůjčení knihy zahrnující delegování zodpovědnosti a změnu stavu.*

## Význam v návrhu
Sekvenční diagramy pomáhají přiřazovat zodpovědnosti třídám (určují metody). Při jejich tvorbě se uplatňují principy [[navrhovy-model-trid|GRASP]].

## Související stránky
- [[navrhovy-model-trid]]
- [[pripady-uziti]]
- [[navrh-softwaru]]

---
#uml #sequence-diagram #behavior #navrh #BI-SWI
