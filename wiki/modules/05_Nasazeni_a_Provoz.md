# Nasazení, provoz a integrace aplikací

**Shrnutí**: Tato sekce se zabývá fázemi po dokončení vývoje – od sestavení a nasazení softwaru přes jeho údržbu a podporu až po integraci s jinými systémy pomocí webových služeb.

**Zdroje**:

- `wiki/lectures/10-nasazeni-udrzba-a-integrace.md`

**Naposledy aktualizováno**: 2026-05-18

---

## Nasazení aplikace

Proces [[nasazeni-aplikace|nasazení (Deployment)]] začíná sestavením (**buildem**) produktu ze zdrojových kódů (např. pomocí nástrojů Maven, Gradle či npm). Moderní vývoj preferuje automatizované procesy **CI/CD** (Continuous Integration / Continuous Deployment), které zajišťují stabilitu při přenosu mezi vývojovým, testovacím a produkčním prostředím. Pro izolaci prostředí se často využívá kontejnerizace (Docker).

## Podpora a údržba

Po nasazení přechází systém do fáze [[podpora-a-udrzba|podpory a údržby]]. Podpora se typicky dělí na tři úrovně (**L1–L3**), přičemž parametry provozu (dostupnost, rychlost řešení chyb) jsou definovány v dohodě **SLA (Service Level Agreement)**.

Rozlišujeme čtyři typy údržby:

1. **Opravná**: Opravy nahlášených chyb.
2. **Adaptivní**: Přizpůsobení změnám okolí (nový OS, legislativa).
3. **Zdokonalovací**: Přidávání nových funkcí a optimalizace.
4. **Preventivní**: Předcházení budoucím problémům.

Při údržbě je nutné dbát na bezpečnost dat a soulad s **GDPR** (anonymizace testovacích dat).

## Integrace aplikací

[[integrace-aplikaci|Integrace]] řeší propojení izolovaných systémů za účelem sdílení dat. Mezi základní integrační styly patří:

- **Přenos souborů**: Dávkové zpracování.
- **Sdílená databáze**: Rychlá výměna, ale vysoká provázanost.
- **Vzdálené volání procedur (RPC)**: Synchronní komunikace.
- **Zasílání zpráv (Messaging)**: Asynchronní komunikace přes fronty, která zvyšuje robustnost systému.

## Webové služby

K technické realizaci integrací se využívají [[webove-sluzby-rest-soap|webové služby]]:

- **SOAP**: Robustní protokol využívající XML a WSDL, vhodný pro komplexní podnikové integrace.
- **REST**: Architektonický styl využívající standardní HTTP metody (GET, POST, PUT, DELETE) a formáty jako **JSON**. Je lehčí a preferovaný pro webové a mobilní aplikace.

## Persistence dat

Pro efektivní ukládání objektů do databáze (v rámci [[vrstvy-architektury|datové vrstvy]]) se využívají vzory pro [[persistence-dat|persistenci]]:

- **Table Data Gateway**: Jedna třída pro celou tabulku.
- **Active Record**: Objekt obsahuje data i business logiku (vhodné pro menší systémy).
- **Data Mapper**: Úplné oddělení business objektů od databáze (využívané v moderních ORM jako Hibernate).

## Související stránky

- [[nasazeni-aplikace]]
- [[podpora-a-udrzba]]
- [[integrace-aplikaci]]
- [[webove-sluzby-rest-soap]]
- [[persistence-dat]]
- [[vrstvy-architektury]]

---
#nasazeni #udrzba #integrace #rest #soap #persistence #BI-SWI
