# Dziennik (journal/)

## Cel

Surowe, nieustrukturyzowane, datowane myśli. Miejsce, do którego rzeczy trafiają *najpierw*, zanim mają kształt.

To miejsce o najmniejszym tarciu w repo. Istnieje po to, żeby obserwacje w ogóle były złapane — polerowanie odbywa się później, w `sessions/`, `patterns/` lub `psychological-map.md`.

Wpisy w dzienniku są **dowodami**, nie faktami i nie wnioskami. Są surowymi obserwacjami, które zasilają wszystko, co dalej.

## Reguły aktualizacji

- **Tylko dopisuj.** Nigdy nie edytuj przeszłego wpisu. Jeśli późniejsza myśl odwraca wcześniejszą, napisz nowy wpis, który to mówi.
- **Datuj każdy wpis.** Jeden plik na dzień: `RRRR/MM/RRRR-MM-DD.md` (rok i miesiąc jako podkatalogi, pełna data w nazwie pliku). Wiele wpisów w jednym pliku dostaje własne nagłówki czasowe.
- **Bez wymogu szablonu.** Punkty, akapity, fragmenty — wszystko OK.
- **Bez presji interpretacji.** To miejsce, w którym można napisać „czułem się dziś nie tak i nie wiem dlaczego", bez obowiązku podania powodu.
- **Bez promocji stąd.** Wpisy z dziennika trafiają do `patterns/` lub `psychological-map.md` tylko przez `analyze-pattern` lub `update-map` — nigdy mimochodem.

## Sugerowana ścieżka pliku

```
journal/RRRR/MM/RRRR-MM-DD.md
```

Np. wpis z 14 czerwca 2026 trafia do `journal/2026/06/2026-06-14.md`. Pełna data zostaje w nazwie pliku, żeby cytaty w `patterns/` i `psychological-map.md` były czytelne także bez kontekstu ścieżki.

Jeśli wiele wpisów w tym samym dniu:

```markdown
## HH:MM

<wpis>

## HH:MM

<inny wpis>
```

## Czego ten katalog NIE jest

- Nie jest miejscem na ustrukturyzowane podsumowania sesji — te idą do `sessions/`.
- Nie jest miejscem na logi eksperymentów — te idą do pliku eksperymentu w `experiments/`.
- Nie jest listą zadań.
