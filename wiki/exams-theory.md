# Teoretické otázky ze zkoušek

Tento přehled obsahuje syntézu teoretických otázek, které se objevily v minulých zkouškových termínech. Otázky jsou sjednoceny podle témat a doplněny o klíčové body pro úspěšné zodpovězení.

---

## 1. Procesy a Metodiky

### Fáze Unified Process (UP)

**Otázka**: Vyjmenujte 4 fáze Unified procesu.

**Odpověď**:

1.  **Inception (Zahájení)**: Definice rozsahu projektu, hrubé odhady a ověření proveditelnosti.
2.  **Elaboration (Rozpracování)**: Detailní analýza požadavků, návrh a stabilizace architektury a zmírnění hlavních rizik.
3.  **Construction (Konstrukce)**: Kompletní implementace zbývajících funkcí a jejich testování.
4.  **Transition (Dodání)**: Nasazení systému u uživatelů, beta testování, školení a opravy drobných chyb.

**Výskyt**: `18. 5. 2012`, `29. 5. 2018`

**Související koncepty**: [[unified-process|Unified Process (UP)]]

---

### Fáze a činnosti SCRUM

**Otázka**: Vyjmenujte fáze projektu dle metodiky SCRUM a popište typické činnosti v nich vykonávané.

**Odpověď**:

- **Předehra (Prelude)**: Plánování, sestavení úvodního Product Backlogu a hrubý návrh architektury.
- **Hra (Play)**: Samotný vývoj probíhající v iteracích (sprintech), které zahrnují plánování, každodenní schůzky a review.
- **Dohra (Post-game)**: Finální integrace, akceptační testy se zákazníkem a příprava dokumentace k nasazení.

**Výskyt**: `12. 6. 2018`, `6. 6. 2019`, `27. 1. 2021`

**Související koncepty**: [[scrum|metodice SCRUM]]

---

### Praktiky Extrémního programování (XP)

**Otázka**: Uveďte alespoň 6 typických praktik nebo charakteristik Extrémního programování.

**Odpověď**:

- **Párové programování**: Dva vývojáři pracují společně u jednoho stroje.
- **Test Driven Development (TDD)**: Psaní unit testů před samotným kódem.
- **Průběžná integrace (CI)**: Časté začleňování změn do hlavní větve kódu.
- **Malá vydání**: Časté dodávky fungujícího, ale menšího kusu softwaru.
- **Jednoduchý návrh**: Implementace pouze toho, co je aktuálně potřeba (YAGNI).
- **Zákazník na místě**: Neustálá přítomnost a dostupnost zástupce zákazníka pro konzultace.
- **Refaktoring**: Neustálé vylepšování struktury kódu při zachování funkčnosti.

**Výskyt**: `10. 1. 2017`, `2. 1. 2019`

**Související koncepty**: [[agilni-vyvoj|agilnímu vývoji]], [[metodiky-vyvoje|metodikám vývoje]]

---

### Průběžná integrace (CI)

**Otázka**: Co je to průběžná integrace a jaké jsou její výhody?

**Odpověď**:

Jde o praxi častého (i několikrát denně) začleňování kódu všech vývojářů do společné hlavní větve. Každé začlenění je automaticky ověřeno sestavením (buildem) a sadou testů, což umožňuje včasnou detekci chyb integrace.

**Výskyt**: `23. 1. 2019`

**Související koncepty**: [[nasazeni-aplikace|nasazování aplikací]], [[agilni-vyvoj|agilním praktikám]]

---

## 2. Návrh a Architektura

### Modely OMG MDA

**Otázka**: Jaké modely jsou definovány v rámci Model Driven Architecture (MDA)?

**Odpověď**:

- **CIM (Computation Independent Model)**: Model nezávislý na výpočetním systému, odpovídá doménovému modelu.
- **PIM (Platform Independent Model)**: Model nezávislý na konkrétní platformě (např. čisté UML bez detailů jazyka).
- **PSM (Platform Specific Model)**: Model přizpůsobený konkrétní technologii (např. J2EE nebo .NET).
- **Kód**: Samotná implementace (někdy označována jako ISM - Implementation Specific Model).

**Výskyt**: `30. 5. 2011`, `22. 5. 2018`

**Související koncepty**: [[softwarova-architektura|softwarové architektuře]]

---

### Principy GRASP

**Otázka**: Vysvětlete principy GRASP, konkrétně nízkou provázanost (Low Coupling) a vysokou soudržnost (High Cohesion).

**Odpověď**:

- **Nízká provázanost**: Snaha o minimalizaci závislostí mezi třídami. Změna v jedné třídě by měla mít minimální dopad na ostatní. Zvyšuje znovupoužitelnost a udržovatelnost.
- **Vysoká soudržnost**: Třída by měla mít jasně definovanou a úzkou zodpovědnost. Metody třídy by měly úzce souviset s jejím účelem. Usnadňuje pochopení a testování kódu.

**Výskyt**: `5. 6. 2018`, `10. 6. 2021`

**Související koncepty**: [[navrhovy-model-trid|návrhovému modelu tříd]], [[clean-code|principu Clean Code]]

---

