# Zdravotní pojišťovna

**Shrnutí**: Zadání doménového modelu systému zdravotní pojišťovny s evidenčními kartami, konty pojištěnců a elektronickými recepty (e-recepty).

**Zdroje**:

- `domenove-modely/zdravotni-pojistvona.md`
- `domenove-modely/dump.md`

**Výskyty tématu**: `15. 6. 2012`, `16. 5. 2014`, `12. 6. 2025` (jako „Elektronická zdravotní karta pacienta")

---

tmp

## Zadání doménového modelu

Vláda v hypotetickém státě se rozhodla, že pro účely zjednodušení plateb za zdravotní péči nařídí zavedení evidenčních karet pro občany tohoto státu. Centrální registr občanů vygeneruje občanům jednoznačné identifikační číslo (tzv. SSN = „Social Security Number"), které bude sloužit při identifikaci transakcí tohoto občana. Pro zabezpečení autentizace si každý občan může zvolit dvě různá hesla. Jedno bude sloužit pro potvrzení správné transakce, druhé jako žádost o pomoc, pokud by byl k transakci nucen proti své vůli.

Každý občan tohoto státu musí mít smlouvu s některou zdravotní pojišťovnou. Pojišťovny přijímají žádosti občanů o uzavření smlouvy. Žádost je možno podat písemně nebo elektronicky. V žádosti jsou uvedena základní data žadatele, volba pojistného programu z nabídky dané pojišťovnou. Pojistné programy mohou být různé, ale základní vyrovnání s občanem se děje přes jeho konto. Tam se evidují platby pojistného, dotace od státu, příspěvky pojišťovny apod.

Každá pojišťovna musí k takto vytvořenému kontu vydávat svým klientům evidenční karty kompatibilní s vybranou (zde blíže nespecifikovanou) technologií pro čtení obsahu karty. Evidenční kartou se občan identifikuje při návštěvě lékaře, při vyzvedávání léků a při komunikaci s pojišťovnou.

Pojištěný občan má právo si nechat vyhotovit přehled transakcí ověřených jeho evidenční kartou. Každé zdravotnické i lékárenské zařízení má právo požádat o ověření evidenční karty pacienta. Při předepisování léčiv se pacientům nevystavuje papírový recept, lékař potřebná léčiva vkládá do záznamů občana-pacienta, spolu s časovým údajem. Pacient si léky může vyzvednout v kterékoliv lékárně, kde se samozřejmě musí identifikovat. Předpisy léků mají omezenou časovou platnost, dle druhu léku. Po jejím uplynutí již lékárna nemusí lék pacientovi vydat. Lékárník také může pacientovi doporučit alternativní medikaci, která se rovněž zaznamená do záznamů občana.


## Praktické úkoly

### [[domenovy-model|Doménový model]]

- Vytvořte doménový model.

### [[diagram-aktivit|Diagram aktivit]]

- Nakreslete diagram aktivit při vyzvedávání léků v lékárně. Nezapomeňte na zanesení procesu autorizace uživatele (kartou či heslem).

### [[stavovy-diagram|Stavový diagram]]

- Nakreslete stavový diagram předpisu. V případě, že lékárník nabízí alternativní lék, je nutné toto brát jako speciální stav.

### [[diagram-pripadu-uziti|Diagram případů užití]]

- Napište 5 případů užití, použijte alespoň jednou `<<include>>` a `<<extend>>`, jeden ze scénářů detailně rozepište.

## Související stránky
- [[domenovy-model|Doménový model]]
- [[diagram-aktivit|Diagram aktivit]]
- [[stavovy-diagram|Stavový diagram]]
- [[diagram-pripadu-uziti|Diagram případů užití]]
- [[pripady-uziti|Případy užití]]

---
#zkouska #domenovy-model #BI-SWI
