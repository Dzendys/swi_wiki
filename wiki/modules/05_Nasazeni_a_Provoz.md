# Nasazení, provoz a integrace aplikací

**Shrnutí**: Tato sekce se zabývá fázemi po dokončení vývoje – od sestavení a nasazení softwaru přes jeho údržbu a podporu až po integraci s jinými systémy pomocí webových služeb.

**Zdroje**:

- `wiki/lectures/10-nasazeni-udrzba-a-integrace.md`

**Naposledy aktualizováno**: 2026-05-18

---

## Nasazení aplikace (Deployment)

Proces [[nasazeni-aplikace|nasazení]] začíná sestavením (**buildem**) produktu ze zdrojových kódů.

- **CI/CD (Continuous Integration / Continuous Deployment)**: Automatizovaný proces (pipeline), který při každé změně v kódu spustí testy a (pokud projdou) sestaví a nasadí aplikaci. Cílem je rychlá a spolehlivá dodávka.

- **Kontejnerizace**: Pro zajištění, že aplikace poběží stejně na vývojářském notebooku i na produkčním serveru, se využívají kontejnery (např. Docker).

## Podpora a údržba

Z pohledu celoživotních nákladů na software představuje údržba často tu největší položku (až 70 %). Po nasazení do produkce začíná fáze [[podpora-a-udrzba|podpory a údržby]].

**Úrovně podpory (SLA - Service Level Agreement)**:

- **L1 (Helpdesk)**: První kontakt s uživatelem, řešení základních dotazů.

- **L2**: Techničtější podpora, konfigurace, řešení známých chyb.

- **L3**: Samotní vývojáři aplikace, oprava složitých chyb v kódu.

**Typy údržby**:

1. **Opravná (Korektivní)**: Opravy chyb objevených v produkci.

2. **Adaptivní**: Reakce na změny v okolí (nová verze operačního systému, nová legislativa jako EET/GDPR).

3. **Zdokonalovací (Perfektivní)**: Přidávání nových funkcí na žádost uživatelů (tvoří většinu údržby).

4. **Preventivní**: Zlepšování vnitřní kvality (refaktoring), aby se předešlo budoucím chybám.

## Integrace aplikací

Většina firemních systémů nefunguje izolovaně, ale potřebuje sdílet data s ostatními ([[integrace-aplikaci|integrace]]).

Základní integrační styly:

- **Přenos souborů**: Typicky asynchronní a dávkové dávkové (např. exporty přes noc). Náchylné na chyby formátu.

- **Sdílená databáze**: Aplikace čtou a zapisují do jedné DB. Rychlé, ale vytváří extrémní svázanost (Coupling).

- **Vzdálené volání procedur (RPC)**: Synchronní komunikace "point-to-point". Pokud protistrana neodpovídá, systém čeká.

- **Zasílání zpráv (Messaging)**: Asynchronní komunikace přes fronty (Message Broker). Systémy jsou volně vázané a výpadky neblokují ostatní.

## Webové služby

Moderní standard pro RPC komunikaci po síti.

- **[[webove-sluzby-rest-soap|SOAP (Simple Object Access Protocol)]]**: Klasický, robustní standard. Komunikuje přes **XML** a má přísný kontrakt popsaný přes **WSDL**. Vhodný pro enterprise systémy a banky.

- **[[webove-sluzby-rest-soap|REST (Representational State Transfer)]]**: Architektonický styl postavený nad protokolem **HTTP** (využívá metody GET, POST, PUT, DELETE). Nejčastěji přenáší data ve formátu **JSON**. Lehčí, preferovaný pro webové a mobilní aplikace.

## Další vzory: Persistence dat

Pro efektivní ukládání objektů do relační databáze (Object-Relational Mapping - ORM) definuje [[persistence-dat|persistence]] několik základních vzorů:

- **Table Data Gateway**: Jedna třída pro celou databázovou tabulku (obsahuje metody jako `FindAll`, `Insert`, `Update`).

- **Active Record**: Samotný byznys objekt nese i databázové metody (`customer.Save()`). Vhodné pro menší aplikace (časté v Ruby on Rails, Laravel).

- **Data Mapper**: Kompletní oddělení byznys objektů od databáze. O ukládání a načítání se stará nezávislý mapper. Používá se v komplexních systémech (Hibernate, Entity Framework).

## Související stránky

- [[nasazeni-aplikace]]

- [[podpora-a-udrzba]]

- [[integrace-aplikaci]]

- [[webove-sluzby-rest-soap]]

- [[persistence-dat]]

- [[vrstvy-architektury]]

---
#nasazeni #udrzba #integrace #rest #soap #persistence #BI-SWI