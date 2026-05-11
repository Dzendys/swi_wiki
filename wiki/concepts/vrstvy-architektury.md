# Vícevrstvé architektury

**Shrnutí**: Rozdělení systému do logických vrstev s jasně definovanými zodpovědnostmi a směrem závislostí za účelem zvýšení udržovatelnosti a testovatelnosti.

**Zdroje**:

- `raw/lectures/06.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Vrstvy představují horizontální rozdělení [[softwarova-architektura|softwarové architektury]]. Každá vrstva seskupuje logicky související komponenty a služby.

## Typy architektur dle počtu vrstev

- **Monolitická (jednovrstvá)**: Veškerý kód (UI, logika, DB přístup) je v jednom celku. Vhodné pro prototypy a velmi rychlý počáteční vývoj, ale extrémně náročné na údržbu u větších systémů.
- **Dvouvrstvá**: Typicky dělí systém na *Prezentační vrstvu* a *Datovou vrstvu*. Vhodná pro jednoduché CRUD aplikace (vytvoř, čti, uprav, smaž), kde není složitá business logika.
- **Třívrstvá**: Nejrozšířenější pro informační systémy. Skládá se z:
    1. **Prezentační vrstva**: GUI, formátování výstupů, zpracování vstupů od uživatele (např. HTML šablony, REST API).
    2. **Business vrstva (Doménová)**: Implementuje business logiku, procesy a validace. Je nezávislá na tom, jak jsou data zobrazena nebo uložena.
    3. **Datová vrstva (Technické služby)**: Zajišťuje [[persistence-dat|persistenci dat]] a komunikaci s externími službami (např. logování, odesílání emailů).

## Pravidla závislostí
Závislosti by měly směřovat vždy **shora dolů**. Rozlišujeme dva přístupy:

| Striktní vrstvení | Relaxované vrstvení |
| :---: | :---: |
| ![[imgs/06.prednaska-023.jpg\|250]] | ![[imgs/06.prednaska-025.jpg\|300]] |

- **Striktní architektura**: Vrstva může využívat pouze vrstvu bezprostředně pod ní.
- **Relaxovaná architektura**: Vrstva může využívat jakoukoliv vrstvu pod ní (např. prezentační vrstva může volat přímo technickou službu pro logování). V praxi je tento přístup nejčastější.

## Výhody vrstvení

- **Oddělení zájmů (Separation of Concerns)**: Snazší lokalizace chyb a pochopení kódu.
- **Znovupoužitelnost**: Nižší vrstvy (technické služby) jsou obecnější a lze je použít ve více projektech. Vyšší vrstvy jsou specifické pro konkrétní projekt.
- **Snadná výměna vrstev**: Lze např. vyměnit databázi nebo přidat mobilní aplikaci k existující business logice bez její změny.
- **Testovatelnost**: Jednotlivé vrstvy lze testovat izolovaně (pomocí mocků).

## Související stránky

- [[softwarova-architektura]]
- [[persistence-dat]]
- [[mvc-mvp]]

---
#swi #architektura #vrstvy #design #BI-SWI
