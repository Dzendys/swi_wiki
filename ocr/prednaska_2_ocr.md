# Analýza obrázků - Přednáška 2: Modelování obchodních procesů

Tento dokument obsahuje popis obrázků s prefixem `02.prednaska` získaných z podkladů k přednášce. Popisy jsou doplněny o kontext z odpovídajících slidů PDF prezentace.

## Přehled diagramů a schémat

### 02.prednaska-019.jpg (Slide 14)
**Téma:** Notace Eriksson-Penker
**Popis:** Procesní diagram znázorňující proces výpůjčky knihy v knihovně.
- **Vstup:** Žádost o výpůjčku.
- **Aktivity:** Vyhledání knihy v katalogu, Nalezení exempláře knihy, Záznam o výpůjčce.
- **Objekty:** Katalogová karta, Kniha.
- **Role:** Čtenář (vyhledává), Knihovník (zaznamenává výpůjčku).

### 02.prednaska-021.jpg (Slide 15)
**Téma:** BPMN (Business Process Model and Notation)
**Popis:** Fragment diagramu v notaci BPMN.
- Znázorňuje sekvenci "Vyhledání knihy v katalogu" následovanou aktivitou "Nalezení exempláře knihy".
- Mezi aktivitami je datový objekt "Katalogová karta", který je výstupem první a vstupem druhé aktivity.

### 02.prednaska-023.jpg (Slide 16)
**Téma:** UML Diagram aktivit (Základní proces)
**Popis:** Diagram aktivit se dvěma zónami zodpovědnosti (swimlanes): **Čtenář** a **Knihovník**.
- **Čtenář:** Vyhledá výtisk, předá výtisk a průkazku knihovníkovi, odnese si vypůjčené výtisky.
- **Knihovník:** Převezme výtisky, provede buď vypůjčení nebo vrácení (paralelní větve/rozhodování).

### 02.prednaska-030.jpg (Slide 21)
**Téma:** Řídící uzly (Control Nodes)
**Popis:** Legenda symbolů používaných v diagramech aktivit:
- Počáteční uzel (plné kolečko).
- Koncový uzel (kolečko s tečkou).
- Rozhodovací/slučovací uzel (kosočtverec).
- Paralelní souběh (fork/join - silná čára).
- Konec toku (kolečko s křížkem).

### 02.prednaska-028.jpg (Slide 20)
**Téma:** Akční uzly (Action Nodes)
**Popis:** Přehled různých typů akčních uzlů v diagramu aktivit:
- Základní akce (zakulacený obdélník).
- Akce vyvolávající aktivitu (se symbolem trojzubce).
- Odeslání události (pětiboký tvar šipky).
- Přijetí události (tvar vlajky).
- Časová událost (přesýpací hodiny).

### 02.prednaska-032.jpg (Slide 22)
**Téma:** Průchody a podmínky
**Popis:** Dva příklady větvení toku:
1. **Rozhodování:** Akce A vede k rozhodovacímu uzlu, ze kterého jdou větve do B nebo C na základě podmínek, následně se slučují do D.
2. **Paralelismus:** Akce E se dělí (fork) na paralelní větve F a G, které se následně spojují (join) do akce H.

### 02.prednaska-034.jpg (Slide 23)
**Téma:** Zóny zodpovědnosti (Swimlanes)
**Popis:** Ukázka rozdělení diagramu do zón zodpovědnosti. Jsou zde dva sloupce: **Student** a **Učitel**.

### 02.prednaska-036.jpg (Slide 24)
**Téma:** Objektové uzly (Object Nodes) - Varianta 1
**Popis:** Zobrazení toku objektu mezi akcemi. Akce "Vytvoření zadání zkoušky" produkuje objekt `:Test`, který je vstupem pro akci "Vyplnění zkouškového testu".

