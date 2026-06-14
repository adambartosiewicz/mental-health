# Journal

## Purpose

Raw, unstructured, dated thoughts. The place where things go *first*, before they have a shape.

This is the lowest-friction surface in the repo. It exists so that observations are captured at all — the polishing happens later, in `sessions/`, `patterns/`, or `core/`.

## Update rules

- **Append-only.** Never edit a past entry. If a later thought reverses an earlier one, write a new entry that says so.
- **Date every entry.** One file per day is fine: `YYYY-MM-DD.md`. Multiple entries within a file get their own timestamp heading.
- **No template required.** Bullet points, paragraphs, fragments are all fine.
- **No interpretation pressure.** This is the place to write "I felt off today and I don't know why" without owing a reason.
- **No promotion from here.** Journal entries get promoted to `patterns/` or `core/` only by `analyze-pattern` or `update-map` — not casually.

## Suggested filename

```
journal/YYYY-MM-DD.md
```

If multiple entries on the same day:

```markdown
## HH:MM

<entry>

## HH:MM

<another entry>
```

## What this directory is NOT

- Not a place for structured session summaries — those go in `sessions/`.
- Not a place for experiment logs — those go in the experiment file under `experiments/`.
- Not a to-do list.
