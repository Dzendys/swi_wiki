# Webové služby (REST vs. SOAP)

**Shrnutí**: Technologie pro realizaci vzdálené komunikace mezi systémy pomocí standardizovaných protokolů a datových formátů (XML, JSON).

**Zdroje**:

- `raw/lectures/10.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Webové služby umožňují integraci aplikací běžících na různých platformách a v různých jazycích (zdroj: raw/lectures/10.prednaska.pdf).

## SOAP (Simple Object Access Protocol)
Robustní průmyslový standard pro výměnu strukturovaných informací.

- **Protokol**: XML.
- **Popis rozhraní**: WSDL (Web Services Description Language).
- **Vlastnosti**: Mnoho podpůrných standardů, typické pro integraci komplexních podnikových aplikací.
- **Transport**: HTTP, SMTP, JMS a další.

## REST (Representational State Transfer)
Architektonický styl (nikoliv protokol) orientovaný na zdroje.

- **Zdroje**: Každý zdroj (resource) je identifikován unikátním **URI**.
- **Operace**: Využívá standardní HTTP metody pro CRUD operace:
    - **GET**: Retrieve/Read (čtení).
    - **POST/PUT**: Create/Update (vytvoření/změna).
    - **DELETE**: Delete (smazání).
- **Vlastnosti**: Lehčí než SOAP, ideální pro webové aplikace a mobilní klienty.

## Datové formáty

### JSON (JavaScript Object Notation)
Textová notace nezávislá na jazyku.

- **Výhody**: Jednoduché zpracování v JS, úsporný formát.
- **Použití**: Veřejná API, přenos dat pro GUI.

### XML (eXtensible Markup Language)
Hierarchický značkovací jazyk.

- **Výhody**: Snadná definice datových typů (**XSD**), transformace (**XSLT**), dotazování (**XPath/XQuery**).
- **Použití**: Komplexní podnikové integrace.

| Vlastnost | JSON | XML |
| :--- | :--- | :--- |
| **Čitelnost** | Vysoká (stručný) | Střední (ukecaný) |
| **Typování** | Slabé | Silné (XSD) |
| **Transformace** | Obtížnější | Snadná (XSLT) |

## Související stránky

- [[integrace-aplikaci]]
- [[komponenty-a-rozhrani]]

---
#rest #soap #xml #json #web-services #api #BI-SWI
