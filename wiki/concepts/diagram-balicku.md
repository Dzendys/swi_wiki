# Diagram balíčků (UML)

**Shrnutí**: Strukturální diagram v UML používaný k organizaci modelových elementů do logických skupin (balíčků). Slouží k rozdělení rozsáhlých systémů na přehledné oblasti.

**Zdroje**:
- `raw/lectures/03.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

[[diagram-balicku|Diagram balíčků]] (Package Diagram) umožňuje rozdělit systém na jednotlivé „oblasti“ (např. Evidence čtenářů, Správa výpůjček), které jsou následně detailně analyzovány (zdroj: raw/lectures/03.prednaska.pdf).

## Využití v analýze
- **High-level pohled**: Poskytuje přehled nad celým systémem bez zabřednutí do detailů.
- **Prvotní odhady**: Pomáhá při hrubém stanovení rozsahu a [[odhad-pracnosti|pracnosti]] projektu.
- **Hierarchie**: Balíčky mohou být do sebe vnořovány, což umožňuje hierarchickou organizaci požadavků nebo komponent (zdroj: raw/lectures/03.prednaska.pdf).

## Notace
- **Balíček (Package)**: Symbol složky s názvem oblasti.
- **Závislost (Dependency)**: Směrovaná čárkovaná šipka mezi balíčky, značící, že jeden balíček využívá elementy jiného balíčku.

## Související stránky
- [[role-analytika]]
- [[odhad-pracnosti]]
- [[pozadavky]]

---
#uml #package-diagram #analyza #organizace #swi #BI-SWI
