# Komponenty a rozhraní

**Shrnutí**: Základní stavební bloky pro modularizaci systému. Komponenta reprezentuje fyzickou, samostatně nasaditelnou část systému, zatímco rozhraní definuje kontrakt pro komunikaci mezi nimi.

**Zdroje**:
- `raw/lectures/07.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

V moderním softwarovém inženýrství je kladen důraz na modularitu a znovupoužitelnost. Toho se dosahuje pomocí komponent a jasně definovaných rozhraní.

![|x250](imgs/07.prednaska-011.jpg)
*Obrázek: Základní UML notace pro komponentu a rozhraní (stereotyp «interface»).*

## Komponenta (Component)
Komponenta je fyzická část systému, která je **samostatně nasaditelná** (např. soubory `.exe`, `.jar`, `.war`, `.dll`). 
- Má svou vnitřní strukturu (může se skládat z mnoha tříd).
- Je oddělena od ostatních komponent pomocí rozhraní.
- Pro vizualizaci se v UML používá **diagram komponent** (Structural - Component).

## Rozhraní (Interface)
Rozhraní je množina operací, která specifikuje služby poskytované třídou nebo komponentou.
- **Účel**: Odděluje specifikaci ("co") od implementace ("jak"). Tím výrazně **snižuje provázanost** (coupling) mezi částmi systému.

![|x250](imgs/07.prednaska-015.jpg)
*Obrázek: Vztah realizace mezi konkrétní třídou a rozhraním.*

- **Typy rozhraní v UML**:
    - **Nabízené (Provided)**: Rozhraní, které komponenta realizuje (kreslí se jako plné kolečko "lollipop").
    - **Vyžadované (Required)**: Rozhraní, které komponenta potřebuje ke své činnosti (kreslí se jako půlkruh "socket").

![|x250](imgs/07.prednaska-013.jpg)
*Obrázek: Znázornění nabízeného rozhraní, vyžadovaného rozhraní a jejich sestavení (assembly).*

## Architektura založená na komponentách
Použití komponent a rozhraní umožňuje vytvářet čistou architektura, kde jsou jednotlivé vrstvy a moduly propojeny přes kontrakty (rozhraní).

![|x350](imgs/07.prednaska-017.jpg) ![|x350](imgs/07.prednaska-019.jpg)
*Obrázek: Komplexní diagram komponent a detailní specifikace metod v rozhraních.*

## Propojování komponent
Komponenty lze propojovat manuálně přímo ve zdrojovém kódu (méně flexibilní), nebo pomocí principu **[[dependency-injection|Inversion of Control (IoC)]]**. V tomto případě třída nezávisí na konkrétní implementaci, ale na abstraktním rozhraní.

![|x350](imgs/07.prednaska-022.jpg)
*Obrázek: Závislost na rozhraní (ICtenarDAO) namísto konkrétní implementace.*

## Související stránky
- [[softwarova-architektura]]
- [[dependency-injection]]
- [[diagram-balicku]]

---
#swi #komponenty #rozhrani #uml #modularity #BI-SWI
