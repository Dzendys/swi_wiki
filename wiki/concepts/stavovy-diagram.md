# Stavový diagram (UML)

**Shrnutí**: Diagram chování v UML (State Machine Diagram) používaný k zachycení životního cyklu entity, jejích stavů a přechodů mezi nimi vyvolaných událostmi.

**Zdroje**:

- `raw/lectures/04.prednaska.pdf`



---

[[stavovy-diagram|UML Stavový diagram]] slouží k porozumění životnímu cyklu entit, které se v systému nacházejí v různých stavech v závislosti na čase a událostech.

## Základní pojmy

- **Stav (State)**: Podmínka nebo situace v životě objektu, během které objekt splňuje určitou podmínku nebo vykonává nějakou aktivitu.
- **Přechod (Transition)**: Vztah mezi dvěma stavy naznačující, že objekt v prvním stavu provede určité akce a přejde do druhého stavu, nastane-li specifikovaná událost a jsou-li splněny podmínky.
- **Událost (Event)**: Výskyt něčeho, co může spustit přechod.

![[imgs/04.prednaska-042.jpg|851]]

*Obrázek: Životní cyklus entity Výtisk (stavy Volný, Vypůjčený, Ztracený, Vyřazený).*


## Notace

- **Počáteční stav**: Plné kolečko.
- **Koncový stav**: Terčík.
- **Stav**: Obdélník se zaoblenými rohy s názvem stavu.
- **Hrana přechodu**: Šipka s popisem ve formátu: `Událost [Podmínka] / Akce`.

## Důležitá upozornění
Stavový diagram **není diagramem aktivit**. Diagram aktivit popisuje tok činností v procesu, zatímco stavový diagram popisuje stavy, ve kterých se nachází konkrétní objekt.

## Související stránky

- [[domenovy-model]]
- [[obchodni-procesy]]

---
#uml #state-machine #analyza #stavy #BI-SWI
