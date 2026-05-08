# 10. Nasazení, údržba a integrace aplikací

**Shrnutí**: Tato přednáška se zabývá závěrečnými fázemi životního cyklu softwaru – od sestavení a nasazení přes podporu a různé typy údržby až po propojení aplikací pomocí integračních stylů a webových služeb.

**Zdroje**:
- `raw/lectures/10.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Přednáška pokrývá provozní aspekty softwaru a jeho začlenění do technologického ekosystému zákazníka po dokončení vývoje.

## Klíčová témata

### Nasazení aplikace
Proces [[nasazeni-aplikace|nasazení]] začíná sestavením (buildem) produktu ze zdrojových kódů. Přednáška vysvětluje přechod od rizikového manuálního nasazování k moderním automatizovaným **CI/CD** procesům (pipeline), které zajišťují opakovatelnost a stabilitu v různých prostředích (dev, test, prod).

### Podpora a údržba
Po nasazení přebírá systém tým [[podpora-a-udrzba|podpory a údržby]]. Přednáška definuje úrovně podpory (L1–L3) a smluvní garance provozu (**SLA**). Dále klasifikuje typy údržby na opravnou (chyby), adaptivní (změna okolí), zdokonalovací (nové funkce) a preventivní (předcházení budoucím problémům).

### Integrace aplikací
Aplikace málokdy fungují izolovaně. [[integrace-aplikaci|Integrace aplikací]] řeší jejich propojení za účelem sdílení dat a procesů. Rozebírají se základní styly jako přenos souborů, sdílená databáze, vzdálené volání procedur a asynchronní zasílání zpráv (Messaging), které zvyšuje robustnost při výpadcích.

### Webové služby (REST vs. SOAP)
V oblasti technické realizace integrací přednáška porovnává robustní standard **SOAP** (postavený na XML a WSDL) s lehčím architektonickým stylem **REST**, který využívá standardní HTTP metody a formát **JSON**. Rozebírají se výhody a typická užití obou přístupů. Podrobnosti viz [[webove-sluzby-rest-soap]].

## Související stránky
- [[implementace]]
- [[softwarova-architektura]]
- [[testovani]]

---
#prednaska #nasazeni #udrzba #integrace #rest #soap #sla #BI-SWI
