# Zahrádkářské kolonie

**Shrnutí**: Zadání doménového modelu systému pro správu elektrických přípojek v zahrádkářském spolku, včetně životního cyklu přípojky a fakturace.

**Zdroje**:

- `domenove-modely/zahradkarske-kolonie.md`
- `domenove-modely/dump.md`

**Výskyty tématu**: `11. 5. 2011`, `30. 5. 2011`, `17. 12. 2014`, `5. 6. 2018`

---

tmp

## Zadání doménového modelu

Namodelujte systém pro správu elektrických přípojek v zahrádkářském spolku. Zahrádkářský spolek je rozdělen na jednotlivé parcely, u kterých se eviduje jejich rozloha a podrobná historie majitelů (tj. od kdy do kdy majitel parcelu vlastnil). Každý majitel parcely musí být zároveň oficiálním členem zahrádkářského spolku. Na parcelách se nacházejí objekty a ke každému objektu náleží elektrická přípojka.

Životní cyklus elektrické přípojky začíná tím, že majitel podá žádost o připojení, čímž přípojka přechází do stavu čekání na připojení. Následně se elektrikář pokusí na přípojku nainstalovat elektroměr a zapojit ji. Pokud se z nějakého důvodu k přípojce nedostane, změní její stav na „nedostupná". V takovém případě musí majitel parcely problém odstranit a nahlásit změnu stavu na „problém odstraněn". Poté se proces opakuje a elektrikář se opětovně pokouší o zapojení. Jakmile se to podaří, je přípojka úspěšně zapojena.

Pro účely fakturace provádí elektrikář (případně pověřená osoba) pravidelné odpočty stavu elektroměru. Tento odpočet zadává prostřednictvím speciální mobilní aplikace, ze které se následně vypočítá výška poplatku za elektřinu. U každého vygenerovaného poplatku (faktury) se eviduje celková částka k úhradě, konkrétní odpočty, na které se poplatek vztahuje (počáteční a koncový stav), a datum splatnosti.

Majitel má povinnost uhradit tento poplatek do data splatnosti na bankovní konto zahrádkářského spolku. Administrativní pracovník pravidelně kontroluje bankovní účet. Není-li poplatek uhrazen do data splatnosti, zašle majiteli upozornění (upomínku). Pokud majitel nezaplatí dlužnou částku ani do jednoho měsíce od odeslání tohoto upozornění, je dán pokyn elektrikáři, aby elektrickou přípojku fyzicky odpojil. Pokud bude chtít majitel v budoucnu přípojku opět zapojit, musí nejprve uhradit dlužný poplatek a následně podstoupit celý proces znovu podáním nové žádosti o připojení.

Systém využívá běžný uživatel (majitel) skrze webové rozhraní, zatímco servisní technik (elektrikář) se připojuje přes dedikovanou mobilní aplikaci.


## Praktické úkoly

### [[domenovy-model|Doménový model]]

- Nakreslete analytický doménový model tříd.

### [[diagram-aktivit|Diagram aktivit]]

- Nakreslete diagram aktivit (kdo za co zodpovídá / swimlanes) zachycující procesy podání žádosti o připojení, platbu a případné odpojení.

### [[stavovy-diagram|Stavový diagram]]

- Nakreslete diagram stavů elektrické přípojky, včetně zachycení událostí a podmínek, na základě kterých ke změnám dochází.

### [[diagram-pripadu-uziti|Diagram případů užití]]

- **Varianta A**: Nakreslete use case diagram s alespoň 7 příklady užití a použijte `<<include>>` a `<<extend>>`.
- **Varianta B**: Nakreslete diagram s alespoň 3 aktéry a 6 případy užití (včetně include/extend).
- **Varianta C**: 6 případů užití pro 3 různé aktéry (od každého 2), kde složitější diagramy nahradí psaný scénář.

## Související stránky
- [[domenovy-model|Doménový model]]
- [[diagram-aktivit|Diagram aktivit]]
- [[stavovy-diagram|Stavový diagram]]
- [[diagram-pripadu-uziti|Diagram případů užití]]
- [[pripady-uziti|Případy užití]]

---
#zkouska #domenovy-model #BI-SWI
