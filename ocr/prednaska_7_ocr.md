# Analýza obrázků - Přednáška 7: Návrhové vzory, komponenty

Tento dokument obsahuje popis obrázků s prefixem `07.prednaska` získaných z podkladů k přednášce. Popisy se zaměřují na komponenty, rozhraní a návrhové vzory z rodiny GoF (Gang of Four).

## Přehled diagramů a schémat

### 07.prednaska-011.jpg (Slide 6)
**Téma:** Základní notace komponenty a rozhraní
**Popis:** Ukázka UML diagramu komponent. Zobrazuje obdélník s ikonou komponenty v pravém horním rohu s názvem `Komponenta` a samostatný obdélník pro rozhraní (s označením stereotypu `«interface»` a názvem `Rozhraní`), který obsahuje definice metod `metoda1` a `metoda2`.

### 07.prednaska-013.jpg (Slide 7)
**Téma:** Typy rozhraní komponent
**Popis:** Zobrazení různých vazeb rozhraní na komponenty:
- `Komponenta A` poskytuje "nabízené" rozhraní (znázorněno jako plné kolečko na lince - lollypop notace).
- `Komponenta B` má "vyžadované" rozhraní (znázorněno jako půlkruh/kapsička).
- `Komponenta C` a `Komponenta D` ukazují sestavení (assembly), kde vyžadované rozhraní jedné komponenty zapadá do nabízeného rozhraní druhé.

### 07.prednaska-015.jpg (Slide 8)
**Téma:** Implementace rozhraní třídou
**Popis:** UML diagram ukazující vztah realizace (přerušovaná čára s prázdnou šipkou) mezi konkrétní `Třída` a rozhraním `«interface» Rozhraní`.

### 07.prednaska-017.jpg (Slide 9)
**Téma:** Architektura s komponentami a rozhraními
**Popis:** Komplexní diagram komponent ilustrující propojení prezentační a logické vrstvy přes rozhraní. Komponenty `REST API` a `GUI` přes vyžadovaná rozhraní komunikují s nabízenými rozhraními `IZpracovaniVypujckyController` a `IViewVypujckyController`, které jsou implementovány nad komponentami `Knihy` a `Vypujcky`. Mezi komponentami `Knihy` a `Vypujcky` je také definována závislost přes rozhraní `IKniha`.

### 07.prednaska-019.jpg (Slide 10)
**Téma:** Detail specifikace rozhraní Controllerů
**Popis:** UML reprezentace dvou rozhraní pro komponentu výpůjček:
- `vypujcky::IViewVypujckyController`: rozhraní pro pohled (GUI), obsahující metody pro přidání/odebrání pohledu a získání volných či vypůjčených výtisků.
- `vypujcky::IZpracovaniVypujckyController`: rozhraní pro zpracování logiky výpůjček, s metodami pro zápis knihy, přihlášení/odhlášení čtenáře a získání aktivních výpůjček.

### 07.prednaska-022.jpg (Slide 12)
**Téma:** Propojení komponent pomocí rozhraní (IoC princip)
**Popis:** Diagram tříd ukazující závislost třídy `vypujcky::SpravceCtenaru` na abstraktním rozhraní `dao::ICtenarDAO` namísto konkrétní implementace. Spojení je znázorněno orientovanou asociací s rolí `-ctenarDAO`.

### 07.prednaska-031.jpg (Slide 20)
**Téma:** GoF vzor: Abstraktní továrna (Abstract Factory)
**Popis:** Kompletní UML diagram vzoru Abstract Factory. Klient závisí pouze na abstraktních rozhraních (`AbstractFactory`, `AbstractProductA`, `AbstractProductB`). Konkrétní továrny (`ConcreteFactory1`, `ConcreteFactory2`) pak generují odpovídající rodiny konkrétních produktů (`ProductA1/B1` vs `ProductA2/B2`), aniž by o nich klient musel znát detaily.

### 07.prednaska-035.jpg (Slide 23)
**Téma:** GoF vzor: Stavitel (Builder)
**Popis:** Diagram ilustrující návrhový vzor Stavitel na příkladu generování SQL. Řídící třída (`Director`) používá rozhraní `SqlBuilder` pro stavbu SQL dotazu krok za krokem. Konkrétní implementace (např. `OracleBuilder`, `MSSQLBuilder`, `PostgreSQLBuilder`) řeší specifika daného dialektu SQL.

### 07.prednaska-038.jpg (Slide 25)
**Téma:** GoF vzor: Stav (State) - Koncept
**Popis:** Základní struktura vzoru State. `StavováTřída` udržuje referenci na abstraktní `Stav` a deleguje na něj chování (např. metodu `Zpracuj()`). Abstraktní `Stav` je pak implementován konkrétními stavy `Stav A` a `Stav B`. Umožňuje to snadné přidávání nových stavů bez nutnosti měnit `StavovouTřídu`.

### 07.prednaska-040.jpg (Slide 26)
**Téma:** GoF vzor: Stav (State) - Aplikace na výpůjčky
**Popis:** Aplikace vzoru State na doménu knihovny. Třída `VytiskBO` udržuje aktuální stav (`Stav`). Rozhraní stavu je definováno abstraktní třídou `Stav`, která obsahuje konstanty pro dostupné stavy (`VOLNY`, `VYPUJCENY`). Konkrétní chování implementují třídy `StavVolny` a `StavVypujcen`.

### 07.prednaska-042.jpg (Slide 27)
**Téma:** Vzor State v akci - Výtisk není vypůjčen
**Popis:** Sekvenční diagram pro operaci výpůjčky, když je kniha volná. `VytiskBO` deleguje metodu `zpracuj` na aktuální stav `:StavVolny`. Ten následně volá zapsání výpůjčky do `KnihaVypujcek`, vytvoří instanci `Vypujcka`, nastaví v ní potřebné vazby a na konci změní stav výtisku na `Stav.VYPUJCENY`.

### 07.prednaska-044.jpg (Slide 28)
**Téma:** Vzor State v akci - Výtisk je vypůjčen
**Popis:** Sekvenční diagram pro operaci vrácení výtisku. Metoda `zpracuj` je volána na `VytiskBO`, který ji deleguje na aktuální stav `:StavVypujcen`. Ten ukončí výpůjčku v `KnihaVypujcek`, nastaví datum vrácení a přepne stav výtisku zpět na `Stav.VOLNY`.

### 07.prednaska-048.jpg (Slide 31)
**Téma:** GoF vzor: Adaptér (Adapter)
**Popis:** UML diagram vzoru Adaptér. `Klient` vyžaduje určité rozhraní, které poskytuje `PoužívanáTřída`. Protože existující `PřizpůsobenáTřída` má nekompatibilní rozhraní (`SpecifickýPožadavek()`), je vytvořen `Adapter`, který dědí z `PoužívanéTřídy` a uvnitř metody `Požadavek()` volá metodu z `PřizpůsobenéTřídy`, čímž obě rozhraní propojí.
