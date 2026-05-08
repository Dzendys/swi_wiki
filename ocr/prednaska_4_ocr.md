# Analýza obrázků - Přednáška 4: Analýza problémové domény

Tento dokument obsahuje popis obrázků s prefixem `04.prednaska` získaných z podkladů k přednášce. Popisy jsou doplněny o kontext z odpovídajících slidů PDF prezentace zaměřených na analytický doménový model a modelování stavů entit.

## Přehled diagramů a schémat

### 04.prednaska-010.jpg (Slide 5)
**Téma:** Notace UML třídy
**Popis:** Detailní pohled na notaci třídy v UML.
- Horní část: Název třídy (**Název**).
- Prostřední část: Atributy s vyznačením viditelnosti (`- atribut1: int`, `+ atribut2: char`).
- Dolní část: Metoda s parametry a návratovým typem (`+ metoda(char): byte`).

### 04.prednaska-012.jpg (Slide 6)
**Téma:** Typy vztahů v UML
**Popis:** Přehled základních typů vazeb mezi třídami:
- **Asociace:** Plná čára se směrovou šipkou a násobností `0..*`.
- **Kompozice:** Plná čára s plným kosočtvercem u "celku" (násobnost `1` vs `0..*`).
- **Agregace:** Plná čára s prázdným kosočtvercem u "celku".
- **Generalizace / Dědičnost:** Čára s prázdnou trojúhelníkovou šipkou směřující k nadřazené třídě.

### 04.prednaska-014.jpg (Slide 7)
**Téma:** Atribut vs. Asociace
**Popis:** Porovnání dvou způsobů modelování stejné informace.
1. Atribut `adresa: Adresa` přímo uvnitř třídy `Dům`.
2. Samostatná třída `Adresa` spojená s třídou `Dům` pomocí asociace. Druhý způsob je v doménovém modelu považován za názornější.

### 04.prednaska-016.jpg (Slide 8)
**Téma:** Asociační třída
**Popis:** Znázornění asociační třídy `C`, která je napojena čárkovanou čarou na vztah mezi třídami `A` a `B`. Používá se pro zachycení informací, které patří k samotné vazbě.

### 04.prednaska-022.jpg (Slide 15)
**Téma:** Tvorba doménového modelu - Kniha a Autor
**Popis:** První krok refaktoringu doménového modelu. Místo atributů jména autora v třídě `Kniha` (viz Slide 13/14) je vytvořena samostatná třída `Autor` se vztahem "je napsána" (násobnost `1..*` na obou stranách).

### 04.prednaska-024.jpg & 04.prednaska-026.jpg (Slide 16/17)
**Téma:** Modelování výpůjček - Nevhodná varianta
**Popis:** Pokus o modelování výpůjčky přímou vazbou mezi `Kniha` a `Ctenar` ("je půjčena").
- **Nevýhoda:** Nelze takto sledovat historii výpůjček, pouze aktuální stav.

### 04.prednaska-028.jpg (Slide 18)
**Téma:** Modelování výpůjček - Lepší řešení
**Popis:** Zavedení nové třídy `Vypujcka`, která stojí mezi `Kniha` a `Ctenar`. Třída obsahuje atributy `od`, `do`, `vracena`, což umožňuje evidovat historii i detaily každé výpůjčky.

### 04.prednaska-030.jpg (Slide 20)
**Téma:** Rozlišení pojmů Kniha a Výtisk
**Popis:** Finální struktura modelu, kde je `Kniha` (obecný popis) oddělena od třídy `Vytisk` (fyzický exemplář s `evidencniCislo`). `Vytisk` je pak ten objekt, který se skutečně půjčuje (vazba na `Vypujcka`).

### 04.prednaska-032.jpg (Slide 21)
**Téma:** Komplexní doménový model knihovny
**Popis:** Celkový pohled na analytický model zahrnující entity: `Vytisk`, `Kniha`, `Autor`, `Rezervace`, `Vypujcka`, `Ctenar` a jejich vzájemné vazby a násobnosti.

### 04.prednaska-035.jpg (Slide 25)
**Téma:** Stavový diagram (State Machine)
**Popis:** Životní cyklus entity `Vytisk`:
- Počáteční stav -> **Volný**.
- Přechod **Vypůjčený** (při žádosti o výpůjčku).
- Přechod **Ztracený** (při nahlášení ztráty).
- Přechod **Vyřazený** (při poškození zjištěném kontrolou).

### 04.prednaska-042.jpg (Slide 28)
**Téma:** Chyby v DM - Implementační detaily
**Popis:** Ukázka chyby, kdy třída `Kniha` obsahuje atributy (`rowid`) a metody (`print()`), které jsou specifické pro implementaci/programování, nikoliv pro pochopení problémové domény.

### 04.prednaska-046.jpg (Slide 29)
**Téma:** Chyby v DM - Softwarové třídy
**Popis:** Přeškrtnutá třída `DatabazeKnih` s metodou `backup()`. Doménový model by neměl obsahovat technické/softwarové třídy, ale pouze objekty z reálného světa.

### 04.prednaska-048.jpg (Slide 30)
**Téma:** Chyby v DM - Cizí klíče
**Popis:** Ukázka nevhodného použití atributu `cisloFaktury` v třídě `Kniha` pro identifikaci jiné entity. Správně má být tento "cizí klíč" nahrazen asociací na třídu `Faktura`.

### 04.prednaska-050.jpg (Slide 31)
**Téma:** Chyby v DM - Míchání instance a popisu
**Popis:** Ukázka nevhodné třídy, která kombinuje atributy fyzické instance (`evidencniCislo`, `stav`) s atributy obecného popisu (`nazev`, `isbn`). Správným řešením je rozdělení na dvě třídy (viz Slide 20).

### 04.prednaska-052.jpg (Slide 32)
**Téma:** Chyby v DM - Nevhodná dědičnost (Kategorie)
**Popis:** Přeškrtnutý diagram, kde `Kniha` je nadřazenou třídou pro `Detektivka`, `Sci-fi` a `Beletrie`. Nevhodné, pokud kniha může patřit do více kategorií nebo měnit typ.

### 04.prednaska-054.jpg (Slide 33)
**Téma:** Správné modelování kategorií
**Popis:** Místo dědičnosti je použita samostatná třída `Žánr` spojená s třídou `Kniha` asociací. Toto řešení je flexibilnější.

### 04.prednaska-056.jpg (Slide 34)
**Téma:** Chyby v DM - Historie jako entita
**Popis:** Přeškrtnutý diagram, kde třída `Produkt` má vazbu na třídu `Historie`. Historie sama o sobě není entita, je to vlastnost vznikající uchováváním údajů v čase.

### 04.prednaska-058.jpg (Slide 35)
**Téma:** Správné zachycení historie (Cena)
**Popis:** Korektní způsob modelování historie ceny. Třída `Produkt` je spojena s třídou `Cena`, která obsahuje časové rozmezí (`od`, `do`) a hodnotu.
