# Patterns: Anxiety

## Purpose

Detailed catalog of recurring anxiety patterns. Patterns are **analytical artifacts** — they support `psychological-map.md` but are not themselves the source of truth. They sit between raw observation (in `sessions/`, `journal/`) and the high-level model (in the map). A pattern earns a place here once it has recurred. It earns a place in the map only when it is well-supported and stable.

## Update rules

- A pattern is added only after **at least 3 distinct observations on different days**.
- Every pattern entry has the five required fields: **description, evidence, counter-evidence, confidence, experiments.** Additional fields below are optional but useful.
- **Counter-evidence is required.** A pattern without a search for counter-examples is suspect.
- Avoidance is itself a pattern. If something is being systematically dodged in sessions, name it here.
- This file is **not** an inventory of every anxious moment. Single events belong in `sessions/` or `journal/`. Patterns are the recurring shape.
- When a pattern weakens, mark `confidence: lowered` rather than deleting. When it disappears, move the entry to `archive/`.
- Patterns may *propose* updates to `psychological-map.md` but never replace it. Promotion goes through `update-map`.

## Entry template

```markdown
### <Pattern name>

- **Description:** <plain-language description: trigger, body signal, behavior, time course>
- **Evidence:** `sessions/...`, `journal/...`
- **Counter-evidence:** <situations where the pattern would have been expected but did not occur>
- **Confidence:** low / medium / high
- **Experiments:** `experiments/...` (or "proposed: <one-line idea>" if not yet designed)
- **Map status:** not promoted / proposed for map / present in map (`section`)
- **Last reviewed:** YYYY-MM-DD
```

## Example

```markdown
### Anticipation spike before social evaluation

- **Description:** Anxiety spikes 12–24h before scheduled 1:1s with managers, performance reviews, or social events with new people. Jaw tension first, then shallow breathing. Behaviorally: avoidance of agenda prep, late-night doomscrolling. Peaks the night before; drops sharply once the event begins.
- **Evidence:** `sessions/2026-05-18-pre-1on1-spike.md`, `sessions/2026-05-30-review-eve.md`
- **Counter-evidence:** Peer 1:1s with M and J did not produce the spike — suggests the "evaluation" axis matters more than "social interaction."
- **Confidence:** medium
- **Experiments:** `experiments/2026-06-01-agenda-night-before.md`
- **Map status:** proposed for map (Anxiety Model → Triggers)
- **Last reviewed:** 2026-06-09
```

## Sections

### Active patterns

<!-- entries here -->

### Watch list (sub-threshold)

<!-- candidate patterns with 1–2 observations, not yet promoted -->

### Weakened / under review

<!-- patterns that previously held but are losing support -->
