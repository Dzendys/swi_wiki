# 08. Implementace

**Shrnutí**: Tato přednáška se věnuje fázi implementace, objektovému paradigmatu, pravidlům pro psaní čistého kódu a technikám refaktoringu.

**Zdroje**:

- `raw/lectures/08.prednaska.pdf`

**Naposledy aktualizováno**: 2026-05-08

---

Implementace je klíčová fáze transformující navržené modely do spustitelného kódu. Je to jediná činnost v projektu, kterou nelze vynechat a která přímo dodává hodnotu zákazníkovi.

## Klíčová témata

### Proces implementace
Přednáška definuje hlavní cíle [[implementace|implementace]], jako jsou funkčnost dle požadavků, použitelnost, stabilita a snadná udržovatelnost. Zahrnuje "návrh v malém", tedy rozhodování o detailech kódu, které musí být v souladu s celkovou architekturou systému.

### Objektové paradigma
Moderní implementace v SWI stojí na [[objektove-paradigma|objektovém paradigmatu]]. Základní principy jako zapouzdření, dědičnost a polymorfismus umožňují stavět komplexní, ale udržitelné systémy. Pro pochopení stavu systému v určitém čase se využívá [[objektovy-diagram|objektový diagram]].

### Clean Code a principy návrhu
Kvalita kódu je zajištěna dodržováním pravidel **[[clean-code|čistého kódu]]**. Mezi klíčové patří SRP (jedna zodpovědnost), DRY (neopakování se), Law of Demeter (omezení vazeb) a LSP (správné využití dědičnosti). Programování proti rozhraní pak umožňuje budoucí rozšiřitelnost.

### Ošetření chyb a logování
Robustní aplikace musí počítat s chybovými stavy. Přednáška rozebírá strategie pro [[osetreni-chyb-a-logovani|ošetření chyb]] (výjimky, chybové kódy) a význam logování na různých úrovních priorit pro diagnostiku a audit provozu.

### Refaktoring
[[refaktoring|Refaktoring]] je proces vylepšování vnitřní struktury kódu bez změny jeho vnějšího chování. Pomáhá odstraňovat "code smells" (např. duplicity, dlouhé metody) a udržovat kód srozumitelný. Nezbytnou podmínkou pro bezpečný refaktoring je existence testů.

## Související stránky

- [[navrh-softwaru]]
- [[navrhovy-model-trid]]
- [[softwarova-architektura]]

---
#prednaska #implementace #clean-code #objektove-orientovane-programování #refaktoring #BI-SWI
