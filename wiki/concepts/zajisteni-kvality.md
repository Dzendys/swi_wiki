# Zajištění kvality (Quality Assurance)

**Shrnutí**: Systematický proces a sada aktivit zaměřených na zajištění a měření kvality softwarového produktu v průběhu celého vývojového cyklu.

**Zdroje**:
- `raw/lectures/09.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Zajištění kvality (QA) je systematický přístup k zajištění toho, aby softwarový produkt splňoval stanovené požadavky a standardy. Testování je pouze jednou z forem aktivit v rámci QA (zdroj: raw/lectures/09.prednaska.pdf).

## Cíle QA
- **Zajištění kvality dodávaného řešení**: Naplnění očekávání zákazníka a bezchybnost.
- **Měření kvality**: Kvantifikace stavu produktu pomocí metrik.
- **Úspora financí a zdrojů**: Prevence chyb je levnější než jejich následná oprava. Cena opravy chyby roste exponenciálně s časem (zdroj: raw/lectures/09.prednaska.pdf).

![[imgs/09.prednaska-012.jpg|1000]]
*Obrázek: Exponenciální nárůst nákladů na opravu chyby v závislosti na fázi odhalení.*

## Měření kvality (Statická analýza)
Moderní nástroje pro statickou analýzu (např. SonarQube) umožňují vizualizovat kvalitu kódu pomocí různých metrik, jako je technický dluh, spolehlivost a udržovatelnost.

![[imgs/09.prednaska-022.jpg|620]] ![[imgs/09.prednaska-023.jpg|615]]
*Obrázek: Ukázky výstupů statické analýzy zaměřené na spolehlivost (chyby) a udržovatelnost (technický dluh).*

## Charakteristiky kvality
Kvalitu lze posuzovat z různých úhlů pohledu (vychází z modelu [[pozadavky#Model FURPS|FURPS]] a normy ISO/IEC 25010):

### Externí charakteristiky (podpora uživatele)
- **Korektnost**: Systém plní specifikované funkce a neobsahuje chyby.
- **Použitelnost**: Snadné naučení a používání systému.
- **Efektivita**: Optimální využívání hardwarových zdrojů (čas, paměť).
- **Spolehlivost**: Schopnost systému fungovat bez výpadků.
- **Integrita**: Ochrana před neoprávněným přístupem a změnami.
- **Robustnost**: Schopnost reagovat na nevalidní vstupy a stresové situace.

### Interní charakteristiky (podpora vývoje)
- **Udržovatelnost**: Snadný rozvoj, opravy chyb a přizpůsobivost.
- **Testovatelnost**: Snadné psaní a provádění testů.
- **Znovupoužitelnost**: Možnost využít části kódu v jiných systémech.
- **Čitelnost a srozumitelnost**: Snadné pochopení kódu a architektury (souvisí s [[clean-code]]).

## Aktivity v procesu QA
1.  **Naplánování procesů**: Stanovení cílů (např. "minimalizace paměťových nároků") a definice, kdo a kdy bude aktivity provádět (školení, inspekce, testování).
2.  **Měření kvality**: Sběr dat (např. výsledky code review, metriky statické analýzy).
3.  **Vyhodnocení a zlepšování**: Analýza výsledků a úprava procesů pro zvýšení kvality.
4.  **Řízení**: Celková koordinace QA aktivit v rámci projektu.

## Související stránky
- [[verifikace-a-validace]]
- [[testovani]]
- [[pozadavky]]

---
#qa #quality-assurance #software-engineering #metrics #BI-SWI
