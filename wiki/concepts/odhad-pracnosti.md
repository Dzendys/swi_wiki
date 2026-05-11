# Odhad pracnosti

**Shrnutí**: Proces stanovení množství práce potřebné k dokončení úkolu nebo celého projektu, vyjádřený v člověkohodinách nebo dnech.

**Zdroje**:

- `raw/lectures/01.prednaska.pdf`
- `raw/lectures/11.prednaska.pdf`



---

[[odhad-pracnosti|Odhad pracnosti]] je klíčový pro plánování projektu a stanovení termínu dodání nebo potřebné velikosti týmu.

## Používané jednotky
Pracnost se určuje v "člověko-jednotkách":

- **Man-hour (MH)**: Pracovní hodina člověka.
- **Man-day (MD)**: Pracovní den člověka (obvykle 1 MD = 8 MH).
- **Man-week (MW)**: Pracovní týden člověka (obvykle 1 MW = 5 MD).

## Vztah pracnosti a času
Termín dodání lze odvodit z pracnosti a velikosti týmu. Teoreticky lze úkol o rozsahu 10 MD stihnout ve dvou lidech za 5 dní.
**Pozor**: V praxi spolupráce více osob přináší režii (komunikace, koordinace), takže doba trvání se s počtem lidí **nezkracuje lineárně**.

## Stanovení odhadu
Odhad nelze snadno provést bez detailní znalosti rozsahu (**scope**) projektu. Rozsah zahrnuje nejen implementaci, ale i dokumentaci, školení a řízení.

### Metody odhadování

-   **Úsudek (Expert Judgment)**: Rychlý, ale často nepřesný (programátoři bývají příliš optimističtí).
-   **Karnerova metoda (Use Case Points)**: Odhad na základě počtu a složitosti [[pripady-uziti|aktérů a případů užití]].
-   **COCOMO (Constructive Cost Model)**: Matematický model založený na odhadovaném počtu řádek kódu (LOC).
-   **Historická data**: Porovnání s dřívějšími projekty v daném odvětví je nejspolehlivější cestou.

### Pravidla pro přesnější odhady

-   **Odhadujte v rozmezí**: Místo jednoho čísla určete dolní a horní hranici (např. s 90% pravděpodobností se výsledek vejde do tohoto intervalu).

![[imgs/11.prednaska-025.jpg|1286]]

*Obrázek: Tlak na odhadování a nejistota s tím spojená.*

-   **Zohledněte velikost**: Pracnost s velikostí projektu neroste lineárně.
-   **Nepodléhejte tlaku**: Úmyslně nižší odhad je "sleva", která by měla být věcí obchodu, nikoliv technika.
-   **Použijte více metod**: Výsledky porovnejte a analyzujte rozdíly.

## Související stránky

- [[projektove-rizeni]]
- [[role-analytika]]
- [[rizeni-rizik]]
- [[tymova-spoluprace]]

---
#planovani #management #pracnost #BI-SWI