### 02.prednaska-037.jpg (Slide 24)
**Téma:** Objektové uzly (Object Nodes) - Varianta 2
**Popis:** Alternativní zobrazení toku objektu pomocí "pinů" na okrajích akcí. Mezi piny je vazba s popiskem `Test`.

### 02.prednaska-039.jpg (Slide 25)
**Téma:** Vícenásobné provedení akce (Expansion Region)
**Popis:** Diagram se dvěma swimlanes: **Organizátor průzkumu** a **Účastník průzkumu**.
- Organizátor provede "Přípravu dotazníků".
- Účastník provádí "Vyplnění dotazníku", přičemž aktivita má symbol vícenásobného provedení (tři čtverečky na okraji).
- Následuje "Zpracování dotazníků" organizátorem.

### 02.prednaska-041.jpg (Slide 26)
**Téma:** Přerušení provádění
**Popis:** Region přerušení (přerušitelná oblast).
- Probíhá "Příprava objednávky".
- Pokud nastane "Událost" (cik-cak šipka), region se opustí a provede se "Zrušení objednávky".

### 02.prednaska-043.jpg (Slide 27)
**Téma:** Zachycení stavu objektu
**Popis:** Zobrazení objektových uzlů se specifikací stavu v hranatých závorkách:
- `Název:Třída` v horní části, `[Stav]` ve spodní části.
- `:Třída` (anonymní objekt), `[Stav]` ve spodní části.

### 02.prednaska-045.jpg (Slide 28)
**Téma:** Komplexní diagram aktivit (Rezervace)
**Popis:** Detailní model procesu rezervace knihy se swimlanes Čtenář a Knihovník.
- Zahrnuje podání on-line vs. osobně, zaznamenání požadavku, notifikaci o dostupnosti.
- Obsahuje časovou událost (čekání 3 dny) a stavy objektu Rezervace ([Aktivní], [Dokončená]).

### 02.prednaska-049.jpg (Slide 31)
**Téma:** Typické chyby - Špatné slučování
**Popis:** Ukázka chyby, kdy se dvě větve (z aktivity a zpětná vazba cyklu) spojují přímo do akce "Provedení kontroly" bez použití slučovacího uzlu (kosočtverce). V UML by se taková akce nespustila, protože by čekala na tokeny z obou větví najednou.

### 02.prednaska-051.jpg (Slide 32)
**Téma:** Správné řešení - Slučovací uzel
**Popis:** Oprava předchozí chyby. Před akci "Provedení kontroly" je vložen kosočtverec, který korektně slučuje tok z počátku i z cyklu.

### 02.prednaska-053.jpg (Slide 33)
**Téma:** Typické chyby - Míchání stavů a akcí
**Popis:** Chyba v modelu, kde jsou stavy "Zařízení opraveno" a "Zařízení vyřazeno" použity jako akce (zakulacené obdélníky).

### 02.prednaska-055.jpg (Slide 34)
**Téma:** Správné řešení - Objektové uzly
**Popis:** Oprava předchozí chyby. Jsou použity správné akce ("Vystavení protokolu o opravě", "Vyřazení z evidence") a výsledné stavy jsou zachyceny v objektových uzlech (obdélníky) jako `:Zařízení [Opraveno]` a `:Zařízení [Vyřazeno]`.

---

## Ostatní soubory (PPM)
Soubory ve formátu PPM pravděpodobně odpovídají zbývajícím slidům prezentace, které nebyly exportovány do formátu JPG:
- **02.prednaska-028.ppm:** Pravděpodobně "Akční uzly" (Slide 20).
- **02.prednaska-034.ppm:** Pravděpodobně "Zóny zodpovědnosti" (Slide 23).
- **02.prednaska-036.ppm:** Pravděpodobně "Objektové uzly" (Slide 24).
- **02.prednaska-037.ppm:** Pravděpodobně "Vícenásobné provedení akce" (Slide 25).
- **02.prednaska-043.ppm:** Pravděpodobně "Zachycení stavu objektu" (Slide 27).
