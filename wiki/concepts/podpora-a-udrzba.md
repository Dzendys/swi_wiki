# Podpora a údržba

**Shrnutí**: Činnosti spojené s provozem systému po jeho dodání, zahrnující řešení incidentů, opravy chyb a přizpůsobování systému novým potřebám.

**Zdroje**:

- `raw/lectures/10.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Fáze podpory a údržby je typicky mnohem delší než samotný vývojový projekt. Je to stabilní, běžná činnost zajišťující firmě pravidelné příjmy (zdroj: raw/lectures/10.prednaska.pdf).

## Úrovně podpory
Pro efektivní řešení problémů se podpora dělí na úrovně (tiers):
1.  **1. úroveň (L1)**: Komunikace se zákazníkem, identifikace příčiny, řešení pomocí znalostní báze. Vyřeší většinu běžných problémů.
2.  **2. úroveň (L2)**: Technická úroveň, hlubší znalost produktu. Často tvořena členy vývojového týmu.
3.  **3. úroveň (L3)**: Experti v dané oblasti, řeší nejvíce obtížné případy vyžadující např. opravu přímo v kódu.

## SLA (Service Level Agreement)
Smluvní garance provozních parametrů mezi dodavatelem a zákazníkem. Typicky obsahuje:
- **Dostupnost systému** (např. 99.9 %).
- **Rychlost zahájení řešení** incidentu.
- **Doba pro vyřešení** (v závislosti na prioritě: P1 – kritická, P2 – omezení, P3 – ostatní).

## Klasifikace údržby
1.  **Opravná (Corrective)**: Hledání a opravy chyb reportovaných uživateli.
2.  **Adaptivní (Adaptive)**: Udržování v měnícím se prostředí (nový HW, verze OS, legislativní změny).
3.  **Zdokonalovací (Perfective)**: Rozšiřování funkcí, zlepšování výkonu nebo udržovatelnosti.
4.  **Preventivní (Preventive)**: Opravy chyb dříve, než se projeví u zákazníka.

## Nutná prostředí a data
Pro bezpečné provádění údržby je nutná existence více oddělených prostředí: **Vývojové** (dev), **Testovací** (test), **Produkční** (prod) a případně školicí.
- **Testovací data**: Musí být reprezentativní, ale zároveň v souladu s **GDPR** (nutná **anonymizace** citlivých údajů). Příliš velká data mohou být problémem pro výkonnostní testy.

## Související stránky
- [[nasazeni-aplikace]]
- [[testovani]]
- [[zajisteni-kvality]]

---
#maintenance #support #sla #gdpr #environments #BI-SWI
