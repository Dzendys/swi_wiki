# 06. Architektonické vzory

**Shrnutí**: Šestá přednáška se zaměřuje na hlubší pohled do architektonických vzorů, vrstvení systémů, vzory pro persistenci dat a vzory pro prezentační vrstvu.

**Zdroje**:
- `raw/lectures/06.prednaska.pdf`
- `raw/extra/Table Data Gateway.pdf`
- `raw/extra/Row Data Gateway.pdf`
- `raw/extra/Active Record.pdf`
- `raw/extra/Data Mapper.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Přednáška navazuje na základy [[navrh-softwaru|návrhu]] a představuje konkrétní šablony řešení opakujících se problémů v architektuře rozsáhlých systémů.

## Klíčová témata přednášky

### 1. GRASP Principy (Recap)
Byl kladen důraz na tři základní principy pro přiřazování zodpovědností třídám:
- **Informační expert**: Dej metodu tam, kde jsou data.
- **Nízká provázanost**: Minimalizuj počet vazeb mezi třídami.
- **Vysoká soudržnost**: Třída má dělat jen jednu věc a dobře.
Podrobněji popsáno v [[navrhovy-model-trid#Přiřazování zodpovědností (GRASP)]].

### 2. Vícevrstvé architektury
Vysvětlení rozdílu mezi monolitickou, dvouvrstvou a **třívrstvou architekturou**. Třívrstvá architektura (Prezentační, Business, Datová vrstva) je standardem pro podnikové aplikace díky své rozšiřitelnosti a testovatelnosti. Byly definovány pojmy *striktní* a *relaxovaná* architektura (zdroj: raw/lectures/06.prednaska.pdf). Podrobnosti viz [[vrstvy-architektury]].

### 3. Persistence dat
Představení čtyř základních vzorů pro komunikaci s databází:
- **Table Data Gateway**: Jedna třída pro celou tabulku.
- **Row Data Gateway**: Objekt pro každý řádek.
- **Active Record**: Objekt s daty i business logikou (oblíbené, ale porušuje vrstvení).
- **Data Mapper**: Úplné oddělení doménových objektů od databáze (využití v ORM).
Podrobnosti viz [[persistence-dat]].

### 4. MVC a MVP
Architektonické vzory pro prezentační vrstvu umožňující oddělení logiky zobrazení od dat. U MVP je zdůrazněna snadnější testovatelnost Presenteru oproti Controlleru v MVC. Podrobnosti viz [[mvc-mvp]].

### 5. Spolupráce objektů
Využití **sekvenčních diagramů** k popisu interakce mezi instancemi tříd. Diagram zachycuje synchronní a asynchronní zprávy, vytváření objektů a cykly nad kolekcemi. Byl ukázán příklad na procesu "vypůjčení výtisku" (zdroj: raw/lectures/06.prednaska.pdf). Podrobnosti viz [[sekvencni-diagram]].

## Související stránky
- [[vrstvy-architektury]]
- [[persistence-dat]]
- [[mvc-mvp]]
- [[sekvencni-diagram]]
- [[navrhovy-model-trid]]

---
#swi #prednaska #architektura #vzory #grasp #uml #BI-SWI
