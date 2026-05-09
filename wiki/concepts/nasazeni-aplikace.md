# Nasazení aplikace

**Shrnutí**: Proces sestavení produktu ze zdrojových kódů a jeho přenosu do cílového prostředí k užívání.

**Zdroje**:

- `raw/lectures/10.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Nasazení (Deployment) je fáze, kdy se z vytvořeného kódu stává produkt připravený pro koncového uživatele (zdroj: raw/lectures/10.prednaska.pdf).

## Sestavení produktu (Build)
Před nasazením musí být produkt "sestaven". To obvykle zahrnuje stažení knihoven v požadovaných verzích, kompilaci, spuštění testů a reporting.

- **Nástroje**:
    - **Java**: Maven, Gradle.
    - **JavaScript**: npm, yarn.
- **Výstupy sestavení**:
    - Samostatný balíček (např. SpringBoot JAR s vloženým serverem).
    - Balíček pro aplikační server (WAR, EAR).
    - Instalační balíček pro OS (.exe, .deb).
    - Obraz kontejneru (Docker).

## Způsoby nasazení

### 1. Manuální nasazení
Administrátor ručně kopíruje soubory a provádí konfiguraci (např. připojení k databázi).

- **Nevýhody**: Nespolehlivost, riziko lidské chyby, obtížná opakovatelnost.

### 2. Automatické nasazení (CI/CD)
Nasazení je součástí automatizované **pipeline**. 

- **Výhody**: Minimalizace rizik, rychlost, stejný proces pro všechna prostředí.
- **Technologie**: SCP/SSH kopírování, nahrávání do registru kontejnerů (OKD, Kubernetes).
- **Konfigurace**: Specifické parametry pro prostředí (logy, DB linky) jsou uloženy jako **proměnné prostředí**.

## Související stránky

- [[implementace]]
- [[testovani]]
- [[podpora-a-udrzba]]

---
#deployment #build #maven #cicd #automation #BI-SWI
