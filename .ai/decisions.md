# System Decisions

Durable decisions about **how this repository works** — not about the user. When a workflow rule, naming convention, or structural choice gets settled, record it here so future sessions don't relitigate.

## Update rules

- Append new decisions to the bottom with a date.
- Never edit a decision in place. If a decision is reversed, add a new entry that supersedes it, and link back.
- Keep entries short: the rule, the reason, and (if reversed) what replaced it.

## Format

```
## YYYY-MM-DD — <short title>

**Decision:** <what we decided>
**Why:** <the reason — usually a problem this avoided>
**Status:** active | superseded by <date>
```

---

## 2026-06-14 — Sessions use date-topic filenames

**Decision:** Session files are named `YYYY-MM-DD-short-topic.md` (kebab-case topic). One session per file.
**Why:** Sortable chronologically, greppable by topic, no collisions.
**Status:** active

## 2026-06-14 — Map updates require ≥3 observations

**Decision:** Nothing is added to `psychological-map.md` from fewer than three distinct observations on different days.
**Why:** Single-event conclusions are how this kind of system becomes a hall of mirrors.
**Status:** active

## 2026-06-14 — Archive instead of delete

**Decision:** Outdated content from `psychological-map.md` is moved to `archive/psychological-map-YYYY-MM-DD.md`, not deleted. The replacement entry links to the archive.
**Why:** Trend detection needs history. We need to be able to ask "what did I used to believe about X?"
**Status:** active

## 2026-06-14 — Single source of truth at the root

**Decision:** `psychological-map.md` lives at the repository root and is the only authoritative document about the user. The `core/` directory was removed; its contents (values, strengths, open-questions) were merged into the map as sections.
**Why:** The repository was fragmenting the model across multiple "core" files, undermining the single-source-of-truth principle. The map should be readable on its own.
**Status:** active

## 2026-06-14 — `references/` never auto-merges

**Decision:** External material in `references/` (articles, ADHD resources, therapy concepts, frameworks) is an input, not part of the model. Reference material does not flow into `psychological-map.md` automatically — the same evidence threshold applies as for any user-specific pattern.
**Why:** A compelling framework is not evidence. Without this rule the map would fill with other people's models.
**Status:** active

## 2026-06-14 — Success is not "less anxiety"

**Decision:** The success metric of this repository is: larger life, reduced avoidance, increased psychological flexibility, increased engagement, improved self-understanding. Reduction of anxiety is **not** the success metric.
**Why:** Anxiety can drop because life got smaller. That is a failure presenting as success. Encoded so the AI does not optimize for the wrong objective.
**Status:** active
