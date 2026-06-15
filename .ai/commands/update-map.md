# Command: update-map

> **Output language:** Polish. All generated files, diff proposals, and report text must be in Polish. The command instructions below remain in English; the templates and any user-facing output are in Polish.

## Purpose

Update `psychological-map.md` (at the repository root) based on accumulated material in:

- recent `sessions/`
- `journal/` entries
- closed and ongoing `experiments/`
- existing `patterns/` files

The map is the **single source of truth** and the **slowest-moving file** in this repo. Most invocations should result in **small edits, no edits, or only an open question added** — not a rewrite.

## Rules

1. **Only add recurring patterns.** A pattern needs at least ~3 distinct observations on different days across `sessions/`, `journal/`, or `patterns/` before it earns a map entry. If you can't cite three, do not promote it.
2. **Avoid single-event conclusions.** A bad week, a single conflict, or one productive sprint is not a map update.
3. **Separate observations from interpretations.** Use the Polish entry template (below).
4. **Cite sources.** Every map entry or update must reference the session/journal/pattern/experiment files that justify it.
5. **Supersede, don't overwrite.** If a map entry is being changed because the old version is wrong, move the old version to `archive/psychological-map-<data>.md` and write the new entry with a back-reference.
6. **Demote, don't delete.** If a pattern is weakening, mark `pewność: obniżona, obserwuj` rather than removing it.
7. **References do not auto-merge.** Anything in `references/` is an input, not evidence.

## Procedure

1. Read `psychological-map.md` in full.
2. Read all `sessions/` files since the date noted at the top of the map (or the last 4 weeks if no date).
3. Read recent `journal/` entries.
4. Scan `patterns/` files for entries that have crossed the recurrence threshold but are not yet in the map.
5. Produce a **diff proposal in Polish** before writing: list (a) wpisy do dodania, (b) wpisy do aktualizacji, (c) wpisy do degradacji/archiwizacji. Present this to the user for confirmation before applying.
6. Apply approved changes. Update the "Ostatnia aktualizacja" date at the top of the map. Log the update in `.ai/session-log.md` with `→ mapa`.

## Polish entry template (use when proposing additions)

```markdown
### <Krótka nazwa>

- **Obserwacja:** <co jest wielokrotnie obserwowane, prostym językiem, ze źródłami>
- **Interpretacja:** <aktualna najlepsza hipoteza, oznaczona jako hipoteza>
- **Pewność:** niska / średnia / wysoka
- **Źródła:** `patterns/...`, `sessions/...`, `experiments/...`
- **Ostatni przegląd:** RRRR-MM-DD
```

## Output expectations

- Bias toward fewer, higher-confidence entries.
- It is a successful invocation to add nothing and surface a question instead.
- Never silently remove an entry.
- Keep the map within its target size (3–10 pages). If it grows beyond that, prune or archive.
