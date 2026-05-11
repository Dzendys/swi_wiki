# MVC a MVP

**Shrnutí**: Architektonické vzory pro prezentační vrstvu, které oddělují data (Model) od jejich zobrazení (View) a logiky řízení (Controller/Presenter).

**Zdroje**:

- `raw/lectures/06.prednaska.pdf`



---

Tyto vzory řeší typické problémy [[vrstvy-architektury|prezentační vrstvy]], jako je míchání kódu pro vykreslování GUI s aplikační logikou. Cílem je zvýšit udržovatelnost a umožnit snadnou změnu vzhledu nezávisle na datech.

## MVC (Model-View-Controller)
Původní vzor, kde jsou komponenty provázány takto:

- **Model**: Zapouzdřuje data a business logiku.
- **View**: Zobrazuje data uživateli (čte je z modelu).
- **Controller**: Reaguje na uživatelské vstupy a mění stav modelu.
- **Varianty**:
    - **Aktivní model**: Model upozorňuje View na změny (pomocí vzoru Observer). View se pak samo překreslí.
    - **Pasivní model**: Controller po změně modelu přímo řekne View, aby se aktualizovalo.

## MVP (Model-View-Presenter)
Modernější varianta, která více izoluje View:

- **Model**: Stejný jako v MVC.
- **View**: Je velmi jednoduché (tzv. "hloupé"). Pouze vykresluje komponenty a zachytává události (kliknutí), které okamžitě deleguje na Presenter.
- **Presenter**: Obsahuje logiku řízení. Čte data z modelu a explicitně je "tlačí" do View (např. přes rozhraní).
- **Výhoda**: View lze snadno nahradit mockem a testovat Presenter bez nutnosti spouštět grafické rozhraní.

## Praktické využití
Vzory jsou základem většiny moderních frameworků:

- **Web**: Angular, React, Vue, Spring MVC, ASP.NET Core, Laravel.
- **Desktop**: JavaFX, Swing, .NET WPF.

## Související stránky

- [[vrstvy-architektury]]
- [[softwarova-architektura]]

---
#swi #mvc #mvp #prezentace #architektura #BI-SWI
