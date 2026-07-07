# Internetové bankovnictví

**Shrnutí**: Zadání doménového modelu systému pro pokročilé internetové bankovnictví malých podniků, zahrnující správu účtů, platební příkazy, disponenty a historii transakcí. Jedno z nejobsáhlejších a nejnáročnějších zkouškových témat.

**Zdroje**:

- `domenove-modely/intenetove-bankovnictvi.md`
- `domenove-modely/dump.md`

**Výskyty tématu**: `4. 2. 2015`, `20. 5. 2015`, `13. 1. 2016`, `22. 5. 2018`, `8. 6. 2023`, `5. 6. 2025`

---

tmp

## Zadání doménového modelu

Namodelujte systém pro pokročilé Internetové bankovnictví, které je určeno malým podnikům. Internetové bankovnictví musí umožňovat spravovat více účtů, které má klient v bance vedeny. Každý z těchto účtů je identifikován svým číslem. Aplikace je určena pro jednu banku, není možné v ní spojit účty z různých bank. Pro každý účet má jeho majitel (u kterého banka eviduje jméno, příjmení a rodné číslo) možnost nastavit si jeho název a limity. Pro každý účet může mít majitel nastaveno více limitů s různou periodou (např. denní, týdenní a měsíční). Vždy však musí být nastaven alespoň jeden tento limit. Aplikace musí také umožnit zjistit, jak byly tyto limity nastaveny v minulosti (sledovat historii změn nastavení daných limitů). Účet má vždy právě jednoho majitele.

Existuje-li k nějakému účtu více disponentů (osob oprávněných nakládat s účty majitele), pak je nutné sledovat od kdy a do kdy měl daný disponent právo disponovat s daným účtem. Disponent může zadávat platební příkazy a zobrazovat si pohyby na účtu, nemůže však měnit nastavení limitů na účtu ani jejich názvy (to může vždy pouze majitel).

Nastavení přístupů do internetového bankovnictví pro klienty (majitele účtů i disponenty) musí provádět zaměstnanec banky na pobočce přes jinou vlastní aplikaci, která není součástí tohoto internetového bankovnictví. Tato aplikace musí umožnit i zablokování a odblokování přístupu daného klienta v případě podezření na zneužití.

V Internetovém bankovnictví musí mít klient možnost zadávat jednorázové platební příkazy. Každý příkaz musí obsahovat minimálně částku, měnu, číslo účtu příjemce, kód banky příjemce a účet majitele, ze kterého mají být peníze zaslány. Volitelně dále variabilní symbol, specifický symbol a konstantní symbol. Platební příkaz může uživatel pouze uložit (v tomto případě nebude bankou dále zpracováván, do doby, než uživatel odešle ke zpracování), případně ho může odeslat do banky ke zpracování. Do banky lze příkaz odeslat pouze v případě, že má vyplněné všechny povinné údaje. Pokud datum splatnosti příkazu je nastaveno na budoucí čas, tak v tomto případě čeká platební příkaz na toto datum. Ve chvíli, kdy toto nastane, banka na jeho základě převede požadovanou částku a stav příkazu se změní na provedený. Pokud v době, kdy má dojít k provedení příkazu, není na účtu dostatek peněz (nebo byl překročen limit), změní se stav příkazu na neprovedený. V tomto stavu zůstává, dokud ho uživatel neodstraní (fyzicky se nesmaže, pouze není zobrazován uživateli) nebo znovu neodešle ke zpracování. Všechny přechody mezi stavy platebního příkazu jsou zaznamenávány do jejich historie, aby bylo možné zjistit, k danému přechodu došlo.

V rámci internetového bankovnictví bude mít uživatel možnost zadávat i trvalé příkazy, u kterých k informacím evidovaným u jednorázových příkazů budou dále evidovány informace o datu zahájení platnosti trvalého příkazu, datumu konce platnosti trvalého příkazu, četnosti provádění (měsíčně/čtvrtletně, ročně, týdně) a pořadové číslo v měsíci, kdy má být transakce uskutečněna. Naopak u tohoto typu příkazů nejsou sledovány informace o jeho stavu (může být pouze aktivní nebo blokovaný) ani datum provedení.

V rámci internetového bankovnictví musí být možné sledovat pohyby na účtu (příchozí a odchozí transakce). V rámci této aplikace musí být možné sledovat nejenom transakce vyvolané platebními příkazy z Internetového bankovnictví, ale i příchozí platby nebo vklady na účet/výběry z účtu na pobočce. Pro každý pohyb musíme znát částku, měnu, datum a popis této transakce. V případě, že odchozí transakce proběhne na základě platebního příkazu podaného přes Internetové bankovnictví, pak musí být tato informace v aplikaci také dohledatelná. V případě, že se jedná o příchozí transakce, pak je sledováno ještě jméno odesílatele a číslo účtu odesílající banky.


## Praktické úkoly

### [[domenovy-model|Doménový model]]

- Vytvořte analytický doménový model, nutno popsat všechny hrany a násobnosti.

### [[diagram-aktivit|Diagram aktivit]]

- Nakreslete diagram aktivit procesu vytvoření a zpracování jednorázového platebního příkazu (diagram musí znázorňovat i stavy objektů, swimlanes nejsou nutné).

### [[stavovy-diagram|Stavový diagram]]

- Popsat stavový diagram jednorázového platebního příkazu k úhradě včetně všech popisů přechodů a podmínek.

### [[sekvencni-diagram|Sekvenční diagram]]

- Varianta A: Vypočítání zůstatku na účtu k danému datu s využitím metod `vratKonto(mesic)`, `vratPohyby()` a `vratCastku()` volaných na polymorfní Transakci.
- Varianta B: Sekvenční diagram pro metodu `vratZustatek(datum)`, k dispozici jsou metody `vratPohyby()` na třídě Účet a `vratCastku()` na třídě Transakce.

### [[diagram-pripadu-uziti|Diagram případů užití]]

- Model případů užití: identifikovat aktéry, min. 5 UC. Důležité je použít hranice systému (boundaries) pro odlišení toho, co se dělá v Internetovém bankovnictví, a toho, co v aplikaci na pobočce.


## Související stránky
- [[domenovy-model|Doménový model]]
- [[diagram-aktivit|Diagram aktivit]]
- [[stavovy-diagram|Stavový diagram]]
- [[sekvencni-diagram|Sekvenční diagram]]
- [[diagram-pripadu-uziti|Diagram případů užití]]
- [[pripady-uziti|Případy užití]]

---
#zkouska #domenovy-model #BI-SWI
