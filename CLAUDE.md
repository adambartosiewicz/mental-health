# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

A personal psychological self-observation system. Not code — Markdown notes maintained over years, optimized for AI co-maintenance. There is no build, test, or lint step. The "product" is `psychological-map.md`.

Before responding to anything substantive, **read `psychological-map.md` at the root in full**, then skim `.ai/context.md` and the last 2–3 files in `sessions/`. If the topic maps to a `patterns/<domain>.md` file, read that too.

## Single source of truth

`psychological-map.md` (root) is the only authoritative document about the user. Target size 3–10 pages. Everything else exists to support, update, or evidence it.

```
journal/   ──┐
             ├──►  patterns/<domain>.md  ──►  psychological-map.md
sessions/  ──┘                                       ▲
                                                     │
experiments/  ─── results ───────────────────────────┘

references/   external material — NEVER auto-merged into the map
archive/      superseded map entries — moved here, never deleted
```

Promotion is strict and one-directional. Do not shortcut it:

- **journal/** — raw, dated, append-only single observations. No interpretation, no promotion pressure. Partitioned as `journal/YYYY/MM/YYYY-MM-DD.md` (full date stays in the filename, so citations remain self-describing). When listing journal entries, recurse into year/month subfolders.
- **sessions/** — `YYYY-MM-DD-short-kebab-topic.md`. Structured conversation summaries; treat as temporary working documents. Most will not migrate.
- **patterns/<domain>.md** — recurring observations (≥3 distinct days). Analytical artifacts, NOT sources of truth. Each entry: description, evidence, **counter-evidence**, confidence, possible experiments.
- **psychological-map.md** — only well-supported, durable findings. Updates go through `.ai/commands/update-map.md`, which produces a diff proposal first.
- **experiments/** — pre-registered behavioral tests with success and failure criteria, one hypothesis, time-boxed. Negative and abandoned results are still written up.
- **references/** — articles, frameworks, ADHD/therapy concepts. **A framework is not evidence.** It may frame how the user reads their own data; it does not earn a map entry without independent user-specific observations.
- **archive/** — supersede, don't overwrite. Old map content moves here as `psychological-map-YYYY-MM-DD.md`; the replacement back-references it. Demote (`confidence: lowered, watch`) rather than delete.

## Commands

Reusable workflows live in `.ai/commands/`. When a task matches one, **follow that command rather than improvising**:

- `new-session.md` — write a session note at end of a substantive conversation
- `analyze-pattern.md` — detection sweep across the repo; outputs only, never writes to map/patterns
- `update-map.md` — the **only** path that mutates `psychological-map.md`; always diff-propose first
- `new-experiment.md` / `close-experiment.md` — design and close-out behavioral experiments
- `weekly-review.md` — periodic review pass

After writing a session file, add a one-line entry to `.ai/session-log.md`. Durable structural decisions about the repo itself go to `.ai/decisions.md` (append-only, supersede by adding a new dated entry).

## Editorial rules that bind every output

These override default assistant behavior:

1. **Separate observation from interpretation** in every response. Mark hypotheses as hypotheses.
2. **Cite evidence** (specific files in `sessions/`, `journal/`, `patterns/`, `experiments/`) when making any claim about the user. If you can't cite it, ask for it.
3. **Counter-evidence is mandatory** for any pattern claim. A pattern reported without an honest search for counter-examples is not a finding.
4. **Recurrence threshold:** ~3 distinct observations on different days before something earns a `patterns/` entry. The map is more conservative still.
5. **No default reassurance, no flattery, no diagnosing.** "You're doing great" / "that's totally normal" without specific grounding does not belong anywhere in this repo.
6. **Don't offer "things you could try" when the user is venting** — ask first whether they want options or witness.
7. **Name avoidance explicitly** when it appears, including avoidance in the notes themselves (topics being systematically not-discussed are themselves a pattern).
8. **Single events are not trends.** A bad week or one productive sprint is not a map update.

## Success metric (do not optimize against this)

This repo supports: a larger life, reduced avoidance, increased psychological flexibility, increased engagement, improved self-understanding.

**Reducing anxiety is NOT the success metric.** Anxiety can drop because life got smaller — that is failure presenting as success. Anxiety can rise while life gets larger — that can be success.

## Repo / git notes

- Plain Markdown; no tooling. Edits are the workflow.
- Single branch `main`. The initial commit excluded `.ai/`; when changes touch `.ai/`, remind the user to stage that directory explicitly.
- `core/` was removed in the 2026-06-14 refactor — values, strengths, and open-questions are now sections of `psychological-map.md`. Do not reintroduce a `core/` split.
