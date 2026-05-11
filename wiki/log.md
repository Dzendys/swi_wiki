# Log změn

## [2026-05-11] Merge: update/refactor-sources
- Bulk source refactoring: removed inline sources `(zdroj: ...)` from all pages in `wiki/`.
- All cited sources were moved to the header `**Zdroje**:` and sorted (lectures and seminars numerically, others alphabetically).
- Removed redundant `**Last updated**:`, as history is tracked in Git.

## [2026-05-11] Merge: style/fix-inheritance-layout
- Reorganizace rozložení obrázků v `mapovani-dedicnosti.md`.
- Obrázky přesunuty až za popisný text s odsazením (newline), aby se zabránilo chybám v zalomení a zachovala se integrita číslovaných seznamů.

## [2026-05-11] Merge: fix/broken-anchor-links
- Oprava nefunkčních kotev (anchor links) v dokumentaci.
- Přidány explicitní kotvy pomocí `{: #id }` do souborů `objektove-paradigma.md`, `softwarova-architektura.md` a `metodiky-vyvoje.md`, aby odpovídaly generovaným odkazům z Obsidianu.

## [2026-05-11] Merge: fix/image-links-format
- Oprava formátu odkazů na obrázky v `mapovani-dedicnosti.md` na Obsidian wikilinky (`![[...]]`), aby byly správně zpracovány pluginem `obsidian-bridge`.

## [2026-05-11] Merge: update/mapovani-dedicnosti-images
- Konverze diagramů mapování dědičnosti z `.ppm` do `.jpg`.
- Integrace obrázků pro **Single Table**, **Concrete Table** a **Class Table Inheritance** do stránky `wiki/concepts/mapovani-dedicnosti.md`.
- Odstranění původních `.ppm` souborů.

## [2026-05-11] Merge: update/fix-changes
- Provedena rozsáhlá sada oprav a vylepšení na základě seznamu `changes.md`.
- **Diagramy (UC, Aktivity, Balíčky, Třídy)**: Reorganizace obrázků, rozdělení do logických bloků, oprava notací a doplnění podrobných popisů dle slidů.
- **Formátování**: Zavedení tabulek pro porovnání chyb (Špatně vs. Dobře) a vynucení zobrazení obrázků vedle sebe. Oprava číslování seznamů a odsazení.
- **Persistence a GoF**: Rozepsání iterací implementace (Builder) a detailní popis mapování datových entit.
- **Čištění**: Odstranění specifických informací o předmětu (BI-SWI) v teorii, smazání doporučené literatury a slangových výrazů (stodynka).
- **Opravy odkazů**: Odstranění spojovníků v zobrazovaných názvech wiki-odkazů.

## [2026-05-09] - Vytvoření indexu přednášek (feat/lectures-index)
- Vytvořena úvodní rozcestníková stránka `wiki/lectures/index.md`.
- Stránka obsahuje seřazený seznam všech 12 přednášek se stručným výtahovým popiskem pro lepší orientaci.
- Aktualizován soubor `wiki/lectures/.pages`, aby se rozcestník objevoval na prvním místě v navigaci.

## [2026-05-09] Merge: refactor/modules-content
- Úspěšně zrefaktorováno 6 modulů (`wiki/modules/`).
- Do textu modulů byly doplněny klíčové definice a informace z přednášek (např. SDLC, FURPS, návrhové vzory, Scrum), aby sloužily jako ucelenější přehled bez nutnosti neustálého prokliku na koncepční stránky.
- Zachován balanc, aby se moduly nepřehltily detaily – hluboké technické znalosti a rozsáhlá vysvětlení zůstávají ve specializovaných konceptech (`wiki/concepts/`).
