# Analýza problémové domény

**Shrnutí**: Tato přednáška se zaměřuje na tvorbu analytického doménového modelu, hledání entit v systému a zachycení jejich stavů pomocí stavových diagramů.

**Zdroje**:

- `raw/lectures/04.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Přednáška propojuje analytické výstupy z procesů a případů užití do strukturovaného datového pohledu, který slouží jako základ pro návrh systému.

## Klíčová témata

### Analytický doménový model
Cílem je vytvořit [[domenovy-model|doménový model]], který zachycuje klíčové pojmy (entity), jejich atributy a vzájemné vztahy na vysoké úrovni abstrakce. Tento model sjednocuje terminologii mezi zákazníkem a vývojáři a je nezávislý na konkrétní technologii uložení dat.

### Modelování životního cyklu (Stavový diagram)
Pro entity, které mají složité chování v čase, se vytváří [[stavovy-diagram|stavový diagram]]. Ten vizualizuje životní cyklus objektu, jeho možné stavy a události, které vyvolávají přechody mezi nimi. Pomáhá tak vyjasnit business logiku entit jako je "Objednávka" nebo "Výpůjčka".

### Hledání entit
Přednáška uvádí praktické postupy, jak identifikovat entity v textech scénářů případů užití nebo v procesních modelech. Typicky se jedná o podstatná jména, která reprezentují důležitá data systému. Správná identifikace entit a jejich vztahů předchází chybám v datovém návrhu.

## Související stránky
- [[domenovy-model]]
- [[stavovy-diagram]]
- [[role-analytika]]
- [[obchodni-procesy]]

---
#analyza #domena #entity #stavovy-diagram #BI-SWI
