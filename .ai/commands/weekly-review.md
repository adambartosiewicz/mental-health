# Command: weekly-review

## Purpose

Review the last 7 days. Pull signal out of noise. Set direction for the next week.

## Inputs

- `sessions/` from the last 7 days
- `journal/` entries from the last 7 days
- Any `experiments/` updated, completed, or due in this window
- Last week's review entry (if it exists), for continuity
- `psychological-map.md` for context on currently active hypotheses and open questions

## Analyze across dimensions

For each dimension, give a one-line read (`trend`, `notes`). Cite at least one source file per dimension when relevant. If there is no data, say so — do not fabricate.

- **Mood** — overall affective baseline, any spikes/dips.
- **Anxiety** — frequency, triggers, intensity. Note avoidance behaviors.
- **ADHD symptoms** — focus, follow-through, time loss, hyperfocus, transitions.
- **Energy** — physical energy, sleep, motivation distinguished from mood.
- **Social activity** — interactions had, declined, dreaded, enjoyed.
- **Experiments** — what ran, what is due, what was learned.

## Output structure

Write the review as a session file: `sessions/YYYY-MM-DD-weekly-review.md`, tagged `[meta]` in `.ai/session-log.md`.

Sections:

```markdown
# Weekly Review — YYYY-MM-DD

## Window
<date range covered>

## Dimensions
- **Mood:** ...
- **Anxiety:** ...
- **ADHD:** ...
- **Energy:** ...
- **Social:** ...
- **Experiments:** ...

## Wins
<things that actually worked — concrete, not generic. Cite evidence.>

## Concerns
<things trending wrong — name them plainly. No reassurance.>

## Patterns
<anything that shows up across multiple dimensions or repeats from last week's review.>

## Suggested next actions
<1–3 concrete actions. Each one names what to do, when, and what would count as having done it. Prefer actions that reduce avoidance over actions that add to a to-do list.>

## Map / pattern candidates
<anything that should be considered for promotion to `patterns/` or `psychological-map.md`. Do not promote here; just flag.>
```

## Rules

- Be terse. A weekly review that takes 20 minutes to read will not be reread.
- No generic advice ("try meditating", "get more sleep"). Actions must connect to specific observed material.
- If avoidance shows up, name it explicitly. Do not euphemize.
- It is fine — sometimes correct — to write "nothing notable this week."
- Remember the success metric: anxiety going down is not in itself a win. A larger week with more avoidance reduced is a win.
