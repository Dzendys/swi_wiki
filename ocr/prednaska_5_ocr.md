# Analýza obrázků - Přednáška 5: Návrhové modely a implementace

Tento dokument obsahuje popis obrázků s prefixem `05.prednaska` získaných z podkladů k přednášce. Popisy se zaměřují na UML diagramy, datové modely a jejich transformaci do implementace.

## Přehled diagramů a schémat

### 05.prednaska-023.jpg (Slide 18)
**Téma:** UML Datový model - Entita Kniha
**Popis:** Detailní návrh tabulky/entity `Kniha` v databázovém schématu.
- **Atributy:** `nazev` (VARCHAR), `isbn` (VARCHAR, PK), `rokVydani` (NUMERIC), `obsah` (TEXT), `klicovaSlova` (VARCHAR).
- **Klíče:** Primární klíč `knihaID`, cizí klíče `regalID` a `nakladatelstviID`.
- **Indexy/Omezení:** Unikátní index na ISBN.

### 05.prednaska-027.jpg (Slide 21)
**Téma:** Trasovatelnost (Traceability) - Od konceptu k databázi
**Popis:** Diagram ukazující vztah mezi konceptuálním modelem (Autor, Kniha) a jeho fyzickou realizací v databázi.
- Zahrnuje asociační tabulku `jeNapsana` pro řešení vztahu M:N mezi autorem a knihou.
- Používá stereotyp `«trace»` pro propojení modelů.

### 05.prednaska-030.jpg (Slide 23)
**Téma:** Balíčkování (Packages)
**Popis:** Rozdělení systému do logických balíčků:
- **Evidence knih:** Obsahuje entity jako Autor, Kniha, Nakladatelstvi, Regal, Zanr.
- **Evidence výpůjček:** Obsahuje entity Ctenar, Vypujcka, Vytisk, Rezervace, Pokuta.

### 05.prednaska-032.jpg (Slide 24)
**Téma:** UML Datový model - Výpůjčky a Čtenáři
**Popis:** Schéma vztahů mezi entitami `Ctenar`, `Vypujcka` a `Vytisk`.
- Ukazuje multiplicity (např. 1 čtenář může mít 0..* výpůjček).
- Definuje cizí klíče a propojení na evidenci knih přes `knihaID`.

### 05.prednaska-039.jpg (Slide 30)
**Téma:** Závislosti mezi balíčky - Jednosměrná závislost
**Popis:** Diagram balíčků zobrazující základní jednosměrnou závislost, kde Balíček A závisí na Balíčku B.

### 05.prednaska-041.jpg (Slide 31)
**Téma:** Závislosti mezi balíčky - Cyklická závislost
**Popis:** Diagram ilustrující problematickou obousměrnou (cyklickou) závislost mezi Balíčkem A a Balíčkem B, která komplikuje rozšiřitelnost.

### 05.prednaska-043.jpg (Slide 32)
**Téma:** Závislosti mezi balíčky - Řešení cyklických závislostí
**Popis:** Diagram znázorňující vyřešení cyklické závislosti vyčleněním tříd (nebo vytvořením rozhraní) do nového Balíčku C. Nyní Balíček A i Balíček B závisí na Balíčku C, čímž se cyklus odstraní.

### 05.prednaska-045.jpg (Slide 33)
**Téma:** Hierarchie a vnořování balíčků - Zobrazení pomocí ikon
**Popis:** Zobrazení vnoření, kde jsou vnitřní balíčky (Balíček B a Balíček C) reprezentovány ikonami složek přímo uvnitř jmenného prostoru Balíčku A.

### 05.prednaska-046.jpg (Slide 33)
**Téma:** Hierarchie a vnořování balíčků - Grafické vnoření
**Popis:** Klasické grafické vnoření (nesting) v UML diagramu, kde jsou obdélníky pro Balíček B a Balíček C nakresleny fyzicky uvnitř těla Balíčku A.

### 05.prednaska-047.jpg (Slide 33)
**Téma:** Hierarchie a vnořování balíčků - Kompoziční vazba
**Popis:** Zobrazení vnoření pomocí čar s křížkem v kroužku. Tato notace explicitně definuje členství (kompozici), kde Balíček A obsahuje Balíček B a Balíček C.

