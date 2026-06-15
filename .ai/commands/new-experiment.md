# Command: new-experiment

> **Output language:** Polish. The experiment file must be in Polish, using the template below.

## Purpose

Design a behavioral experiment to test a specific hypothesis about the user's psychology. Experiments turn vague self-narratives into falsifiable, time-boxed tests.

The system prefers experiments over speculation. When an interpretation in `psychological-map.md` or a pattern in `patterns/` is getting load-bearing, design an experiment rather than refining the interpretation further.

## When to invoke

- A pattern has been identified and there is a testable hypothesis about it.
- The user wants to *change* a behavior, not just understand it.
- An interpretation in the map has become load-bearing and needs to be checked against reality.

Do not run an experiment for things that are not testable in everyday life (e.g. "czy jestem dobrym człowiekiem").

## File to create

```
experiments/RRRR-MM-DD-<krótka-kebab-nazwa>.md
```

Status starts at `aktywny`. Update status when reviewed: `zamknięty`, `wstrzymany`, `porzucony`.

## Polish template

```markdown
# Eksperyment: <Nazwa>

**Status:** aktywny
**Rozpoczęty:** RRRR-MM-DD
**Data przeglądu:** RRRR-MM-DD

## Hipoteza
<Pojedyncze, konkretne, falsyfikowalne stwierdzenie. „Jeśli zrobię X w sytuacji Y, to Z się stanie." Nie „chcę się czuć lepiej." Nie „chcę być bardziej towarzyski.">

## Dlaczego to ważne
<Z którym wzorcem, otwartym pytaniem lub wpisem mapy się to łączy. Linkuj do konkretnych plików w `patterns/`, `sessions/` lub sekcji `psychological-map.md`. Jeśli nie możesz nic podlinkować, eksperyment jest prawdopodobnie przedwczesny.>

## Procedura
<Dokładnie co będzie zrobione, kiedy i jak często. Wystarczająco konkretnie, żeby obca osoba mogła wykonać. Włącz wyzwalacz („gdy X się zdarza"), działanie („zrobię Y") i czas trwania („przez dwa tygodnie").>

## Kryteria sukcesu
<Jaki obserwowalny wynik liczyłby się jako potwierdzenie hipotezy? Konkretnie. Preferuj dowody behawioralne nad uczucia. Jeśli uczucia są miarą, zdefiniuj, jak będą oceniane.>

## Kryteria porażki
<Jaki obserwowalny wynik liczyłby się jako obalenie hipotezy — albo jako sygnał, że eksperyment jest zbyt kosztowny, by kontynuować? Zdefiniuj to PRZED startem.>

## Data przeglądu
<Data, w której eksperyment zostanie oceniony komendą `close-experiment`. Domyślnie: 2–4 tygodnie od startu, chyba że protokół sugeruje inaczej.>

## Notatki w trakcie
<Tylko-dopisuj log obserwacji robionych w trakcie eksperymentu. Datowane wpisy. Bez interpretacji — ta idzie do przeglądu zamykającego.>
```

## Rules

- **One hypothesis per experiment.** If there are two, run two — or pick.
- **Pre-register success and failure.** Both criteria must be written before the experiment starts. Post-hoc redefinition is how experiments turn into self-justification.
- **Time-box.** Open-ended experiments produce no learning.
- **Low cost preferred.** The smallest experiment that could move the question is the right experiment.
- **Cite the source.** The experiment file must link to the pattern, session, or map section that motivated it.
- **Log it.** Add an entry to `.ai/session-log.md` with `→ eksperyment:<nazwa>` (in Polish).
- **Prefer "zaangażuj się bardziej" experiments to "czuj mniej" experiments.** The goal is a larger life, not lower anxiety.
