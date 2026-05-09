# Projektové řízení

**Shrnutí**: Tato sekce se věnuje disciplíně řízení softwarových projektů, plánování zdrojů a času, odhadování pracnosti a systematickému řízení rizik.

**Zdroje**:
- `wiki/lectures/11-projektove-rizeni.md`

**Naposledy aktualizováno**: 2026-05-18

---

## Projektové řízení v SWI

[[projektove-rizeni|Projektové řízení]] zajišťuje dodání softwarového produktu včas, v požadované kvalitě a v rámci stanoveného rozpočtu. Projektový manažer musí neustále vybalancovávat tzv. projektový trojúhelník: **Čas, Cena a Rozsah (Scope)**, přičemž nesmí dojít ke snížení **Kvality**.

### Fáze projektu
1. **Příprava**: Stanovení výstupů, vyhodnocení proveditelnosti a tvorba projektového plánu.
2. **Provádění**: Monitoring postupu, monitoring nákladů (v MDs) a komunikace se zákazníkem i týmem.
3. **Uzavření**: Předání produktu, akceptace a vyhodnocení historických dat pro budoucí projekty.

## Plánování a odhady

Základem každého plánu je [[odhad-pracnosti|odhad pracnosti]], vyjádřený v člověkohodinách (MH) nebo člověkodnech (MD). Odhady mohou vycházet z expertního úsudku, historických dat nebo metod jako Karnerova metoda (Use Case Points).

K vizualizaci harmonogramu a závislostí mezi úkoly se využívají:
- **WBS (Work Breakdown Structure)**: Hierarchický rozklad práce na menší celky.
- **Ganttův diagram**: Časová osa úkolů se zobrazením vazeb a kritické cesty.

![[imgs/11.prednaska-032.jpg|643]]
*Obrázek: Vizualizace projektového plánu pomocí Ganttova diagramu.*

## Řízení rizik

[[rizeni-rizik|Řízení rizik]] je preventivní proces identifikace hrozeb. U každého rizika se sleduje **pravděpodobnost** výskytu a **dopad (impakt)** na projekt. 

Strategie řešení zahrnují:
- **Akceptace**: Přijetí rizika.
- **Minimalizace**: Snížení pravděpodobnosti nebo dopadu.
- **Odstranění**: Eliminace zdroje rizika.
- **Přenesení**: Např. pojištění nebo delegování na subdodavatele.

## Týmová spolupráce

V softwarovém inženýrství je zodpovědnost za výsledek sdílená. [[tymova-spoluprace|Týmová spolupráce]] vyžaduje jasné rozdělení rolí (Analytik, Architekt, Vývojář, Tester) a efektivní využití nástrojů pro komunikaci a správu úkolů (např. GitLab Issues). Důležitým aspektem je transparentnost a pravidelná synchronizace týmu.

## Související stránky
- [[projektove-rizeni]]
- [[odhad-pracnosti]]
- [[rizeni-rizik]]
- [[tymova-spoluprace]]
- [[softwarove-inzenyrstvi]]

---
#management #projekt #rizika #planovani #tym #BI-SWI
