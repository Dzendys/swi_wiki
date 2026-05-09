# Refaktoring

**Shrnutí**: Proces změny vnitřní struktury zdrojového kódu za účelem zlepšení jeho kvality a čitelnosti, aniž by se změnilo jeho vnější chování.

**Zdroje**:

- `raw/lectures/08.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Refaktoring je disciplinovaná technika pro restrukturalizaci existujícího těla kódu. Hlavním cílem je učinit kód čistším, srozumitelnějším a méně náchylným k chybám v budoucnu.

## Základní pravidla
1.  **Nemění se vnější chování**: Systém musí po refaktoringu dělat přesně to samé, co před ním.
2.  **Nutnost testů**: Před začátkem refaktoringu musí existovat sada testů, která ověří, že nedošlo ke změně chování (zdroj: raw/lectures/08.prednaska.pdf).
3.  **Malé kroky**: Změny by měly být prováděny v malých, kontrolovaných krůčcích.

## Kdy začít s refaktoringem (Code Smells)
Příznaky, že kód vyžaduje refaktoring:
-   **Duplicity**: Stejný nebo podobný kód na více místech (viz [[clean-code#DRY (Don't Repeat Yourself)|DRY]]).
-   **Dlouhé metody**: Metody přesahující jednu obrazovku nebo vykonávající více zodpovědností.
-   **Velké třídy**: Třídy s nízkou soudržností, které dělají příliš mnoho věcí.
-   **Příliš mnoho parametrů**: Metody vyžadující velké množství argumentů (často lze nahradit objektem).
-   **Komentáře**: Pokud jsou nutné k vysvětlení "co kód dělá", je lepší kód přepsat tak, aby byl samopopisný.
-   **Složité podmínky**: Hluboce zanořené nebo nepřehledné struktury `if-else`.
-   **Nedodržení jmenných konvencí**.

## Vybrané techniky
-   **Extrahování metody (Extract Method)**: Přesun části kódu do nové, dobře pojmenované metody.
-   **Přejmenování (Rename)**: Změna názvu metody, třídy nebo proměnné na srozumitelnější.
-   **Zapouzdření atributu**: Skrytí veřejného atributu za gettery a settery.
-   **Nahrazení dědičnosti delegováním**: Pokud dědičnost porušuje [[clean-code#Liskov Substitution Principle (LSP)|LSP]].
-   **Nahrazení chybového kódu výjimkou**: Čistší způsob ošetření chyb.
-   **Zavedení Null objektu**: Odstranění častých kontrol na `null`.
-   **Zavedení objektu jako parametru**: Seskupení souvisejících parametrů do jedné třídy.

## Doporučená literatura
-   Martin Fowler: *Refaktoring: zlepšení existujícího kódu* (ISBN: 80-247-0299-1).
-   Web [refactoring.com](http://refactoring.com/).

## Související stránky
- [[clean-code]]
- [[implementace]]
- [[osetreni-chyb-a-logovani]]

---
#refaktoring #clean-code #code-smells #software-quality #BI-SWI
