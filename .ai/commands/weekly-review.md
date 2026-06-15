# Command: weekly-review

> **Output language:** Polish. The session file produced by this command, and all dimension reads, wins, concerns, patterns, and suggested actions, must be in Polish.

## Purpose

Review the last 7 days. Pull signal out of noise. Set direction for the next week.

## Inputs

- `sessions/` from the last 7 days
- `journal/` entries from the last 7 days
- Any `experiments/` updated, completed, or due in this window
- Last week's review entry (if it exists), for continuity
- `psychological-map.md` for context on currently active hypotheses and open questions

## Analyze across dimensions

For each dimension, give a one-line read (`trend`, `notatki`). Cite at least one source file per dimension when relevant. If there is no data, say so — do not fabricate.

- **Nastrój** — overall affective baseline, any spikes/dips.
- **Lęk** — frequency, triggers, intensity. Note avoidance behaviors.
- **Objawy ADHD** — focus, follow-through, time loss, hyperfocus, transitions.
- **Energia** — physical energy, sleep, motivation distinguished from mood.
- **Aktywność społeczna** — interactions had, declined, dreaded, enjoyed.
- **Eksperymenty** — what ran, what is due, what was learned.

## Output structure

Write the review as a session file: `sessions/RRRR-MM-DD-weekly-review.md`, tagged `[meta]` in `.ai/session-log.md`. Everything in Polish.

Sections (Polish):

```markdown
# Przegląd tygodnia — RRRR-MM-DD

## Okno
<zakres dat>

## Wymiary
- **Nastrój:** ...
- **Lęk:** ...
- **ADHD:** ...
- **Energia:** ...
- **Społeczne:** ...
- **Eksperymenty:** ...

## Sukcesy
<rzeczy, które rzeczywiście zadziałały — konkretne, nie ogólne. Cytuj dowody.>

## Obawy
<rzeczy idące źle — nazwij wprost. Bez uspokajania.>

## Wzorce
<cokolwiek, co pojawia się w wielu wymiarach lub powtarza się z poprzedniego tygodnia.>

## Sugerowane następne działania
<1–3 konkretne działania. Każde nazywa, co zrobić, kiedy i co liczyłoby się jako wykonane. Preferuj działania, które zmniejszają unikanie, nad działania, które dokładają do listy zadań.>

## Kandydaci do mapy / wzorców
<cokolwiek, co warto rozważyć do promocji do `patterns/` lub `psychological-map.md`. Nie promuj tutaj; tylko flaguj.>
```

## Rules

- Be terse. A weekly review that takes 20 minutes to read will not be reread.
- No generic advice ("spróbuj medytować", "śpij więcej"). Actions must connect to specific observed material.
- If avoidance shows up, name it explicitly. Do not euphemize.
- It is fine — sometimes correct — to write "w tym tygodniu nic wartego uwagi."
- Remember the success metric: anxiety going down is not in itself a win. A larger week with more avoidance reduced is a win.
