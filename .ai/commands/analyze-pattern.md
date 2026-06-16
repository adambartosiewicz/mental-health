# Command: analyze-pattern

> **Output language:** Polish. All pattern descriptions, evidence summaries, confidence justifications, and promotion recommendations in the report must be in Polish.

## Purpose

Sweep the whole repository — `sessions/`, `journal/`, `experiments/`, `patterns/`, `psychological-map.md`, and contextually `references/` — and identify recurring psychological patterns. Output a structured analysis the user can review.

This is the **detection** step. It does not write to `psychological-map.md` or to the domain pattern files. Promotion happens later, deliberately, through `update-map` or by editing the relevant `patterns/<domain>.md`.

## Procedure

1. Read all of `sessions/` and `journal/` (the latter is partitioned as `journal/YYYY/MM/YYYY-MM-DD.md` — descend recursively, not just the top level). Take note of recurring words, situations, body responses, triggers, time-of-day effects.
2. Cluster recurrences into candidate patterns. A candidate needs **at least 3 instances on distinct days**.
3. For each candidate, gather:
   - direct evidence (sessions/journal that show the pattern)
   - **counter-evidence** (sessions/journal where the pattern would be expected but did not appear)
4. Cross-reference against existing entries in `patterns/` and `psychological-map.md`. Mark each candidate as `nowy`, `potwierdza istniejący`, `rozszerza istniejący` lub `przeczy istniejącemu`.
5. If a `references/` entry happens to describe a similar shape, **note the framing but do not let it substitute for evidence**. The user's own data is the only thing that counts toward promotion.
6. Produce the report below in Polish.

## Polish output format

For every detected pattern, output:

```markdown
### Wzorzec: <krótka nazwa>

- **Opis:** <jedno-akapitowy opis prostym językiem>
- **Dowody:**
  - `sessions/2026-05-18-...md` — <jednolinijkowa notatka>
  - `journal/YYYY/MM/YYYY-MM-DD.md` — <jednolinijkowa notatka>
  - ...
- **Kontrdowody:**
  - <sytuacje lub sesje, w których wzorzec byłby oczekiwany, ale się nie pojawił>
  - <jeśli nie ma — powiedz to wprost; to też jest ustalenie>
- **Pewność:** niska / średnia / wysoka
  - Uzasadnij jednym zdaniem. Pewność powinna odzwierciedlać szerokość dowodów, nie siłę odczucia.
- **Możliwe eksperymenty:**
  - <jeden lub dwa testy behawioralne, które mogłyby pchnąć pytanie>
- **Relacja do istniejącej mapy:** nowy / potwierdza / rozszerza / przeczy <wpis>
- **Istotne materiały (tylko framing):** <jeśli jakiś materiał z `references/` pasuje — nie traktuj jako dowodu>
```

Zakończ raport krótką sekcją **Rekomendacja promocji**, która sugeruje dla każdego wzorca: dalej obserwować, dodać do `patterns/`, dodać do `psychological-map.md` lub zaprojektować eksperyment.

## Rules

- **Counter-evidence is mandatory.** A pattern reported without an honest search for counter-examples is not a finding.
- **Confidence is calibrated.** "Czuję, że tak jest" is not high confidence. High confidence requires breadth across time and contexts.
- **Name avoidance patterns explicitly.** If something is being systematically *not* discussed, that is itself a pattern worth flagging.
- **Do not write to `psychological-map.md` or `patterns/` from this command.** Output only.
- **Frameworks ≠ evidence.** A reference that fits beautifully is not a reason to promote anything.
