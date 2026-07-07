# Revize zdravotnických zařízení

**Shrnutí**: Zadání doménového modelu systému pro správu a plánování pravidelných revizí zdravotnických přístrojů, včetně stavů zařízení a práce technika.

**Zdroje**:

- `domenove-modely/revize-zdravotnickych-zarizeni.md`
- `domenove-modely/dump.md`

**Výskyty tématu**: `12. 6. 2018`, `6. 6. 2019`, `27. 1. 2021`, `19. 6. 2025`

---

tmp

## Zadání doménového modelu

V různých zdravotnických zařízeních jsou zařízení (přístroje), která vyžadují pravidelnou revizi. Datum další revize je evidováno u každého zařízení a četnost revizí je dána konkrétním typem zařízení.

Nové zařízení vždy vyžaduje nejprve úvodní revizi, kterou provádí technik společnosti a následně ji eviduje do systému. Zařízení s platnou revizí jsou přesně měsíc před koncem platnosti označena k revizi, aby jejich kontrolu mohl technik včas naplánovat. Technik v systému spravuje svůj seznam návštěv a zjišťuje, co musí daný den udělat.

Pokud se revize nestihne provést včas, je označena jako propadlá. Pokud zařízení projde revizí úspěšně, nastaví se datum další revize na nový termín dle typu zařízení. Pokud revizí neprojde, je třeba zařízení s neplatnou revizí nejprve opravit, než jej lze opět začít používat.


## Praktické úkoly

### [[domenovy-model|Doménový model]]

- Vytvořte doménový model systému.

### [[diagram-aktivit|Diagram aktivit]]

- Business diagram: zachyťte práci revizního technika v průběhu jednoho pracovního dne.

### [[stavovy-diagram|Stavový diagram]]

- Vytvořte stavový model zachycující všechny stavy, ve kterých se může zdravotnické zařízení/přístroj vyskytnout.

### [[sekvencni-diagram|Sekvenční diagram]]

- Vytvořte sekvenční diagram na scénář, kdy technik chce v systému zjistit seznam návštěv a naplánovat, co musí ten den udělat.

### [[diagram-pripadu-uziti|Diagram případů užití]]

- Varianta A: Nakreslete min. 5 případů užití se zohledněním aktérů technik, zákazník a „systém" (pro automatizované procesy) + detailní textový scénář.
- Varianta B: Popište alespoň 3 případy užití a jejich aktéry.


## Související stránky
- [[domenovy-model|Doménový model]]
- [[diagram-aktivit|Diagram aktivit]]
- [[stavovy-diagram|Stavový diagram]]
- [[sekvencni-diagram|Sekvenční diagram]]
- [[diagram-pripadu-uziti|Diagram případů užití]]
- [[pripady-uziti|Případy užití]]

---
#zkouska #domenovy-model #BI-SWI
