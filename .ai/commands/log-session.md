# Command: log-session

> **Output language:** Polish. The session file created by this command must be in Polish, including all section headers (matching the template below), observations, insights, and notes.

## Purpose

At the end of a substantive conversation, capture it as a structured note in `sessions/` so that future-me and future-AI can reconstruct what happened and what was learned. Session files are **temporary working documents** — the important discoveries are expected to migrate into `psychological-map.md` over time.

## When to invoke

- The conversation surfaced something concrete: an observation, an insight, a felt shift, a stuck point.
- The user explicitly asks for a session summary.
- A pattern was named that might recur.

Do **not** invoke for short tactical exchanges or pure logistics.

## File to create

```
sessions/RRRR-MM-DD-<krótki-kebab-temat>.md
```

Use today's date. The topic should be 2–5 Polish words, lowercase, kebab-case, easy to grep later. Examples: `skok-przed-1na1`, `plaska-sobota`, `petla-feedback-partnerka`.

If two sessions happen the same day on the same topic, append `-2`, `-3`, etc.

## Polish template

```markdown
# RRRR-MM-DD — <Tytuł tematu>

## Kontekst
<Co się działo. Wyzwalacz lub pytanie startowe. 2–5 zdań. Konkretne szczegóły (kto, kiedy, gdzie), gdy istotne.>

## Obserwacje
<Co zostało zauważone — uczucia, zachowania, sygnały z ciała, sytuacje. Prostym językiem. Bez interpretacji.>
- ...
- ...

## Wglądy
<Co rozmowa rozjaśniła. To są interpretacje i mają być tak oznaczone. Używaj sformułowań „aktualna hipoteza", „wstępne odczytanie". Pewność w nawiasie.>
- <wgląd> (pewność: niska/średnia/wysoka)
- ...

## Otwarte pytania
<Rzeczy, które ta sesja podniosła, ale nie rozwiązała. Kandydaci do sekcji Otwarte pytania w `psychological-map.md`, jeśli się powtórzą.>
- ...

## Możliwe aktualizacje mapy
<Cokolwiek z tej sesji, co — jeśli się powtórzy — warto rozważyć do `patterns/` lub `psychological-map.md`. Nie promuj tutaj — tylko flaguj.>
- ...

## Linki
- Powiązane sesje: <plik>, <plik>
- Powiązane wzorce: <plik>
- Powiązane eksperymenty: <plik>
- Powiązane sekcje mapy: <sekcja>
```

## Rules

- **Separate observations from insights.** The single most important rule of this template. An observation is something that happened. An insight is a story about what it means.
- **No reassurance language.** "I jest w porządku" / "to normalne" / "robisz, co możesz" do not belong in a session note. Just record.
- **Cite, don't repeat.** If a session is the third instance of a pattern, link to the prior two rather than restating.
- **Update the session log.** After writing the session file, add a one-line entry to `.ai/session-log.md` (in Polish).
- **Flag, don't promote.** Even if the session screams "this is a core truth about me," only flag it under *Możliwe aktualizacje mapy*. Promotion happens via `update-map`, not here.
- **Sessions are temporary.** Treat them as evidence that may or may not migrate into the map. Most won't.
