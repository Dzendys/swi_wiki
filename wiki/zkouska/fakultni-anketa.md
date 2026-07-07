# Fakultní ankety

**Shrnutí**: Zadání doménového modelu systému pro správu anket o předmětech a jejich hodnocení studenty, zahrnující životní cyklus ankety, anonymitu odpovědí a zveřejnění výsledků.

**Zdroje**:
- `domenove-modely/fakutlni-anketa.md`
- `domenove-modely/dump.md`

**Výskyty tématu**: 7. 1. 2015 · 3. 1. 2017 · 13. 6. 2019 · 13. 1. 2021 · 29. 5. 2025

---

tmp

## Zadání doménového modelu

Namodelujte systém pro správu anket o předmětech a jejich hodnocení studenty. **Anketu připravuje správce ankety**, který do ní přidá předměty, kterých se bude týkat, a jednotlivé odpovědi. Vybrat lze pouze předměty vyučované v semestru, ke kterému se anketa vztahuje. U předmětů se eviduje jejich kód, název a popis. Odpověď může být buď ve formě známky (1 – výborný, 2 – ucházející, 3 – špatný), nebo může obsahovat i názor studenta ve formě textu.

Po připravení je **anketa postoupena garantovi ankety, který ji musí zkontrolovat**. Při zjištění nedostatků ji vrátí správci k přepracování (opravě), v opačném případě je schválena. Poté, co nastane počáteční datum, je anketa zpřístupněna (otevřena) studentům.

Studenti se přihlásí svým uživatelským jménem a heslem a anketu vyplňují. **Každý student může danou anketu vyplnit pouze jednou** (není možné se k ní vrátit ani odpovídat znovu) a za předpokladu, že **má zapsané předměty, kterých se anketa týká**. Každá odpověď je evidována s ohledem na anonymitu, takže **odpovědi nesmí být možné přiřadit ke konkrétnímu studentovi**.

Systém každý den kontroluje, zda vypršel čas pro vyplnění ankety. Po uplynutí koncového data (časového limitu) je **anketa automaticky uzavřena**. Správce musí následně zkontrolovat, zda neobsahuje nevhodné komentáře. Po provedení cenzury a kontroly jsou výsledky ankety zveřejněny. Hodnocení jednotlivých předmětů se v systému trvale uchovává, aby bylo možné sledovat vliv změn ve výuce během doby běhu předmětu.


## Praktické úkoly

### [[domenovy-model|Doménový model]]

- Vytvořte doménový model popsané části systému.

### [[diagram-aktivit|Diagram aktivit]]

- Nakreslete diagram aktivit se swimlines zachycující proces přípravy a průběhu/životního cyklu ankety (do diagramu zahrňte stavy ze stavového diagramu).

### [[stavovy-diagram|Stavový diagram]]

- Nakreslete stavový diagram ankety se všemi podmínkami a akcemi, které daný přechod spustí.

### [[sekvencni-diagram|Sekvenční diagram]]

- Vytvořte sekvenční diagram pro získání statistiky hodnocení dané ankety.

### [[diagram-pripadu-uziti|Diagram případů užití]]

- **Varianta A**: Nalezněte všechny účastníky a uveďte alespoň 5 případů užití.
- **Varianta B**: Jmenujte a popište alespoň 3 případy užití systému a jejich aktéry.

### Diagram komponent

- Aplikace má 3 komponenty – GUI, CORE, REST_API. GUI komunikuje s CORE pomocí rozhraní `SpravaVysledku` a `SpravaAnkety`. REST_API komunikuje s CORE pouze přes `SpravaVysledku`. `SpravaVysledku` má implementaci `SpravaVysledkuImpl`. Zachyťte jako UML diagram (diagram komponent).


## Související stránky
- [[domenovy-model|Doménový model]]
- [[diagram-aktivit|Diagram aktivit]]
- [[stavovy-diagram|Stavový diagram]]
- [[sekvencni-diagram|Sekvenční diagram]]
- [[diagram-pripadu-uziti|Diagram případů užití]]
- [[pripady-uziti|Případy užití]]
- [[komponenty-a-rozhrani|Komponenty a rozhraní]]

---
#zkouska #domenovy-model #BI-SWI