### Liskov Substitution Principle (LSP)

**Otázka**: Definujte Liskov Substitution Principle.

**Odpověď**:

Objekty v programu by měly být nahraditelné instancemi svých podtříd, aniž by se změnila korektnost programu. Podtřída nesmí vyžadovat více (oslabení předpokladů) a nesmí zaručovat méně (posílení následných podmínek) než její nadtřída.

**Výskyt**: `29. 5. 2018`

**Související koncepty**: [[objektove-paradigma|objektovému paradigmatu]], [[clean-code|principu LSP]]

---

### OCL omezení (Object Constraint Language)

**Otázka**: Namodelujte integritní omezení v OCL (např. limit výpůjček, unikátnost záznamů).

**Odpověď**:

OCL se používá k definici invariantů, předpokladů a následných podmínek v UML modelech.
**Příklad** (limit výpůjček):
`context Osoba inv: self.vypujcky->size() <= 10`

**Výskyt**: `30. 5. 2011`, `15. 6. 2012`

**Související koncepty**: [[navrhovy-model-trid|návrhovému modelu tříd]]

---

### Architektura MVC

**Otázka**: Stručně popište princip architektury MVC.

**Odpověď**: Jde o oddělení datové logiky (**Model**), uživatelského rozhraní (**View**) a řízení toku událostí (**Controller**). View čte data přímo z modelu a Controller na základě vstupů od uživatele model mění.

**Výskyt**: `3. 1. 2017`

**Související koncepty**: [[mvc-mvp|vzoru MVC]]

---

### Návrhový vzor Stav (State)

**Otázka**: Popište návrhový vzor Stav a uveďte konkrétní příklad použití.

**Odpověď**: Vzor umožňuje objektu změnit své chování při změně jeho vnitřního stavu, přičemž se navenek jeví, jako by změnil svou třídu. Stavy jsou zapouzdřeny do samostatných tříd se společným rozhraním.
**Příklad**: Životní cyklus objednávky (Nová -> Zaplacená -> Odeslaná) nebo stavy přehrávače médií.

**Výskyt**: `15. 6. 2012`, `16. 5. 2014`, `23. 1. 2019`, `25. 5. 2023`

**Související koncepty**: [[navrhove-vzory-gof|návrhovým vzorům GoF]]

---

### Mapování dědičnosti do DB

**Otázka**: Jakými způsoby lze mapovat hierarchii dědičnosti do relační databáze?

**Odpověď**:

1.  **Single Table Inheritance**: Celá hierarchie v jedné tabulce (nutný diskriminátor, mnoho NULL hodnot).
2.  **Concrete Table Inheritance**: Jaká konkrétní podtřída má vlastní tabulku se všemi zděděnými sloupci.
3.  **Class Table Inheritance**: Každá třída (i abstraktní) má vlastní tabulku, vazby jsou řešeny cizími klíči.

**Výskyt**: `22. 5. 2018`, `8. 6. 2023`

**Související koncepty**: [[mapovani-dedicnosti|mapování dědičnosti]]

---

## 3. Požadavky a Kvalita

### Model FURPS

**Otázka**: Co znamená zkratka FURPS a uveďte příklady pro jednotlivé kategorie.

**Odpověď**: Slouží ke kategorizaci nefunkčních požadavků:

- **F (Functionality)**: Funkčnost (bezpečnost, audity).
- **U (Usability)**: Použitelnost (intuitivnost ovládání, lokalizace).
- **R (Reliability)**: Spolehlivost (dostupnost systému, odolnost proti chybám).
- **P (Performance)**: Výkon (rychlost odezvy, propustnost).
- **S (Supportability)**: Podporovatelnost (udržovatelnost, rozšiřitelnost).

**Výskyt**: `16. 5. 2014`, `5. 6. 2018`

**Související koncepty**: [[pozadavky|požadavkům]]

---

### Statická analýza kódu

**Otázka**: Jaké typy problémů typicky odhalí statická analýza zdrojového kódu?

**Odpověď**:

- Nedosažitelný kód (dead code).
- Použití neinicializovaných proměnných.
- Nekonečné smyčky.
- Porušení kódovacích konvencí a standardů.
- Potenciální bezpečnostní slabiny (např. SQL injection).
- Příliš vysoká komplexita metod (např. cyklomatická).

**Výskyt**: `18. 5. 2012`, `10. 1. 2017`, `2. 1. 2019`

**Související koncepty**: [[verifikace-a-validace|verifikaci a validaci]], [[testovani|testování]]

---

### Typy testování podle znalosti struktury

**Otázka**: Popište rozdíl mezi testováním typu Black Box a White Box.

**Odpověď**:

- **Black Box**: Tester nezná vnitřní strukturu ani kód systému. Ověřuje funkčnost na základě vstupů a očekávaných výstupů vůči specifikaci.
- **White Box**: Tester má přístup ke zdrojovému kódu a zná vnitřní strukturu systému. Testy se zaměřují na pokrytí cest kódu, podmínek a logiky.

**Výskyt**: `24. 5. 2013`, `9. 6. 2019`

**Související koncepty**: [[testovani|testování softwaru]]

---

