# Internetový obchod (E-shop)

**Shrnutí**: Zadání doménového modelu systému pro internetový obchod, zahrnující správu produktů, košík, objednávky, platby a doručení. Jedno z nejpodrobnějších a nejčastěji opakujících se témat.

**Zdroje**:
- `domenove-modely/eshop.md`
- `domenove-modely/dump.md`

**Výskyty tématu**: 29. 5. 2018 · 23. 5. 2019 · 18. 12. 2019 · 20. 5. 2021 · 5. 1. 2022

---

tmp

## Zadání doménového modelu

Internetový obchod nabízí různé druhy zboží (produktů). Každý produkt je charakterizován svým názvem a popisem. Cena každého produktu se v čase mění a je nutné sledovat aktuální hodnotu i vývoj této ceny v historii. V každém okamžiku může být platná pouze jedna cena, za kterou je produkt nabízen. Není možné prodávat současně jeden produkt za různé ceny.

Produkty jsou zařazeny do kategorií, které se odlišují svým názvem. Kategorie tvoří hierarchickou strukturu, takže jedna kategorie může obsahovat několik podkategorií. Každá kategorie však má maximálně jednu nadřazenou kategorii. Jeden produkt může být zařazen do více kategorií.

Zákazník internetového obchodu (u kterého evidujeme jméno, příjmení, email a adresu) může přidávat jednotlivé produkty do košíku. Pro každou položku v košíku je nutné ukládat informace o množství (počet kusů produktu), které si zákazník přeje koupit, a cenu za každý kus. Platnost košíku je 30 minut od posledního přidání nebo odebrání položky z košíku. Poté je obsah košíku vyprázdněn.

Když si zákazník vloží do košíku veškeré požadované zboží, může provést jeho objednávku. Je nutné zaznamenat datum vytvoření objednávky a také datum poslední změny objednávky. Pro každou objednanou položku je nutné udržovat informaci o její ceně v době vytvoření objednávky bez ohledu na cenu, za kterou se aktuálně zboží nabízí ostatním zákazníkům. Během vytváření objednávky si uživatel zvolí způsob úhrady (bankovním převodem nebo dobírkou) a následně musí potvrdit souhlas s vytvořenou objednávkou. Po potvrzení souhlasu je objednávka považována za vytvořenou a je zpracována pracovníkem obchodu.

Jestliže uživatel zvolil bankovní převod jako typ platby, pak pracovník zašle zákazníkovi informace o požadované platbě, kterými jsou číslo účtu, kód banky, variabilní symbol a částka. Poté čeká objednávka 7 dní na příchod platby v požadované výši a s odpovídajícím variabilním symbolem. V případě, že v této lhůtě nedojde k uhrazení objednávky, je objednávka zrušena.

Když je objednávka uhrazena nebo byla zvolena platba dobírkou, pak je objednávka odeslána k doručení. Přepravní společnost je informována o požadavku na převzetí zásilky přes integrovaný systém. K objednávce je nutné zaznamenat jednoznačný identifikátor doručovaného balíku. Ve chvíli, kdy si přepravní společnost zboží převezme, je v systému evidována objednávka jako doručovaná. Když doručovací společnost doručí balík zákazníkovi, zašle notifikaci do systému o jejím doručení. Jestliže zákazník není na uvedené adrese zastižen nebo nezaplatí za zboží (v případě dobírky), je balík vrácen přepravní společností zpět do internetového obchodu a objednávka je zrušena.


## Praktické úkoly

### [[domenovy-model|Doménový model]]

- Vytvořte analytický doménový model.

### [[diagram-aktivit|Diagram aktivit]]

- Nakreslete diagram aktivit se swimlines, který zachycuje proces objednání zboží a zpracování objednávky zaměstnancem až po doručení.

### [[stavovy-diagram|Stavový diagram]]

- Nakreslete stavový diagram objednávky se všemi podmínkami a akcemi, které přechod spustí.

### [[diagram-pripadu-uziti|Diagram případů užití]]

- **Varianta A**: Vytvořte 5 UC pro různé aktéry a ke každému doplňte větu s krátkým popisem.
- **Varianta B**: Vytvořte dohromady 6 UC pro alespoň 2 různé aktéry.

### Diagram nasazení

- Model nasazení: E-shop běží na PHP nad Apachem, DB je MySQL na stejném stroji, server komunikuje přes protokol SOAP s dopravní společností (notifikace).


## Související stránky
- [[domenovy-model|Doménový model]]
- [[diagram-aktivit|Diagram aktivit]]
- [[stavovy-diagram|Stavový diagram]]
- [[diagram-pripadu-uziti|Diagram případů užití]]
- [[webove-sluzby-rest-soap|Webové služby (REST, SOAP)]]

---
#zkouska #domenovy-model #BI-SWI
