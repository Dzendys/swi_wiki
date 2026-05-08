# Softwarové inženýrství

**Shrnutí**: Disciplína zabývající se systematickým, kontrolovaným a efektivním vývojem a údržbou softwarových systémů.

**Zdroje**:
- `raw/lectures/01.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

**Softwarové inženýrství** (SWI) představuje systematický přístup k tvorbě softwaru (zdroj: raw/lectures/01.prednaska.pdf). Nejde pouze o programování, ale o řešení komplexních problémů spojených s vývojem rozsáhlých informačních systémů.

## Životní cyklus vývoje softwaru (SDLC)
Způsob, jakým jsou jednotlivé kroky vývoje uspořádány, definuje **[[metodiky-vyvoje#Modely životního cyklu (SDLC)|model životního cyklu]]** (Vodopád, Iterativní model, Agilní přístup). Moderní inženýrství preferuje iterace:

1.  **[[obchodni-procesy|Modelování obchodních procesů]]**: Pochopení činnosti zákazníka.
2.  **[[pozadavky|Analýza a sběr požadavků]]**: Definice toho, co má systém dělat (funkční požadavky) a jaké má mít vlastnosti (nefunkční požadavky dle modelu [[pozadavky#Model FURPS|FURPS]]).
3.  **[[04-analyza-problemove-domeny|Analýza domény]]**: Vytvoření [[domenovy-model|doménového modelu]], který zachycuje klíčové pojmy a vztahy v reálném světě nezávisle na technologii.
4.  **[[navrh-softwaru|Návrh systému (Design)]]**: Rozhodnutí o tom, *jak* bude systém postaven.
    *   Definice [[softwarova-architektura|architektury]] a [[vrstvy-architektury|vrstev]].
    *   Detailní [[navrhovy-model-trid|návrh tříd]], metod a [[komponenty-a-rozhrani|komponent]].
    *   Volba [[persistence-dat|persistence]] a [[mapovani-dedicnosti|mapování dat]].
5.  **[[implementace|Implementace]]**: Samotná konstrukce kódu. Klíčem je dodržování pravidel [[clean-code|čistého kódu]], využívání [[navrhove-vzory-gof|návrhových vzorů]] a průběžný [[refaktoring]].
6.  **[[zajisteni-kvality|Zajištění kvality (QA)]]**: Průběžná [[verifikace-a-validace|verifikace a validace]] systému pomocí různých úrovní [[testovani|testování]].
7.  **[[nasazeni-aplikace|Nasazení]] a [[podpora-a-udrzba|údržba]]**: Předání systému do provozu, řešení incidentů (SLA) a dlouhodobý rozvoj (opravná, adaptivní či zdokonalovací údržba).

## Průřezová témata
Softwarové inženýrství zahrnuje i disciplíny, které prostupují celým cyklem:
- **Management**: [[tymova-spoluprace|Týmová spolupráce]], [[odhad-pracnosti|odhady pracnosti]] a verzování.
- **Metodiky a proces**: Volba konkrétního přístupu k vývoji, např. klasický [[unified-process|Unified Process]] nebo agilní [[scrum|SCRUM]] (viz [[metodiky-vyvoje]]).
- **Integrace**: Propojování systémů pomocí [[integrace-aplikaci|integračních stylů]] a [[webove-sluzby-rest-soap|webových služeb]].

## Související stránky
- [[role-analytika]]
- [[softwarova-architektura]]
- [[index]]

---
#swi #teorie #metodika #BI-SWI