### 05.prednaska-053.jpg (Slide 38)
**Téma:** UML Notace tříd - Viditelnost a členy
**Popis:** Přehledná ukázka všech prvků třídy v UML v jedné tabulce:
- **Viditelnost:** public (+), protected (#), package (~), private (-).
- **Vlastnosti:** odvozené atributy (/), konstanty {readOnly}, kolekce {bag, ordered}.
- **Metody:** statické (podtržené), abstraktní (kurzíva), konstruktory (označené stereotypem `«constructor»`).

### 05.prednaska-055.jpg (Slide 39)
**Téma:** Šablony a Generika (Templates)
**Popis:** Ukázka parametrizované třídy `Seznam<T>` a její vazby pomocí stereotypu `«bind»` s argumentem `< T->Telefonní číslo >` do konkrétní implementace v třídě `Telefonní seznam`.

### 05.prednaska-057.jpg (Slide 40)
**Téma:** Reprezentace vztahů - Třída s atributem
**Popis:** Modelování vztahu zapsané přímo formou atributu třídy. Třída `Test` má atribut `vyplnil` typu `Student` s multiplicitou `[0..1]`.

### 05.prednaska-058.jpg (Slide 40)
**Téma:** Reprezentace vztahů - Grafická asociace
**Popis:** Alternativní grafická reprezentace stejného vztahu jako v předchozím případě. Třídy `Test` a `Student` jsou propojeny orientovanou asociací (šipkou) s rolí `-vyplnil` a multiplicitami `0..*` a `0..1`.

### 05.prednaska-060.jpg (Slide 41)
**Téma:** Realizace rozhraní (Interface Realization)
**Popis:** Třída `Test` implementující rozhraní `ITest`. V UML je tento vztah naznačen přerušovanou čarou s prázdnou šipkou směrem k rozhraní.

### 05.prednaska-062.jpg (Slide 42)
**Téma:** Transformace z konceptu do implementace
**Popis:** Ukázka trasování (stereotyp `«trace»`) konceptuálních doménových tříd `Vytisk` a `Kniha` do jejich detailních Java/C# návrhových tříd, které implementují rozhraní `Serializable` a obsahují kompletní seznam private atributů a public get/set metod.

### 05.prednaska-064.jpg (Slide 43)
**Téma:** Implementace stavů (State Pattern / Constants) - Návrh
**Popis:** Návrh třídy `Stav`, která obsahuje statické instance sebe sama (konstanty `VOLNY` a `VYPUJCENY`), a abstraktní metodu `zpracuj`. Ukazuje i dědičnost na konkrétní stav `StavVolny`.

### 05.prednaska-066.jpg (Slide 44)
**Téma:** Implementace stavů (State Pattern / Constants) - Korekce chyb
**Popis:** Stejný diagram jako předchozí, avšak prezentovaný v kontextu se zdrojovým kódem. Je zde zdůrazněna oprava chyby ve viditelnosti u statických instancí stavů (změna z `private` na `public static`).

### 05.prednaska-073.jpg (Slide 50)
**Téma:** Návrhový vzor Builder - Základní abstrakce
**Popis:** Závislost `Client`a na rozhraní/třídě `SqlBuilder`. Rozhraní definuje abstraktní metody pro stavbu částí SQL skriptu, jako `createTable`, `dropTable` a `insertData`.

### 05.prednaska-076.jpg (Slide 52)
**Téma:** Návrhový vzor Builder - Konkrétní stavitelé
**Popis:** Rozšíření vzoru Builder o specializace pro konkrétní databáze. Třídy `OracleBuilder`, `MSSQLBuilder` a `PostgreSQLBuilder` implementují společné rozhraní `SqlBuilder`.

### 05.prednaska-079.jpg (Slide 54)
**Téma:** Návrhový vzor Builder - Využití abstraktního předka
**Popis:** Vložení třídy `AbstractSQLBuilder` mezi rozhraní `SqlBuilder` a konkrétní stavitele. Slouží ke sdílení společné logiky a zamezení duplikace kódu u metod, které se chovají pro různé databáze stejně, zatímco specifika se řeší až v potomcích.
