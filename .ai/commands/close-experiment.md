# Command: close-experiment

> **Output language:** Polish. The close-out section appended to the experiment file must be in Polish.

## Purpose

Review a completed (or abandoned) experiment. Extract the learning. Feed it back into `patterns/` and, when warranted, propose updates to `psychological-map.md`.

## When to invoke

- The experiment's review date has arrived.
- The experiment's failure criteria were tripped.
- The user decided to stop, regardless of the original timeline.

Even an abandoned experiment gets a close-out. "Porzuciliśmy to i dlaczego" is a real finding.

## Procedure

1. Open the experiment file in `experiments/`. Read the original hypothesis, success criteria, failure criteria, and run notes.
2. Compare the run notes against the pre-registered success/failure criteria. Do not redefine them now.
3. Decide the result.
4. Append the close-out section (below) to the experiment file. Update the status field to `zamknięty` (or `porzucony`).
5. If the experiment produces a candidate update to `patterns/` or `psychological-map.md`, flag it in the close-out — do not write directly to those files here. Promotion goes through `update-map`.
6. Log it in `.ai/session-log.md` with `→ eksperyment:<nazwa> zamknięty`.

## Polish template (append to the experiment file)

```markdown
---

## Zamknięty: RRRR-MM-DD

## Wynik
<Potwierdzony / Niepotwierdzony / Nierozstrzygnięty / Porzucony. Jeden akapit mówiący, co się rzeczywiście stało wobec z góry zarejestrowanych kryteriów. Bez litygowania kryteriów. Bez „no, w pewnym sensie tak".>

## Co zadziałało
<Części protokołu, które wytworzyły realny sygnał lub były znośne. Konkretnie.>

## Co nie zadziałało
<Części protokołu, które się posypały, były pomijane lub nie wytworzyły sygnału. Konkretnie. Włącz unikanie: jeśli krok był wielokrotnie omijany, nazwij to.>

## Wnioski
<Co teraz wierzę mocniej, słabiej lub inaczej dzięki temu eksperymentowi. Rozróżnij wnioski o *użytkowniku* od wniosków o *projekcie eksperymentu*.>

## Aktualizacje mapy psychologicznej
<Konkretne propozycje do `patterns/` lub sekcji `psychological-map.md`. Dla każdej napisz: który plik/sekcja, jaki wpis dodać/zmienić, jakie dowody to wspierają. To są propozycje — faktyczne edycje robi `update-map`.>

- Propozycja: ...
- Propozycja: ...
```

## Rules

- **No moving the goalposts.** The success/failure criteria were defined upfront. They are the criteria.
- **An honest negative result is a finding.** "Hipoteza niepotwierdzona" is as valuable as confirmation. Do not soften it.
- **Abandonment counts.** Record why it was abandoned (nuda, dryf, okoliczności życiowe, lęk). The reason is often the most useful artifact of the experiment.
- **Do not promote to `psychological-map.md` from this command.** Stage proposals only.
- **Check against the success metric.** If the experiment "succeeded" by making life smaller (more avoidance, less engagement), that is not actually success.
