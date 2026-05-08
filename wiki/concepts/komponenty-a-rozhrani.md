# Komponenty a rozhraní

**Shrnutí**: Základní stavební bloky pro modularizaci systému. Komponenta reprezentuje fyzickou, samostatně nasaditelnou část systému, zatímco rozhraní definuje kontrakt pro komunikaci mezi nimi.

**Zdroje**:
- `raw/lectures/07.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

V moderním softwarovém inženýrství je kladen důraz na modularitu a znovupoužitelnost. Toho se dosahuje pomocí komponent a jasně definovaných rozhraní.

## Komponenta (Component)
Komponenta je fyzická část systému, která je **samostatně nasaditelná** (např. soubory `.exe`, `.jar`, `.war`, `.dll`). 
- Má svou vnitřní strukturu (může se skládat z mnoha tříd).
- Je oddělena od ostatních komponent pomocí rozhraní.
- Pro vizualizaci se v UML používá **diagram komponent** (Structural - Component).

## Rozhraní (Interface)
Rozhraní je množina operací, která specifikuje služby poskytované třídou nebo komponentou.
- **Účel**: Odděluje specifikaci ("co") od implementace ("jak"). Tím výrazně **snižuje provázanost** (coupling) mezi částmi systému.
- **Typy rozhraní v UML**:
    - **Nabízené (Provided)**: Rozhraní, které komponenta realizuje (kreslí se jako plné kolečko "lollipop").
    - **Vyžadované (Required)**: Rozhraní, které komponenta potřebuje ke své činnosti (kreslí se jako půlkruh "socket").
- **Způsoby popisu**:
    - `interface` v programovacích jazycích (Java, C#).
    - **WSDL**: Popis rozhraní pro SOAP webové služby.
    - **Swagger/OpenAPI**: Formát pro popis REST API.
    - **Package** v PL/SQL.

## Propojování komponent
Komponenty lze propojovat manuálně přímo ve zdrojovém kódu (méně flexibilní), nebo pomocí principu **[[dependency-injection|Inversion of Control (IoC)]]**.

## Související stránky
- [[softwarova-architektura]]
- [[dependency-injection]]
- [[diagram-balicku]]

---
#swi #komponenty #rozhrani #uml #modularity #BI-SWI
