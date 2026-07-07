Tady je slíbený přehled sjednocených zadání napříč všemi hlavními tématy ve formátu JSON. Jak jste požadoval, teoretické otázky jsou zcela odstraněny a struktura se zaměřuje pouze na to nejdůležitější – tedy praktické úkoly a konkrétní varianty diagramů. 

```json
[
  {
    "tema": "Letní tábory",
    "prakticka_cast": {
      "domenovy_model": [
        "Vytvořte analytický doménový model, včetně popisu vazeb a násobností."
      ],
      "diagram_aktivit": [
        "Nakreslete diagram aktivit se swimlines (zónami zodpovědnosti) pro proces přihlášení účastníka na tábor."
      ],
      "stavovy_diagram": [
        "Varianta A: Nakreslete stavový diagram zachycující stavy ubytovacího zařízení.",
        "Varianta B: Nakreslete stavový diagram zachycující stavy přihlášky účastníka během celého procesu přihlášení."
      ],
      "sekvencni_diagram": [
        "Varianta A: Vytvořte sekvenční diagram pro výpočet celkového počtu lůžek na táboře.",
        "Varianta B: Vytvořte sekvenční diagram pro implementaci funkce vratCelkovouKapacituTabora() třídy Tábor. Předpokládejte, že třída Tábor již obsahuje metodu vratVsechnaUbytovaciZarizeni().",
        "Varianta C: Vytvořte nespecifikovaný sekvenční diagram (obecně)."
      ],
      "use_case_diagram": [
        "Varianta A: Vytvořte model případů užití. Zaznamenejte alespoň 5 případů užití a použijte vazby <<extend>> a <<include>>.",
        "Varianta B: Zaznamenejte všechny aktéry, min. 5 případů užití a podrobně rozepište případ 'Přihlášení účastníka na tábor' (hlavní i alternativní scénář)."
      ]
    }
  },
  {
    "tema": "Zahrádkářské kolonie (správa elektrických přípojek)",
    "prakticka_cast": {
      "domenovy_model": [
        "Nakreslete analytický doménový model tříd."
      ],
      "diagram_aktivit": [
        "Nakreslete diagram aktivit (kdo za co zodpovídá / swimlanes) zachycující procesy podání žádosti o připojení, platbu a případné odpojení."
      ],
      "stavovy_diagram": [
        "Nakreslete diagram stavů elektrické přípojky, včetně zachycení událostí a podmínek, na základě kterých ke změnám dochází."
      ],
      "use_case_diagram": [
        "Varianta A: Nakreslete use case diagram s alespoň 7 příklady užití a použijte <<include>> a <<extend>>.",
        "Varianta B: Nakreslete diagram s alespoň 3 aktéry a 6 případy užití (včetně include/extend).",
        "Varianta C: 6 případů užití pro 3 různé aktéry (od každého 2), kde složitější diagramy nahradí psaný scénář."
      ],
      "diagram_nasazeni": [
        "Varianta A: Databáze běží na serveru, běžný uživatel se připojuje přes webové rozhraní a servisní technik přes speciální aplikaci.",
        "Varianta B: Databáze je na fyzicky odděleném serveru, technik používá mobilní aplikaci komunikující se serverem přes IRM, klienti jdou přes prohlížeč.",
        "Varianta C: Aplikace běží na serveru Glassfish v Javě, fyzicky oddělená DB, technik má aplikaci na OS Android."
      ]
    }
  },
  {
    "tema": "Internetový obchod (E-shop)",
    "prakticka_cast": {
      "domenovy_model": [
        "Vytvořte analytický doménový model."
      ],
      "diagram_aktivit": [
        "Nakreslete diagram aktivit se swimlines, který zachycuje proces objednání zboží a zpracování objednávky zaměstnancem až po doručení."
      ],
      "stavovy_diagram": [
        "Nakreslete stavový diagram objednávky se všemi podmínkami a akcemi, které přechod spustí."
      ],
      "use_case_diagram": [
        "Varianta A: Vytvořte 5 UC pro různé aktéry a ke každému doplňte větu s krátkým popisem.",
        "Varianta B: Vytvořte dohromady 6 UC pro alespoň 2 různé aktéry."
      ],
      "diagram_nasazeni": [
        "Model nasazení: E-shop běží na PHP nad Apachem, DB je MySQL na stejném stroji, server komunikuje přes protokol SOAP s dopravní společností (notifikace)."
      ]
    }
  },
  {
    "tema": "Internetové bankovnictví",
    "prakticka_cast": {
      "domenovy_model": [
        "Vytvořte analytický doménový model, nutno popsat všechny hrany a násobnosti."
      ],
      "diagram_aktivit": [
        "Nakreslete diagram aktivit procesu vytvoření a zpracování jednorázového platebního příkazu (diagram musí znázorňovat i stavy objektů, swimlanes nejsou nutné)."
      ],
      "stavovy_diagram": [
        "Popsat stavový diagram jednorázového platebního příkazu k úhradě včetně všech popisů přechodů a podmínek."
      ],
      "sekvencni_diagram": [
        "Varianta A: Vypočítání zůstatku na účtu k danému datu s využitím metod vratKonto(mesic), vratPohyby() a vratCastku() volaných na polymorfní Transakci.",
        "Varianta B: Sekvenční diagram pro metodu vratZustatek(datum), k dispozici jsou metody vratPohyby() na třídě Účet a vratCastku() na třídě Transakce."
      ],
      "use_case_diagram": [
        "Model případů užití: identifikovat aktéry, min. 5 UC. Důležité je použít hranice systému (boundaries) pro odlišení toho, co se dělá v Internetovém bankovnictví, a toho, co v aplikaci na pobočce."
      ]
    }
  },
  {
    "tema": "Zdravotní pojišťovny (konta, karty a e-recepty)",
    "prakticka_cast": {
      "domenovy_model": [
        "Vytvořte doménový model."
      ],
      "diagram_aktivit": [
        "Nakreslete diagram aktivit při vyzvedávání léků v lékárně. Nezapomeňte na zanesení procesu autorizace uživatele (kartou či heslem)."
      ],
      "stavovy_diagram": [
        "Nakreslete stavový diagram předpisu. V případě, že lékárník nabízí alternativní lék, je nutné toto brát jako speciální stav."
      ],
      "use_case_diagram": [
        "Napište 5 případů užití, použijte alespoň jednou <<include>> a <<extend>>, jeden ze scénářů detailně rozepište."
      ],
      "diagram_nasazeni": [
        "Server běží jako webová aplikace na Oracle Application Serveru (oddělený od DB Oracle Database 11g). Lékař/lékárna má PC se softwarem napojeným na čtečku karet přes RS485. PC pak se serverem komunikuje přes IPSec."
      ]
    }
  },
  {
    "tema": "Revize zdravotnických zařízení",
    "prakticka_cast": {
      "domenovy_model": [
        "Vytvořte doménový model systému."
      ],
      "diagram_aktivit": [
        "Business diagram: zachyťte práci revizního technika v průběhu jednoho pracovního dne."
      ],
      "stavovy_diagram": [
        "Vytvořte stavový model zachycující všechny stavy, ve kterých se může zdravotnické zařízení / přístroj vyskytnout."
      ],
      "sekvencni_diagram": [
        "Vytvořte sekvenční diagram na scénář, kdy technik chce v systému zjistit seznam návštěv a naplánovat, co musí ten den udělat."
      ],
      "use_case_diagram": [
        "Varianta A: Nakreslete min. 5 případů užití se zohledněním aktérů technik, zákazník a 'systém' (pro automatizované procesy) + detailní textový scénář.",
        "Varianta B: Popište alespoň 3 případy užití a jejich aktéry."
      ]
    }
  },
  {
    "tema": "Fakultní ankety",
    "prakticka_cast": {
      "domenovy_model": [
        "Vytvořte doménový model popsané části systému."
      ],
      "diagram_aktivit": [
        "Nakreslete diagram aktivit se swimlines zachycující proces přípravy a průběhu/životního cyklu ankety (do diagramu zahrňte stavy ze stavového diagramu)."
      ],
      "stavovy_diagram": [
        "Nakreslete stavový diagram ankety se všemi podmínkami a akcemi, které daný přechod spustí."
      ],
      "sekvencni_diagram": [
        "Vytvořte sekvenční diagram pro získání statistiky hodnocení dané ankety."
      ],
      "use_case_diagram": [
        "Varianta A: Nalezněte všechny účastníky a uveďte alespoň 5 případů užití.",
        "Varianta B: Jmenujte a popište alespoň 3 případy užití systému a jejich aktéry."
      ],
      "komponentni_diagram": [
        "Aplikace má 3 komponenty - GUI, CORE, REST_API. GUI komunikuje s CORE pomocí rozhraní SpravaVysledku a SpravaAnkety. REST_API komunikuje s CORE pouze přes SpravaVysledku. SpravaVysledku má implementaci SpravaVysledkuImpl. Zachyťte jako UML diagram (diagram komponent)."
      ]
    }
  }
]
```
