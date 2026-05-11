# Analýza obrázků - Přednáška 4: Analýza problémové domény (DEFINITIVNÍ VERZE)

Tento dokument obsahuje ověřený popis obrázků s prefixem `04.prednaska` na základě vizuální analýzy PDF prezentace.

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

### 04.prednaska-022.jpg (Slide 13)
**Téma:** Ukázka tvorby DM - První návrh
**Popis:** Třída `Kniha` s autorem jako atributy (`autorJmeno`, `autorPrijmeni`).

### 04.prednaska-024.jpg (Slide 14)
**Téma:** Ukázka tvorby DM - Nevýhody prvního návrhu
**Popis:** Stejný diagram jako 022, ale s textem vysvětlujícím nevýhody (duplikace, nelze více autorů).

### 04.prednaska-026.jpg (Slide 15)
**Téma:** Ukázka tvorby DM - Řešení (Nová třída Autor)
**Popis:** Vyčlenění třídy `Autor` a propojení s `Kniha` pomocí asociace "je napsána".

### 04.prednaska-028.jpg (Slide 16)
**Téma:** Sledování výpůjček - 1. varianta
**Popis:** Přímá vazba "je půjčena" mezi `Kniha` a `Ctenar`.

### 04.prednaska-030.jpg (Slide 17)
**Téma:** Sledování výpůjček - Nevýhody 1. varianty
**Popis:** Stejný diagram jako 028, ale s textem (nelze sledovat historii).

### 04.prednaska-032.jpg (Slide 18)
**Téma:** Sledování výpůjček - Lepší řešení (Vazební třída)
**Popis:** Zavedení třídy `Vypujcka` mezi `Kniha` a `Ctenar`.

### 04.prednaska-035.jpg (Slide 20)
**Téma:** Rozlišení pojmů Kniha a Výtisk
**Popis:** Finální model oddělující `Kniha` (popis) a `Vytisk` (instance). Výpůjčka vede na `Vytisk`.

### 04.prednaska-037.jpg (Slide 21)
**Téma:** Komplexní doménový model knihovny
**Popis:** Celkový pohled zahrnující Rezervace, Výpůjčky, Čtenáře, Knihy, Výtisky a Autory.

### 04.prednaska-042.jpg (Slide 25)
**Téma:** Stavový diagram (State Machine)
**Popis:** Životní cyklus entity `Výtisk` (stavy: Volný, Vypůjčený, Ztracený, Vyřazený).

### 04.prednaska-046.jpg (Slide 28)
**Téma:** Chyby v DM - Implementační detaily
**Popis:** Třída `Kniha` s technickým atributem `rowid` a metodou `print()`.

### 04.prednaska-048.jpg (Slide 29)
**Téma:** Chyby v DM - Softwarové třídy
**Popis:** Přeškrtnutá technická třída `DatabazeKnih`.

### 04.prednaska-050.jpg (Slide 30)
**Téma:** Chyby v DM - Cizí klíče
**Popis:** Třída `Kniha` obsahující `cisloFaktury` místo asociace na třídu `Faktura`.

### 04.prednaska-052.jpg (Slide 31)
**Téma:** Chyby v DM - Míchání instance a popisu
**Popis:** Třída `Kniha` kombinující atributy popisu (`isbn`) a instance (`evidencniCislo`).

### 04.prednaska-054.jpg (Slide 32)
**Téma:** Chyby v DM - Nevhodná dědičnost (Kategorie)
**Popis:** Přeškrtnutá dědičnost žánrů z třídy `Kniha`.

### 04.prednaska-056.jpg (Slide 33)
**Téma:** Správné použití dědičnosti / asociace pro kategorie
**Popis:** Modelování žánrů pomocí asociace na třídu `Žánr`.

### 04.prednaska-058.jpg (Slide 34)
**Téma:** Chyby v DM - Historie jako entita
**Popis:** Přeškrtnutá vazba `Produkt` -> `Historie`.

### 04.prednaska-060.jpg (Slide 35)
**Téma:** Správné zachycení historie (Cena)
**Popis:** Modelování historie ceny pomocí třídy `Cena` s atributy `od`, `do`.
