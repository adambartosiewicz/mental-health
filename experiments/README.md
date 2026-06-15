# Eksperymenty (experiments/)

## Cel

Eksperymenty behawioralne — małe, ograniczone czasowo, z góry zarejestrowane testy konkretnych hipotez o tym, jak funkcjonuję. Eksperymenty są drogą, którą interpretacje zamieniają się w wiedzę.

## Reguły aktualizacji

- Pliki eksperymentów twórz komendą `new-experiment` — patrz `.ai/commands/new-experiment.md`.
- Pliki eksperymentów zamykaj komendą `close-experiment` — patrz `.ai/commands/close-experiment.md`.
- Nazwa pliku: `RRRR-MM-DD-<krótka-kebab-nazwa>.md`. Data to dzień, w którym eksperyment **startuje**.
- **Z góry zarejestruj kryteria sukcesu i porażki.** Oba muszą być zapisane przed startem eksperymentu. Definiowanie ich post hoc to droga, którą system zamienia się w samousprawiedliwienie.
- **Ramy czasowe.** Każdy eksperyment ma datę przeglądu.
- **Jedna hipoteza na eksperyment.** Jeśli są dwie, zrób dwa — albo wybierz.
- Pole status w każdym pliku: `aktywny`, `zamknięty`, `wstrzymany`, `porzucony`.
- Porzucony eksperyment też dostaje podsumowanie zamknięcia. *Dlaczego został porzucony* to prawdziwe dane.

## Streszczenie szablonu

Pełny szablon żyje w `.ai/commands/new-experiment.md`. Wymagane sekcje:

- Hipoteza
- Dlaczego to ważne
- Procedura
- Kryteria sukcesu
- Kryteria porażki
- Data przeglądu

Sekcje zamknięcia (dopisywane przez `close-experiment`):

- Wynik
- Co zadziałało
- Co nie zadziałało
- Wnioski
- Aktualizacje mapy psychologicznej (tylko propozycje — faktyczne edycje mapy idą przez `update-map`)

## Czego ten katalog NIE jest

- Nie jest listą celów. Cele są aspiracjami; eksperymenty są testami z falsyfikowalnymi wynikami.
- Nie jest trackerem nawyków. Próba nawyku bez hipotezy i z góry zarejestrowanych kryteriów to nie eksperyment.
