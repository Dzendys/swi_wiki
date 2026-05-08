# Integrace aplikací

**Shrnutí**: Propojení izolovaných softwarových systémů za účelem sdílení dat a funkcí a konsolidace firemních procesů.

**Zdroje**:
- `raw/lectures/10.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Integrace aplikací řeší problém izolovaných "ostrovů informací". Umožňuje pružně reagovat na změny v businessu bez nutnosti vytvářet jednu obří aplikaci, která umí vše (zdroj: raw/lectures/10.prednaska.pdf).

## Důvody pro integraci
- **Konsolidace dat**: Jednotný pohled na data napříč organizací.
- **Využití investic**: Propojení starších (legacy) systémů s novými.
- **Pružnost**: Snazší úprava dílčích částí než celého monolitu.

## Problémy integrace
Integrace přináší nové výzvy: nespolehlivost sítě, pomalá komunikace, různé datové formáty a programovací jazyky, a velké dopady při změně rozhraní jedné z aplikací.

## Integrační styly
Základní přístupy k propojení systémů (dle Gregora Hohpea):
1.  **Přenos souborů (File Transfer)**: Jeden systém soubor vyprodukuje, druhý ho načte. Typické pro dávkové zpracování.
2.  **Sdílená databáze (Shared Database)**: Rychlá výměna dat, ale riziko porušení [[objektove-paradigma#Zapouzdření|zapouzdření]] a problém se zamykáním záznamů při změnách schématu.
3.  **Vzdálené volání procedur (RPC)**: Synchronní volání funkcí jiného systému přes rozhraní.
4.  **Zasílání zpráv (Messaging)**: Asynchronní komunikace přes zprostředkovatele. Systémy nemusí být dostupné současně, což omezuje "lavinový efekt" při výpadku jedné služby.

## Související stránky
- [[webove-sluzby-rest-soap]]
- [[softwarova-architektura]]
- [[komponenty-a-rozhrani]]

---
#integration #enterprise-integration-patterns #messaging #rest #soap #BI-SWI
