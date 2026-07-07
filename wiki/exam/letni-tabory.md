# Letní tábory

**Shrnutí**: Zadání doménového modelu systému pro organizaci letních táborů, včetně přihlašování účastníků, ubytování a plateb. Jedno z nejčastěji se opakujících zkouškových témat.

**Zdroje**:

- `domenove-modely/letni-tabory.md`
- `domenove-modely/dump.md`

**Výskyty tématu**: `18. 5. 2012`, `24. 5. 2013`, `20. 12. 2013`, `23. 1. 2019`, `7. 6. 2021`, `25. 5. 2023`, `15. 5. 2025`

---

tmp

## Zadání doménového modelu

Namodelujte systém pro podporu organizování letních táborů. Každý tábor musí mít určen datum zahájení, datum ukončení, místo konání, krátký popis a cenu, kterou musí každý účastník zaplatit. Jednotlivá místa, na kterých lze tábor uskutečnit, jsou evidována nezávisle na táborech a při zakládání nového tábora sami vedoucí určí, na kterém místě se bude konat. Systém musí kontrolovat, zda se na vybraném místě v této době nekoná již jiný tábor.

Každý tábor musí mít jednoho hlavního vedoucího tábora, který zodpovídá za celý průběh tábora. Dále má přiřazeny ostatní vedoucí, kteří pomáhají s organizováním činností, které budou na táboře probíhat. U každého vedoucího je evidováno jeho jméno, příjmení, e-mail a přezdívka, která je v rámci systému jedinečná. Na jednoho vedoucího může připadnout maximálně 5 přihlášených účastníků na tábor. U každého účastníka je nutné evidovat jeho jméno, rodné číslo, datum narození, telefon nebo e-mail, pohlaví, adresu bydliště a zákonného zástupce v případě, že nemá občanský průkaz. U každého zákonného zástupce musí být evidovány stejné údaje jako u účastníků. Jedna osoba může být zákonným zástupcem několika účastníků. (Některá zadání uvádějí i detail, že zákonný zástupce může být také účastníkem tábora).

Systém musí umožňovat přihlašování jednotlivých účastníků přímo z domova z jejich počítačů. Je-li účastník v systému již registrován, není nutné při podávání žádosti o přihlášení na tábor zadávat žádné další údaje. Stačí pouze vybrat tábor, kterého se chce zúčastnit. Po závazném přihlášení musí systém účastníkovi zobrazit a vytisknout příkaz k úhradě, který bude obsahovat číslo účtu a kód banky konkrétního tábora, dále variabilní symbol, který odpovídá rodnému číslu účastníka. Při přihlášení musí také systém zkontrolovat, zda je na tábor přiřazeno dostatečné množství vedoucích a není překročena maximální kapacita lůžek tábora. V opačném případě nedovolí účastníkovi závazné přihlášení, žádost účastníka však zůstává nadále evidována (čeká na uvolnění kapacity). Pokud dojde k navýšení kapacity lůžek nebo přihlášení dalších vedoucích, pak jsou automaticky informováni účastníci, kteří si žádost podali a kterým nebylo vyhověno. Nedojde-li platba na táborový účet do deseti dnů ode dne přihlášení na tábor, je závazné přihlášení účastníkovi automaticky zrušeno.

U každého tábora musí být evidována ubytovací zařízení, ve kterých budou účastníci bydlet. Ubytovacím zařízením může být stan, stan s podsadou nebo chatka. Každé ubytovací zařízení má uveden počet lůžek. V případě chatky je počet lůžek dán součtem počtů lůžek na jednotlivých pokojích. Při závazném přihlášení je vždy účastník automaticky přiřazen na konkrétní ubytovací zařízení. Přednostně jsou obsazovány ubytovací zařízení, která jsou již částečně obsazena. Na jednom ubytovacím zařízení nemůžou být ubytování účastníci různých pohlaví.


## Praktické úkoly

### [[domenovy-model|Doménový model]]

- Vytvořte analytický doménový model, včetně popisu vazeb a násobností.

### [[diagram-aktivit|Diagram aktivit]]

- Nakreslete diagram aktivit se swimlines (zónami zodpovědnosti) pro proces přihlášení účastníka na tábor.

### [[stavovy-diagram|Stavový diagram]]

- **Varianta A**: Nakreslete stavový diagram zachycující stavy ubytovacího zařízení.
- **Varianta B**: Nakreslete stavový diagram zachycující stavy přihlášky účastníka během celého procesu přihlášení.

### [[sekvencni-diagram|Sekvenční diagram]]

- **Varianta A**: Vytvořte sekvenční diagram pro výpočet celkového počtu lůžek na táboře.
- **Varianta B**: Vytvořte sekvenční diagram pro implementaci funkce `vratCelkovouKapacituTabora()` třídy Tábor. Předpokládejte, že třída Tábor již obsahuje metodu `vratVsechnaUbytovaciZarizeni()`.
- **Varianta C**: Vytvořte nespecifikovaný sekvenční diagram (obecně).

### [[diagram-pripadu-uziti|Diagram případů užití]]

- **Varianta A**: Vytvořte model případů užití. Zaznamenejte alespoň 5 případů užití a použijte vazby `<<extend>>` a `<<include>>`.
- **Varianta B**: Zaznamenejte všechny aktéry, min. 5 případů užití a podrobně rozepište případ „Přihlášení účastníka na tábor" (hlavní i alternativní scénář).

## Související stránky
- [[domenovy-model|Doménový model]]
- [[diagram-aktivit|Diagram aktivit]]
- [[stavovy-diagram|Stavový diagram]]
- [[sekvencni-diagram|Sekvenční diagram]]
- [[diagram-pripadu-uziti|Diagram případů užití]]
- [[pripady-uziti|Případy užití]]

---
#zkouska #domenovy-model #BI-SWI