### Interní a externí charakteristiky kvality

**Otázka**: Jaký je rozdíl mezi interními a externími charakteristikami kvality softwaru? Uveďte příklady.

**Odpověď**:

- **Externí**: Vlastnosti viditelné pro koncového uživatele. Příklady: **korektnost**, **použitelnost**, **spolehlivost**, **efektivita**.
- **Interní**: Vlastnosti důležité pro vývojáře a udržovatele systému. Příklady: **udržovatelnost**, **testovatelnost**, **znovupoužitelnost**, **čitelnost kódu**.

**Výskyt**: `29. 5. 2025`

**Související koncepty**: [[zajisteni-kvality|zajištění kvality]]

---

## 4. Provoz a Management

### Klasifikace údržby

**Otázka**: Jaké druhy údržby rozlišujeme a jaké jsou jejich cíle?

**Odpověď**:

1.  **Korektivní**: Oprava chyb nalezených až po nasazení do provozu.
2.  **Adaptivní**: Úprava systému pro nové prostředí (nový OS, HW, legislativa).
3.  **Perfektivní**: Zlepšování vlastností (výkon, uživatelská přívětivost) na základě požadavků uživatelů.
4.  **Preventivní**: Úpravy snižující riziko budoucích poruch (např. refaktoring).

**Výskyt**: `8. 6. 2023`

**Související koncepty**: [[podpora-a-udrzba|podpoře a údržbě]]

---

### Kritická cesta (CPM)

**Otázka**: Definujte kritickou cestu a vysvětlete její význam pro plánování projektu.

**Odpověď**: Kritická cesta je nejdelší možná cesta v síťovém grafu činností projektu. Určuje celkovou minimální dobu trvání projektu. Jakékoliv zpoždění činnosti na této cestě přímo posouvá termín dokončení celého projektu.

**Výskyt**: `25. 5. 2023`

**Související koncepty**: [[projektove-rizeni|projektovému řízení]], [[odhad-pracnosti|odhadům pracnosti]]

---

### Technologie REST

**Otázka**: Popište základní principy technologie REST.

**Odpověď**: Jde o architektonický styl orientovaný na zdroje (resources), které jsou identifikovány pomocí URI. K manipulaci se zdroji se využívají standardní metody HTTP (GET, POST, PUT, DELETE). Komunikace je bezstavová.

**Výskyt**: `12. 6. 2018`, `6. 6. 2019`

**Související koncepty**: [[webove-sluzby-rest-soap|webovým službám REST]]

---

### Integrační styly aplikací

**Otázka**: Vyjmenujte a stručně popište základní integrační styly.

**Odpověď**:

1.  **Sdílená databáze**: Aplikace přistupují ke stejným datům v jedné DB.
2.  **Přenos souborů**: Předávání dat pomocí exportu a importu souborů.
3.  **Vzdálené volání procedur (RPC)**: Synchronní volání funkcí jiného systému přes rozhraní.
4.  **Zasílání zpráv (Messaging)**: Asynchronní komunikace přes fronty zpráv (zajišťuje vyšší robustnost).

**Výskyt**: `24. 5. 2013`

**Související koncepty**: [[integrace-aplikaci|integraci aplikací]]

---

### Správa verzí (SVN vs. Git)

**Otázka**: Jaké možnosti poskytuje systém správy verzí (např. SVN nebo Git) a jaké jsou výhody/nevýhody?

**Odpověď**:

Systémy pro správu verzí umožňují sledovat historii změn v kódu, vracet se k předchozím verzím a efektivně spolupracovat v týmu.
- **Výhody**: Historie změn, možnost paralelní práce (větvení), záloha kódu, dohledatelnost autorů změn.
- **Nevýhody**: Nutnost řešit konflikty při sloučení změn (merge), režie na správu a naučení nástroje.

**Výskyt**: `3. 1. 2017`

**Související koncepty**: [[tymova-spoluprace|týmové spolupráci]]

---

## 5. Modelovací tipy a drobné poznatky

Tato sekce obsahuje specifické postřehy a drobné teoretické doplňky, které se objevily v zadáních nebo komentářích zkoušejících.

### Čas jako aktér
**Otázka**: Kdo může být aktérem v Use Case diagramu?
**Poznatek**: Aktérem nemusí být jen člověk nebo externí systém, ale také **Čas**. Používá se pro akce, které se spouštějí automaticky v daný okamžik (např. „každý večer se generuje uzávěrka“).

**Výskyt**: `18. 12. 2019`, `16. 12. 2020`

**Související koncepty**: [[pripady-uziti|případům užití]]

---

### Evidence historie (Role a Smlouvy)
**Otázka**: Jak v doménovém modelu zachytit historii rolí (např. kdy byl kdo ředitelem)?
**Poznatek**: Místo přímé vazby mezi Osobou a Rolí se vloží mezilehlá entita (např. **Smlouva** nebo **Působení**), která obsahuje atributy `od` a `do`.

**Výskyt**: `6. 1. 2021`

**Související koncepty**: [[domenovy-model|doménovému modelu]]

---

#zkouska #teorie #mda #up #scrum #furps #rest #BI-SWI
