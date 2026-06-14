# Mental Health

A long-term personal psychological self-observation system. The goal is **pattern detection across months and years** to drive **behavioral change**, not therapy, not journaling for its own sake, and not symptom tracking.

Focus areas: ADHD, anxiety, self-esteem, relationships, life satisfaction, behavioral experiments.

This repository is optimized for collaboration with AI assistants over time.

---

## Single source of truth

There is exactly one authoritative document about me in this repository:

**`psychological-map.md`** (at the root).

Everything else exists to support, update, or evidence the map. The map should be readable on its own without browsing the rest of the repo. If information starts to live anywhere else and never reaches the map, the system has failed.

Target size of the map: **3–10 pages.** If it grows past that, prune or archive.

---

## Information flow

```
journal/  ──┐
            ├──►  patterns/  ──►  psychological-map.md
sessions/ ──┘                              ▲
                                           │
experiments/  ─── results ─────────────────┘

references/   (inputs from outside — never auto-merged into the map)
archive/      (retired material — moved here, not deleted)
```

The rules:

1. **Raw observation → `journal/`.** Single events, vents, fragments. No promotion pressure.
2. **Structured conversation → `sessions/`.** Summaries of substantive AI conversations. Temporary working documents.
3. **Recurrence → `patterns/`.** When the same observation appears on ≥3 distinct days, it earns a place in the relevant `patterns/<domain>.md` file. Patterns are **analytical artifacts**, not sources of truth. They support the map; they do not replace it.
4. **Strong evidence → `psychological-map.md`.** Only well-supported, durable findings reach the map. The map is updated via the `update-map` command after a deliberate review.
5. **Hypotheses → `experiments/`.** When something in the map needs testing — or before promoting an interpretation — design a behavioral experiment.
6. **External material → `references/`.** Articles, ADHD resources, therapy concepts, frameworks. **Never auto-merged into the map.**
7. **Retired material → `archive/`.** When something in the map becomes outdated, the old version is moved here with a date; the new entry links back. Nothing is deleted.

---

## The map's lifecycle

`psychological-map.md` evolves slowly and deliberately.

- **Add** an entry only when there are at least 3 distinct supporting observations across different days.
- **Update** an entry only via the `update-map` command, which produces a diff proposal first.
- **Supersede** rather than overwrite: move the old version to `archive/psychological-map-<date>.md`, write the replacement, link back.
- **Demote** rather than delete: when a pattern weakens, mark `confidence: lowered, watch`. Removal happens only after extended absence.
- **Cite evidence** for every non-trivial entry: link to `patterns/`, `sessions/`, or `experiments/`.
- **Separate observation from interpretation.** Every entry has both, clearly distinguished, plus confidence.

---

## The role of experiments

The system prefers **experiments over speculation**.

When the map contains an interpretation that has become load-bearing, or an open question that everyday life could test, design an experiment under `experiments/`. Experiments are time-boxed, pre-register success and failure criteria, and produce a written close-out — including the negative and abandoned ones.

> "What can I test?" beats "Why am I like this?"

---

## The role of AI agents

AI assistants are **co-maintainers** of this repository, not interlocutors who soothe.

### Rules for AI when processing new information

1. **Capture observations in `journal/`** when they are raw and dated.
2. **Detect recurring themes in `patterns/`** — promote only after recurrence.
3. **Update `psychological-map.md` only when evidence is strong.** Never on the strength of one conversation.
4. **Distinguish observations from interpretations** in every output. Mark hypotheses as hypotheses.
5. **Avoid reassurance-seeking workflows.** No "you're doing great." No reassurance loops about specific anxiety content.
6. **Prefer experiments over speculation.** When an interpretation gets sticky, propose an experiment instead of agreeing with it.

### What AI should refuse

- Diagnosing.
- Generating reassurance without specific grounding.
- Producing lists of "things you could try" when the user is venting (ask first whether they want options or witness).
- Treating a single bad day as a trend.
- Letting `references/` material flow into the map without explicit human approval.

Full AI context lives in `.ai/context.md`. Reusable workflows live in `.ai/commands/`.

---

## Directory map

```
mental-health/
├── README.md                      this file
├── psychological-map.md           the single source of truth
├── .ai/                           AI collaboration layer
│   ├── context.md                   how an AI should approach this repo
│   ├── decisions.md                 durable decisions about the system itself
│   ├── session-log.md               chronological index of sessions
│   └── commands/                    reusable AI workflows
├── journal/                       raw, dated, append-only observations
├── sessions/                      structured conversation summaries
├── patterns/                      analytical artifacts (anxiety, adhd, …)
├── experiments/                   behavioral experiments (active and closed)
├── references/                    external material — never auto-merged
└── archive/                       retired map entries and patterns
```

---

## Success metric

This repository exists to support:

- **a larger life**
- **reduced avoidance**
- **increased psychological flexibility**
- **increased engagement with what matters**
- **improved self-understanding**

The repository **does NOT exist solely to reduce anxiety.** Anxiety going down is not the goal. Anxiety can go down because life got smaller — that is a failure. Anxiety can go up while life gets larger — that can be success.

If the map is becoming more honest, experiments are running, avoidance is being named, and engagement is increasing, the system is working.
