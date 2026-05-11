# Analýza obrázků - Přednáška 4: Analýza problémové domény (OPRAVENO)

Tento dokument obsahuje opravený popis obrázků s prefixem `04.prednaska` na základě PDF prezentace.

## Přehled diagramů a schémat

### 04.prednaska-010.jpg (Slide 5)
**Téma:** Notace UML třídy
**Popis:** Detailní pohled na notaci třídy v UML (Název, atributy: název:typ, metody).

### 04.prednaska-012.jpg (Slide 6)
**Téma:** Typy vztahů v UML
**Popis:** Přehled vazeb: Asociace, Kompozice, Agregace, Generalizace.

### 04.prednaska-014.jpg (Slide 7)
**Téma:** Atribut vs. Asociace
**Popis:** Porovnání modelování adresy jako atributu ve třídě Dům vs. samostatné třídy Adresa s asociací.

### 04.prednaska-016.jpg (Slide 8)
**Téma:** Asociační třída
**Popis:** Třída C napojená na vztah mezi A a B.

### 04.prednaska-022.jpg & 04.prednaska-024.jpg (Slide 13/14)
**Téma:** První návrh DM - Kniha
**Popis:** Třída `Kniha` s autorem modelovaným pomocí atributů `autorJmeno` a `autorPrijmeni`.
- **Chyba:** Duplikace informací, nelze mít více autorů.

### 04.prednaska-026.jpg (Slide 15)
**Téma:** Řešení - Nová třída Autor
**Popis:** Vyčlenění třídy `Autor` a propojení s `Kniha` pomocí asociace "je napsána" (násobnost `1..*` na obou stranách).

### 04.prednaska-028.jpg & 04.prednaska-030.jpg (Slide 16/17)
**Téma:** Sledování výpůjček - 1. varianta
**Popis:** Přidání třídy `Ctenar` a přímé vazby "je půjčena" k `Kniha`.
- **Chyba:** Nelze sledovat historii výpůjček.

### 04.prednaska-032.jpg (Slide 18)
**Téma:** Sledování výpůjček - Lepší řešení
**Popis:** Zavedení vazební třídy `Vypujcka` mezi `Kniha` a `Ctenar` s atributy `od`, `do`, `vracena`.

### 04.prednaska-035.jpg (Slide 20)
**Téma:** Rozlišení pojmů Kniha a Výtisk
**Popis:** Rozdělení na `Kniha` (popis) a `Vytisk` (instance s `evidencniCislo`). Výpůjčka se nyní týká `Výtisku`.

### 04.prednaska-037.jpg (Slide 21)
**Téma:** Komplexní doménový model knihovny
**Popis:** Finální analytický model zahrnující entity: `Vytisk`, `Kniha`, `Autor`, `Rezervace`, `Vypujcka`, `Ctenar`.

### 04.prednaska-042.jpg (Slide 28)
**Téma:** Chyby v DM - Implementační detaily
**Popis:** Třída `Kniha` s technickým atributem `rowid` a metodou `print()`.

### 04.prednaska-046.jpg (Slide 29)
**Téma:** Chyby v DM - Softwarové třídy
**Popis:** Přeškrtnutá technická třída `DatabazeKnih`.

### 04.prednaska-048.jpg (Slide 30)
**Téma:** Chyby v DM - Cizí klíče
**Popis:** Třída `Kniha` obsahující `cisloFaktury` místo asociace na třídu `Faktura`.

### 04.prednaska-050.jpg (Slide 31)
**Téma:** Chyby v DM - Míchání instance a popisu
**Popis:** Třída `Kniha` kombinující atributy popisu (`isbn`) a instance (`evidencniCislo`, `stav`).

### 04.prednaska-052.jpg (Slide 32)
**Téma:** Chyby v DM - Nevhodná dědičnost (Kategorie)
**Popis:** Přeškrtnutá dědičnost `Detektivka`, `Sci-fi` z `Kniha`.

### 04.prednaska-054.jpg (Slide 33)
**Téma:** Správné modelování kategorií
**Popis:** Použití asociace na třídu `Žánr`.

### 04.prednaska-056.jpg (Slide 34)
**Téma:** Chyby v DM - Historie jako entita
**Popis:** Přeškrtnutá vazba `Produkt` -> `Historie`.

### 04.prednaska-058.jpg (Slide 35)
**Téma:** Správné zachycení historie (Cena)
**Popis:** Třída `Produkt` spojená s třídou `Cena` (atributy `od`, `do`).

### 04.prednaska-060.jpg (Slide 37)
**Téma:** Shrnutí - Co víme
**Popis:** Seznam výstupů: Business proces model, Specifikace požadavků, Analytický doménový model, Stavový diagram.
