# Sekvenční diagram (UML)

**Shrnutí**: Interakční diagram v UML, který zobrazuje spolupráci objektů v čase. Slouží k modelování realizace scénářů případů užití.

**Zdroje**:

- `raw/lectures/06.prednaska.pdf`



---

Sekvenční diagram (Sequence Diagram) patří mezi diagramy chování a je klíčový pro fázi [[navrh-softwaru|návrhu]]. Zatímco [[navrhovy-model-trid|diagram tříd]] zachycuje statickou strukturu, sekvenční diagram ukazuje, jak si objekty v čase vyměňují zprávy, aby splnily konkrétní úkol (scénář z [[pripady-uziti|případu užití]]).

## Základní notace

- **Životní čára (Lifeline)**: Svislá čárkovaná čára pod objektem.
- **Objekt**: Obdélník na vrcholu čáry. Zápis: `názevObjektu : Třída` (pojmenovaný) nebo `: Třída` (anonymní).
- **Zpráva (Message)**: Vodorovná šipka mezi životními čárami.
    - **Synchronní**: Plná šipka s vyplněným hrotem. Volající čeká na dokončení.
    - **Asynchronní**: Šipka s otevřeným hrotem. Volající pokračuje v práci.
    - **Návratová hodnota**: Přerušovaná šipka směrem zpět.

![[imgs/06.prednaska-051.jpg|415]] ![[imgs/06.prednaska-053.jpg|400]]

*Obrázek: Základní notace zpráv a způsoby zápisu návratových hodnot.*

- **Aktivace (Execution Specification)**: Úzký svislý obdélník na životní čáře značící, že objekt právě vykonává nějakou metodu.

## Pokročilé prvky

- **Vytvoření a zrušení objektu**: Zpráva se stereotypem `«create»` míří přímo na hlavičku nového objektu. Zrušení instance (např. uvolnění z paměti) se značí křížkem `X` na konci životní čáry, kam míří zpráva `«destroy»`.

    ![[imgs/06.prednaska-055.jpg|350]]


- **Nalezená a vlastní zpráva**:
    - **Nalezená zpráva (Found Message)**: Šipka vycházející z černého bodu reprezentuje vstup z vnějšího prostředí, který není v diagramu explicitně modelován.
    - **Zaslání zprávy sám sobě (Self Message)**: Smyčka zpět na stejnou životní čáru značí volání vnitřní metody daného objektu.

    ![[imgs/06.prednaska-057.jpg|250]]


- **Fragmenty (Kombinované fragmenty)**: Rámečky pro řízení toku:
    - `alt`: Větvení (if-then-else).
    - `loop`: Cyklus (pro iteraci přes prvky kolekce).
    - `opt`: Volitelná část.
    - `par`: Paralelní běh.

![[imgs/06.prednaska-059.jpg|244]]

*Obrázek: Ukázka fragmentů pro větvení (alt) a cykly (loop).*

## Komplexní příklad
Sekvenční diagramy se využívají k detailnímu návrhu realizace konkrétních scénářů, kde je vidět spolupráce mezi business objekty a změny jejich stavů.

![[imgs/06.prednaska-061.jpg|552]]

*Obrázek: Realizace scénáře vypůjčení knihy zahrnující delegování zodpovědnosti a změnu stavu.*

## Význam v návrhu
Sekvenční diagramy pomáhají přiřazovat zodpovědnosti třídám (určují metody). Při jejich tvorbě se uplatňují principy [[navrhovy-model-trid|GRASP]].

## Související stránky

- [[navrhovy-model-trid]]
- [[pripady-uziti]]
- [[navrh-softwaru]]

---
#uml #sequence-diagram #behavior #navrh #BI-SWI
