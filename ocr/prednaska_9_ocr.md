# Analýza obrázků - Přednáška 9: Zajištění kvality

Tento dokument obsahuje popis obrázků s prefixem `09.prednaska` získaných z podkladů k přednášce. Popisy se zaměřují na zajištění kvality, metriky testování a statickou analýzu kódu.

## Přehled diagramů a schémat

### 09.prednaska-012.jpg (Slide 7)
**Téma:** Cena opravy chyby (Cost-factor for fixing bugs)
**Popis:** Sloupcový graf ilustrující, jak exponenciálně roste cena opravy chyby v závislosti na fázi životního cyklu softwaru, kdy je odhalena:
- Fáze návrhu (Design): 1
- Implementace: 6,5
- Testování (Testing): 15
- Údržba/Produkce (Maintenance): 100

### 09.prednaska-022.jpg (Slide 16)
**Téma:** Výsledek statické analýzy kódu - Spolehlivost
**Popis:** Bodový graf (bublinový) z nástroje pro statickou analýzu s názvem "Reliability Overview".
- Osa X: Počet řádků kódu (Lines of Code).
- Osa Y: Úsilí na opravu (Reliability Remediation Effort).
- Velikost bubliny reprezentuje počet chyb (Bugs) a barva označuje hodnocení spolehlivosti (Reliability Rating od A do E). Ukazuje, které části kódu jsou nejvíce problematické.

### 09.prednaska-023.jpg (Slide 16)
**Téma:** Výsledek statické analýzy kódu - Udržovatelnost
**Popis:** Bodový graf s názvem "Maintainability Overview".
- Osa X: Počet řádků kódu (Lines of Code).
- Osa Y: Technický dluh (Technical Debt).
- Velikost bubliny představuje množství "Code Smells" (zápachů v kódu) a barva ukazuje hodnocení udržovatelnosti (Maintainability Rating od A do E).

### 09.prednaska-041.jpg (Slide 33)
**Téma:** Vývoj testů v čase
**Popis:** Plošný graf "Test Result Trend" znázorňující vývoj výsledků testování v čase (jednotlivá sestavení/buildy na ose X). Modrá plocha představuje celkový počet testů, červená plocha ve spodní části ukazuje podíl selhávajících testů.

### 09.prednaska-042.jpg (Slide 33)
**Téma:** Vývoj pokrytí kódu v čase
**Popis:** Čárový graf "Cobertura Coverage Report - Trend" ukazující vývoj procentuálního pokrytí kódu v čase (na ose X jsou čísla buildů). Zobrazuje oddělené křivky pro pokrytí tříd (Classes), podmínek (Conditionals), souborů (Files), řádků (Lines), metod (Methods) a balíčků (Packages).

### 09.prednaska-044.jpg (Slide 34)
**Téma:** Celkový přehled pokrytí kódu
**Popis:** Panel se souhrnnými statistikami z analytického nástroje (např. SonarQube).
- Ukazuje, že celkové pokrytí kódu (Coverage na novém kódu) je 84,3 %.
- Line Coverage je 94,7 % a Condition Coverage je 58,7 %.
- Dále ukazuje počty testů (Unit Tests: 257), chyby, selhání a úspěšnost testů (100 %).

### 09.prednaska-045.jpg (Slide 34)
**Téma:** Detailní pokrytí a složitost
**Popis:** Bublinový graf "Coverage Overview".
- Osa X: Cyklomatická složitost (Cyclomatic Complexity).
- Osa Y: Procento pokrytí kódu testy (Coverage).
- Velikost bubliny je dána počtem nepokrytých řádků (Uncovered Lines). Graf pomáhá identifikovat složité části kódu, které nejsou dostatečně otestovány (bubliny v pravé dolní části).
