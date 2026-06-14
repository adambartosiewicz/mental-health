# Psychological Map

> **Last updated:** YYYY-MM-DD
> **Status:** working document. Updated only via the `update-map` command.

## Purpose

The current best model of how I work. This file is the **slowest-moving artifact** in the repository. Everything here has earned its place by recurring across multiple sessions, experiments, or extended observation. New observations live in `sessions/` and `journal/`. Recurring observations live in `patterns/`. Only well-supported, durable patterns belong here.

## Update rules

- Only updated via `.ai/commands/update-map.md`.
- Every entry must cite at least one supporting file under `Sources`.
- Entries are structured: **Observation → Interpretation → Confidence**.
- When superseded, the old version is moved to `archive/psychological-map-<date>.md`, not deleted.
- The "Last updated" date at the top is bumped on every change.

## Entry template

```markdown
### <Short name of pattern>

- **Observation:** <what is repeatedly observed, in plain language>
- **Interpretation:** <current best hypothesis about why — marked as hypothesis>
- **Confidence:** low / medium / high
- **Sources:** `sessions/...`, `patterns/...`, `experiments/...`
- **Open questions:** <what would change my confidence either way>
- **Last reviewed:** YYYY-MM-DD
```

## Example entry (illustrative — replace with real ones over time)

```markdown
### Anticipation anxiety around social evaluation

- **Observation:** Anxiety spikes the evening before any scheduled 1:1 with a manager, performance review, or social event with new people. Body symptoms (jaw, shallow breath) precede conscious thought.
- **Interpretation:** Hypothesis — this is anticipation of being evaluated, not of the event itself. Supported by: anxiety drops once the event begins.
- **Confidence:** medium
- **Sources:** `sessions/2026-05-18-pre-1on1-spike.md`, `sessions/2026-05-30-review-eve.md`, `patterns/anxiety.md#anticipation`
- **Open questions:** Does it occur for events with peers or only with perceived authority? Tested partially in `experiments/2026-06-01-peer-1on1.md`.
- **Last reviewed:** 2026-06-09
```

## Sections

Organize entries under the following headers. Leave them present even when empty so the structure stays visible.

### ADHD

<!-- entries here -->

### Anxiety

<!-- entries here -->

### Self-esteem

<!-- entries here -->

### Relationships

<!-- entries here -->

### Life satisfaction

<!-- entries here -->

### Cross-cutting

<!-- patterns that span multiple domains -->
