# Clean Code a principy návrhu

**Shrnutí**: Soubor pravidel a principů (SRP, DRY, Law of Demeter, LSP), které vedou k čitelnému, udržovatelnému a rozšiřitelnému zdrojovému kódu.

**Zdroje**:
- `raw/lectures/08.prednaska.pdf`
- `raw/extra/GRASP.pdf`
- `raw/extra/Vysoká soudržnost.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Psaní "čistého kódu" (Clean Code) je základní dovedností softwarového inženýra. Cílem je minimalizovat chybovost a usnadnit budoucí úpravy systému.

## Klíčové principy

### Vysoká soudržnost (High Cohesion) a SRP
- **Soudržnost (Cohesion)**: Míra, jak moc k sobě zodpovědnosti jednoho prvku (metody, třídy) logicky patří.
- **SRP (Single Responsibility Principle)**: Každý prvek by měl mít právě jednu přesně definovanou zodpovědnost (zdroj: raw/extra/Vysoká soudržnost.pdf).
- **Výhody**: Snazší pochopení, údržba a stabilita. Prvky s nízkou soudržností jsou nestabilní, protože se musí měnit z mnoha různých důvodů.
- *Tip*: Pokud metoda obsahuje prázdné řádky nebo komentáře vysvětlující různé sekce, pravděpodobně by měla být rozdělena na více metod.

### Nízká provázanost (Low Coupling) a Law of Demeter
- **Provázanost (Coupling)**: Míra závislosti mezi třídami. Cílem je, aby změna v jedné třídě vyžadovala minimální změny v ostatních.
- **Law of Demeter ("Don't talk to strangers")**: Objekt by měl volat pouze metody svých přímých známých (vlastní metody, metody atributů, vytvořených objektů nebo parametrů). Neměl by "procházet" skrze cizí objekty (např. `a.getB().getC().doSomething()` je porušením tohoto pravidla).

### DRY (Don't Repeat Yourself)
Zákaz duplicity kódu i dat. Duplicita vede k chybám při aktualizacích (zapomenutí na změnu na všech místech). Funkcionalita by měla být zapouzdřena do jedné metody/třídy a data by měla být uložena na jednom místě nebo odvozena.

### Liskov Substitution Principle (LSP)
Podtřída musí být použitelná všude tam, kde je očekávána její nadtřída, aniž by se změnila korektnost programu.

![|x200](imgs/08.prednaska-032.jpg)
*Obrázek: Klasický příklad nevhodného použití dědičnosti, kdy Čtverec dědí z Obdélníku a porušuje jeho chování.*

- **Příklad špatného užití**: Dědění `Čtverce` od `Obdélníka`. Pokud kód nastaví šířku a očekává, že výška zůstane stejná, u čtverce toto selže (změní se obojí).
- **Doporučení**: Upřednostňujte **skládání (composition)** před dědičností. Dědičnost je velmi silná vazba a vícenásobná dědičnost často porušuje vysokou soudržnost.

### Programování proti rozhraní (Interface)
Kód by měl záviset na **[[komponenty-a-rozhrani|rozhraní]]**, nikoliv na konkrétní implementaci. To umožňuje snadnou výměnu komponent nebo rozšíření systému bez zásahu do existující logiky. Rozhraní by mělo být vnímáno jako "neměnný kontrakt".

## Čitelnost a konvence
- **Srozumitelné názvy**: Třídy, metody a parametry musí být samopopisné (např. `pokutaZaZpozdeni` místo `y`).
- **Pojmenování**: Dodržování konvencí (`camelCase`, `PascalCase`, `SNAKE_CASE`) dle standardů daného jazyka (např. Java, C#, Kotlin, TS).
- **Délka metod**: Ideálně jedna obrazovka (max. 100-200 řádků). Čím delší metoda, tím vyšší chybovost.
- **Magické konstanty**: Nepoužívat literály v kódu (např. `50`), ale pojmenované konstanty (`SPRAVNI_POPLATEK`).

## Související stránky
- [[implementace]]
- [[objektove-paradigma]]
- [[refaktoring]]
- [[komponenty-a-rozhrani]]

---
#clean-code #srp #dry #solid #lsp #software-quality #BI-SWI
