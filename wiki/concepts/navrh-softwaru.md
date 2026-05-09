# Návrh softwaru

**Shrnutí**: Fáze softwarového inženýrství, která navazuje na analýzu. Zatímco analýza odpovídá na otázku "Co systém dělá?", návrh řeší "Jak to systém dělá?".

**Zdroje**:

- `raw/lectures/05.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Návrh softwaru (Design) je kritickým krokem před samotnou implementací. Zodpovědnost za tuto fázi obvykle nese **Solution Architekt** a výsledkem je prováděcí (návrhová) dokumentace. 

## Hlavní oblasti návrhu

- **Výběr implementačního jazyka**: Zvažuje se programovací paradigma (procedurální, objektově orientované, funkcionální), znalosti týmu, dostupnost frameworků a požadavky na přenositelnost. Většina moderních rozsáhlých systémů využívá objektově orientovaný (OO) přístup.
- **Způsob uložení dat**: Rozhodnutí mezi relační databází (nejrozšířenější, např. PostgreSQL, MySQL), objektovou databází, NoSQL databází (např. MongoDB) nebo prostými soubory. Volba závisí na nefunkčních požadavcích, budoucím rozvoji a rozpočtu.
- **[[softwarova-architektura|Návrh architektury]]**: Rozdělení systému na menší, udržovatelné části a definování jejich interakcí.
- **[[navrhovy-model-trid|Návrhový model tříd]]**: Realizace případů užití pomocí konkrétních objektů a přiřazení zodpovědností jednotlivým metodám softwarových tříd.

## Související stránky

- [[03-analyza-a-sber-pozadavku|Analýza požadavků]]
- [[role-analytika]]
- [[mapovani-dedicnosti]]

---
#swi #navrh #architektura #design #BI-SWI
