# Sesje (sessions/)

## Cel

Ustrukturyzowane podsumowania znaczących rozmów z AI. Każda sesja łapie kontekst, co zostało zaobserwowane, co zinterpretowane (jako hipoteza) i co zostaje otwarte.

Sesje są **podstawową bazą dowodów** dla wszystkiego w `patterns/` i `psychological-map.md`. Gdy wpis w tych plikach cytuje źródło, prawie zawsze cytuje plik sesji.

**Sesje są tymczasowymi dokumentami roboczymi.** Ważne odkrycia powinny ostatecznie migrować do `psychological-map.md` przez ścieżkę promocji (`patterns/` → mapa). Pliki sesji pozostają jako dowody po migracji.

## Reguły aktualizacji

- Pliki sesji twórz komendą `log-session` — pełny szablon w `.ai/commands/log-session.md`.
- Nazwa pliku: `RRRR-MM-DD-<krótki-kebab-temat>.md`. Powtórki tego samego dnia dostają `-2`, `-3` itd.
- **Oddzielaj obserwację od interpretacji** w pliku. To najważniejsza reguła tego szablonu.
- Dodaj jednolinijkowy wpis do `.ai/session-log.md` dla każdej nowej sesji.
- Sesji nie edytuje się po fakcie — z wyjątkiem literówek i dodania linku do późniejszej sesji, która podejmuje wątek. Jeśli interpretacja z sesji okaże się błędna, jest to zapisywane w *nowej* sesji, nie przez przepisanie starej.

## Streszczenie szablonu

Pełny szablon żyje w `.ai/commands/log-session.md`. Wymagane sekcje:

- Kontekst
- Obserwacje
- Wglądy (oznaczone jako hipotezy, z poziomem pewności)
- Otwarte pytania
- Możliwe aktualizacje mapy
- Linki

## Czego ten katalog NIE jest

- Nie jest dziennikiem — dzienniki idą do `journal/`.
- Nie jest listą zadań.
- Nie jest miejscem na wyniki eksperymentów — te idą do pliku eksperymentu w `experiments/`.
