# Command: update-map

## Purpose

Update `psychological-map.md` (at the repository root) based on accumulated material in:

- recent `sessions/`
- `journal/` entries
- closed and ongoing `experiments/`
- existing `patterns/` files

The map is the **single source of truth** and the **slowest-moving file** in this repo. Most invocations of this command should result in **small edits, no edits, or only an open question added** — not a rewrite.

## Rules

1. **Only add recurring patterns.** A pattern needs at least ~3 distinct observations on different days across `sessions/`, `journal/`, or `patterns/` before it earns a map entry. If you can't cite three, do not promote it.
2. **Avoid single-event conclusions.** A bad week, a single conflict, or one productive sprint is not a map update.
3. **Separate observations from interpretations.** When writing to the map, structure entries as:
   - **Observation:** what was observed, citing source files.
   - **Interpretation:** the current best hypothesis, marked as a hypothesis.
   - **Confidence:** low / medium / high.
4. **Cite sources.** Every map entry or update must reference the session/journal/pattern/experiment files that justify it.
5. **Supersede, don't overwrite.** If a map entry is being changed because the old version is wrong, move the old version to `archive/psychological-map-<date>.md` and write the new entry with a back-reference.
6. **Demote, don't delete.** If a pattern is weakening, mark `confidence: lowered, watch` rather than removing it.
7. **References do not auto-merge.** Anything in `references/` is an input, not evidence. A concept from a reference reaches the map only via the same threshold as any other pattern, and the cited evidence must be the user's own.

## Procedure

1. Read `psychological-map.md` in full.
2. Read all `sessions/` files since the date noted at the top of the map (or the last 4 weeks if no date).
3. Read recent `journal/` entries.
4. Scan `patterns/` files for entries that have crossed the recurrence threshold but are not yet in the map.
5. Produce a **diff proposal** before writing: list (a) entries to add, (b) entries to update, (c) entries to demote/archive. Present this to the user for confirmation before applying.
6. Apply approved changes. Update the "Last updated" date at the top of the map. Log the update in `.ai/session-log.md` with `→ map`.

## Output expectations

- Bias toward fewer, higher-confidence entries.
- It is a successful invocation to add nothing and surface a question instead.
- Never silently remove an entry.
- Keep the map within its target size (3–10 pages). If it grows beyond that, prune or archive.
