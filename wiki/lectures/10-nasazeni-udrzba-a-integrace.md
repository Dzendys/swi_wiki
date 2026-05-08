# 10. Nasazení, údržba a integrace aplikací

**Shrnutí**: Tato přednáška se zabývá závěrečnými fázemi životního cyklu softwaru – od sestavení a nasazení přes podporu a různé typy údržby až po propojení aplikací pomocí integračních stylů a webových služeb.

**Zdroje**:
- `raw/lectures/10.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Po fázi [[implementace|implementace]] a [[testovani|testování]] následuje nasazení systému do provozu, jeho následná správa a často i nutnost propojení s jinými systémy.

## Klíčová témata

### [[nasazeni-aplikace|Nasazení aplikace]]
- **Sestavení (Build)**: Použití nástrojů jako Maven, Gradle (Java) nebo npm (JavaScript).
- **Proces**: Stažení závislostí, vytvoření spustitelného systému, generování dokumentace.
- **Způsob**: Přechod od nespolehlivého manuálního nasazení k automatizovaným **pipeline** (minimalizace lidské chyby).

### [[podpora-a-udrzba|Podpora a údržba]]
- **Úrovně podpory**: 1. úroveň (helpdesk), 2. úroveň (technická), 3. úroveň (experti/vývojáři).
- **SLA (Service Level Agreement)**: Garance dostupnosti, doby výpadku a rychlosti vyřešení incidentů.
- **Typy údržby**: Opravná (hledání chyb), adaptivní (změna prostředí), zdokonalovací (nové funkce) a preventivní (předcházení problémům).
- **Technický dluh**: Nedostatečná kvalita kódu zvyšuje náklady na údržbu.

### [[integrace-aplikaci|Integrace aplikací]]
- **Důvody**: Konsolidace dat a procesů, využití stávajících investic.
- **Integrační styly**:
    - Přenos souborů (dávkové zpracování).
    - Sdílená databáze (rychlá výměna, ale porušuje zapouzdření).
    - Vzdálené volání procedur (synchronní).
    - Zasílání zpráv (Messaging – asynchronní, omezuje lavinový efekt při výpadku).

### [[webove-sluzby-rest-soap|Webové služby a formáty dat]]
- **SOAP**: Robustní průmyslový standard, XML, WSDL.
- **REST**: Datově orientovaný styl, využití HTTP metod (GET, POST, PUT, DELETE), JSON.
- **JSON vs. XML**: JSON je ideální pro GUI a webové aplikace, XML pro složité integrace se silnou typovou kontrolou (XSD).

## Související stránky
- [[implementace]]
- [[softwarova-architektura]]
- [[testovani]]

---
#prednaska #nasazeni #udrzba #integrace #rest #soap #sla #BI-SWI
