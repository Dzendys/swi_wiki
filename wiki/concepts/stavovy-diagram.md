# Stavový diagram (UML)

**Shrnutí**: Diagram chování v UML (State Machine Diagram) používaný k zachycení životního cyklu entity, jejích stavů a přechodů mezi nimi vyvolaných událostmi.

**Zdroje**:
- `raw/lectures/04.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

[[stavovy-diagram|UML Stavový diagram]] slouží k porozumění životnímu cyklu entit, které se v systému nacházejí v různých stavech v závislosti na čase a událostech (zdroj: raw/lectures/04.prednaska.pdf).

## Základní pojmy
- **Stav (State)**: Podmínka nebo situace v životě objektu, během které objekt splňuje určitou podmínku nebo vykonává nějakou aktivitu (zdroj: raw/lectures/04.prednaska.pdf).
- **Přechod (Transition)**: Vztah mezi dvěma stavy naznačující, že objekt v prvním stavu provede určité akce a přejde do druhého stavu, nastane-li specifikovaná událost a jsou-li splněny podmínky (zdroj: raw/lectures/04.prednaska.pdf).
- **Událost (Event)**: Výskyt něčeho, co může spustit přechod (zdroj: raw/lectures/04.prednaska.pdf).

![|500](imgs/04.prednaska-035.jpg)
*Obrázek: Životní cyklus entity Výtisk (stavy Volný, Vypůjčený, Ztracený, Vyřazený).*

## Notace
- **Počáteční stav**: Plné kolečko.
- **Koncový stav**: Terčík.
- **Stav**: Obdélník se zaoblenými rohy s názvem stavu.
- **Hrana přechodu**: Šipka s popisem ve formátu: `Událost [Podmínka] / Akce` (zdroj: raw/lectures/04.prednaska.pdf).

## Důležitá upozornění
Stavový diagram **není diagramem aktivit**. Diagram aktivit popisuje tok činností v procesu, zatímco stavový diagram popisuje stavy, ve kterých se nachází konkrétní objekt (zdroj: raw/lectures/04.prednaska.pdf).

## Související stránky
- [[domenovy-model]]
- [[obchodni-procesy]]

---
#uml #state-machine #analyza #stavy #BI-SWI
