# Softwarová architektura

**Shrnutí**: Rozdělení systému na menší, udržovatelné a nezávislé části (komponenty, vrstvy, balíčky) a definice jejich vzájemné komunikace za účelem zajištění srozumitelnosti, rozšiřitelnosti a snadné údržby.

**Zdroje**:
- `raw/lectures/05.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Návrh architektury je ústředním bodem [[navrh-softwaru|návrhu softwaru]]. Zaměřuje se na identifikaci míst, kde bude systém rozšiřován (nestabilní části). Tato místa je nutné izolovat od zbytku systému (např. pomocí rozhraní, zapouzdření), aby jejich změny neměly plošný dopad. Cílem je minimalizovat dopady změn, izolovat externí závislosti a umožnit souběžnou práci více týmů.

Architekturu lze zkoumat ze dvou základních pohledů:

## Logická architektura
Zabývá se organizací zdrojových kódů a konceptuálních celků:
- **Organizace**: Sdružování softwarových tříd do balíčků (packages) a jmenných prostorů (namespaces).
- **Vrstvy a podsystémy**: Uspořádání balíčků do vyšších logických celků (např. prezentační vrstva, aplikační logika, datová vrstva). Pro vizualizaci se používá [[diagram-balicku|diagram balíčků]].

## Fyzická architektura (Nasazení)
Zabývá se rozložením běžícího softwaru na fyzický hardware:
- **Komponenty**: Rozdělení systému na nasaditelné jednotky (např. knihovny, spustitelné soubory, kontejnery).
- **Výpočetní uzly**: Určení, na kterých strojích komponenty poběží. Rozhoduje se například mezi architekturou tenkého klienta (většina logiky na serveru), tlustého klienta (významná část logiky na straně uživatele) a využitím aplikačních clusterů.

## Využití návrhových vzorů
Návrh architektury by neměl znovu "vymýšlet kolo". Pro řešení opakujících se architektonických a návrhových problémů se využívají osvědčené **návrhové vzory** (Design Patterns, např. ze skupiny GoF). Příkladem je vzor *Stavitel (Builder)* pro flexibilní konstrukci složitých objektů (např. sestavování SQL skriptů nezávisle na konkrétním dialektu relační databáze).

## Související stránky
- [[navrh-softwaru]]
- [[diagram-balicku]]
- [[navrhovy-model-trid]]

---
#swi #architektura #nasazeni #design-patterns #BI-SWI
