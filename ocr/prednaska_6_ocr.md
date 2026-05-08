# Analýza obrázků - Přednáška 6: Architektonické vzory

Tento dokument obsahuje popis obrázků s prefixem `06.prednaska` získaných z podkladů k přednášce. Popisy se zaměřují na vícevrstvé architektury, persistenci dat a sekvenční diagramy.

## Přehled diagramů a schémat

### 06.prednaska-023.jpg (Slide 18)
**Téma:** Třívrstvá architektura - Striktní varianta
**Popis:** Schéma zobrazující striktní vrstvení (Prezentační -> Business -> Datová). V této variantě je povolena závislost pouze na bezprostředně nižší vrstvě. Balíček Prezentační závisí na Business a Business na Datové.

### 06.prednaska-025.jpg (Slide 19)
**Téma:** Třívrstvá architektura - Relaxovaná varianta
**Popis:** Schéma relaxovaného vrstvení, které je v praxi nejčastěji používané. Vyšší vrstvy mohou záviset na jakékoliv nižší vrstvě (např. Prezentační vrstva může přímo přistupovat k Datové vrstvě, pokud je to účelné).

### 06.prednaska-033.jpg (Slide 26)
**Téma:** Persistence dat - Table Data Gateway
**Popis:** Detail třídy `Kniha Gateway`, která zapouzdřuje veškerý přístup k tabulce v databázi. Obsahuje metody pro CRUD operace: `najdi(isbn)`, `smaz(isbn)`, `uprav(...)` a `vytvoř(...)`.

### 06.prednaska-035.jpg (Slide 27)
**Téma:** Persistence dat - Row Data Gateway
**Popis:** Modelování vzoru Row Data Gateway, kde jedna instance třídy `Kniha` odpovídá jednomu řádku v tabulce. Pro vyhledávání instancí se používá pomocná třída `Vyhledávač knih` s metodami jako `najdiFulltext(text)` nebo `najdiPodleISBN(isbn)`.

### 06.prednaska-037.jpg (Slide 28)
**Téma:** Persistence dat - Row Data Gateway (Modifikace)
**Popis:** Varianta vzoru Row Data Gateway, kde jsou vyhledávací metody (např. `najdiFulltext`) umístěny přímo ve třídě `Kniha` jako statické metody. Dokumentace uvádí, že jde o méně vhodné řešení z hlediska testovatelnosti (IoC).

### 06.prednaska-039.jpg (Slide 29)
**Téma:** Persistence dat - Active Record
**Popis:** Ukázka vzoru Active Record, který je obdobou Row Data Gateway, ale navíc do třídy `Kniha` přidává business logiku (např. metodu `zjistiPopularitu()`). Tento vzor typicky porušuje zásady striktní třívrstvé architektury.

### 06.prednaska-041.jpg (Slide 30)
**Téma:** Persistence dat - Data Mapper
**Popis:** Schéma vzoru Data Mapper, který odděluje paměťovou reprezentaci objektů od databázového schématu. Třída `Kniha Mapper` zajišťuje přenos dat mezi objektem `Kniha` a databází, což umožňuje komplexní mapování (dědičnost, kolekce).

### 06.prednaska-051.jpg (Slide 39)
**Téma:** Spolupráce objektů - Sekvenční diagram (Základy)
**Popis:** Ukázka základní notace sekvenčního diagramu zobrazující interakci mezi objekty `:Třída B` a `Objekt A:Třída A`. Rozlišuje mezi asynchronní zprávou (otevřená šipka) a synchronní zprávou (plná šipka) včetně návratové hodnoty (přerušovaná šipka).

### 06.prednaska-053.jpg (Slide 40)
**Téma:** Spolupráce objektů - Návratová hodnota
**Popis:** Dva způsoby zápisu návratové hodnoty v sekvenčním diagramu: buď jako explicitní přiřazení k proměnné u volání zprávy (`výsledek = zprava()`), nebo jako samostatná návratová šipka s popiskem `výsledek`.

### 06.prednaska-055.jpg (Slide 41)
**Téma:** Spolupráce objektů - Životní cyklus objektu
**Popis:** Notace pro vytvoření a zrušení objektu v sekvenčním diagramu. Zpráva se stereotypem `«create»` míří na hlavičku nového objektu, zatímco stereotyp `«destroy»` a symbol "X" na konci životní čáry značí smazání instance.

### 06.prednaska-057.jpg (Slide 42)
**Téma:** Spolupráce objektů - Nalezená a vlastní zpráva
**Popis:** Zobrazení "nalezené zprávy" (Found Message), která přichází z vnějšího prostředí (černý puntík), a "vlastní zprávy" (Self Message), kdy objekt `:Třída B` volá svou vlastní metodu `metodaB2()`.

### 06.prednaska-059.jpg (Slide 43)
**Téma:** Spolupráce objektů - Kombinované fragmenty
**Popis:** Ukázka fragmentů pro řízení toku v sekvenčním diagramu: `alt` pro větvení (podmínky `[a>b]`, `[a<=b]`), `loop` pro cykly a iteraci přes prvky kolekce.

### 06.prednaska-061.jpg (Slide 44)
**Téma:** Spolupráce objektů - Scénář Vypůjčení výtisku
**Popis:** Komplexní sekvenční diagram realizující scénář vypůjčení knihy. Zahrnuje interakci mezi objekty `vytisk: VytiskBO`, `:StavVolny`, `knihavypujcek: KnihaVypujcek` a vytvoření nové instance `vypujcka: Vypujcka`. Ukazuje delegování odpovědnosti a změnu stavu objektu.
