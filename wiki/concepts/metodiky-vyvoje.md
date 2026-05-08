# Metodiky vývoje softwaru

**Shrnutí**: Sada doporučení, pravidel a pracovních postupů, které definují, jakým způsobem se vyvíjí softwarový produkt.

**Zdroje**:
- `raw/lectures/12.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

**Softwarový proces** je posloupnost kroků vedoucích k vytvoření produktu. Snaha o jeho standardizaci a opakovatelnost vede k vytvoření **metodiky** (zdroj: raw/lectures/12.prednaska.pdf).

## Modely životního cyklu (SDLC)
Způsob, jakým jsou jednotlivé kroky (analýza, návrh, implementace, testování) uspořádány v čase:

### 1. Vodopád (Waterfall)
Sekvence kroků, kde každá fáze musí být dokončena před začátkem další.
- **Vlastnosti**: Lineární postup, obtížný návrat zpět (pouze o jeden krok).
- **Vhodné pro**: Projekty s jasnými, fixními požadavky na začátku.

### 2. Iterativní model
Projekt je rozdělen do menších celků (iterací), které fungují jako "malé vodopády".
- **Vlastnosti**: Průběžné dodávky funkčních částí, rychlá zpětná vazba od zákazníka, možnost měnit směr (požadavky) během vývoje.
- **Příklad**: [[unified-process|Unified Process (UP)]].

### 3. Agilní přístup
Iterativní model, kde je délka iterace zkrácena na minimum (týdny).
- **Vlastnosti**: Extrémní důraz na spolupráci, fungující software a reakci na změnu (viz [[agilni-vyvoj|Agilní manifest]]).
- **Příklad**: [[scrum|SCRUM]].

## Kategorizace metodik

### Klasické metodiky ("Těžké")
Kladou velký důraz na proces, plánování a rozsáhlou dokumentaci. Bývají propracovanější a řeší širší spektrum problémů, ale jejich dodržování je pracné.
- **Příklady**: [[unified-process|Unified Process (UP)]], RUP, Moderní strukturovaná analýza (MSA).

### Agilní metodiky ("Lehké")
Zaměřují se na samotnou tvorbu produktu a minimalizaci dokumentace. Upřednostňují rychlé dodání první verze a následné úpravy na základě zpětné vazby od zákazníka.
- **Příklady**: [[scrum|SCRUM]], XP (Extrémní programování), TDD (Test Driven Development).

## Výběr metodiky
Neexistuje jediná správná metodika. Volba závisí na:
- **Velikosti a složení týmu** (zkušenosti, distribuovanost).
- **Stabilitě požadavků** (pokud se mění, je lepší agilní přístup).
- **Zákazníkovi** (jeho ochota spolupracovat a akceptovat daný styl).
- **Kultuře organizace**.

## Související stránky
- [[softwarove-inzenyrstvi]]
- [[projektove-rizeni]]
- [[unified-process]]
- [[agilni-vyvoj]]

---
#metodiky #proces #software-engineering #management #BI-SWI
