# 06. Architektonicke-vzory

**Shrnutí**: Šestá přednáška se zaměřuje na hlubší pohled do architektonických vzorů, vrstvení systémů, vzory pro persistenci dat a vzory pro prezentační vrstvu.

**Zdroje**:

- `raw/lectures/06.prednaska.pdf`



---

Přednáška představuje osvědčené šablony (vzory) pro řešení opakujících se architektonických problémů v rozsáhlých systémech.

## Klíčová témata

### Vícevrstvé architektury
Logické rozdělení systému na nezávislé [[vrstvy-architektury|vrstvy]] (Prezentační, Business, Datová) je standardem pro podnikové aplikace. Přednáška vysvětluje pravidla závislostí, které by měly směřovat vždy shora dolů, a rozdíl mezi striktní a relaxovanou architekturou.

### Persistence dat
Přednáška detailně rozebírá čtyři základní vzory pro komunikaci s databází, které definoval Martin Fowler. Tyto vzory pro [[persistence-dat|persistenci dat]] (Table/Row Data Gateway, Active Record, Data Mapper) se liší mírou provázání business logiky s databázovým schématem.

### Vzory pro prezentační vrstvu
Oddělení logiky zobrazení od dat je klíčové pro testovatelnost a údržbu GUI. Přednáška porovnává klasický vzor **MVC** (Model-View-Controller) s modernějším **MVP** (Model-View-Presenter), který lépe izoluje pohled od aplikační logiky. Podrobnosti viz [[mvc-mvp]].

### Spolupráce objektů (Sekvenční diagram)
Pro zachycení dynamického chování systému v čase se využívá [[sekvencni-diagram|sekvenční diagram]]. Ten vizualizuje interakci mezi instancemi tříd (výměnu zpráv) při realizaci konkrétního scénáře případu užití.

## Související stránky

- [[vrstvy-architektury]]
- [[persistence-dat]]
- [[mvc-mvp]]
- [[sekvencni-diagram]]
- [[navrhovy-model-trid]]

---
#swi #prednaska #architektura #vzory #grasp #uml #BI-SWI

