# Mental Health

A long-term personal psychological self-observation system. The goal is not therapy, not journaling for its own sake, and not symptom tracking. The goal is **pattern detection over months and years** to drive **behavioral change**.

Focus areas:

- ADHD
- Anxiety
- Self-esteem
- Relationships
- Life satisfaction
- Behavioral experiments

This repository is optimized for collaboration with AI assistants. The structure exists so that an AI (or future-me) can re-enter the context cold and quickly understand the current psychological map, open questions, and active experiments.

---

## Workflow

1. **Have a conversation** with an AI assistant about something happening in life (a mood, a conflict, a stuck pattern, a decision).
2. **Capture it.** At the end of the conversation, run the `new-session` command to produce a structured note in `sessions/`.
3. **Free-write** in `journal/` whenever useful — raw, unstructured, undated thoughts welcome.
4. **Periodically run** `analyze-pattern` and `update-map` to fold recent material into the long-lived `core/` files.
5. **Run `weekly-review`** roughly once a week.
6. **Design behavioral experiments** when a pattern is identified and a hypothesis is testable. Track them in `experiments/`.
7. **Archive** anything stale, contradicted, or no longer load-bearing into `archive/` — don't delete history.

---

## Directory map

```
mental-health/
├── README.md                this file
├── .ai/                     AI collaboration layer
│   ├── context.md             how an AI should approach this repo
│   ├── decisions.md           durable decisions about the system itself
│   ├── session-log.md         chronological index of sessions
│   └── commands/              reusable AI workflows
├── core/                    the slow-moving truth
│   ├── psychological-map.md   current best model of self
│   ├── values.md              what actually matters
│   ├── strengths.md           what works, what to lean on
│   └── open-questions.md      live unknowns being investigated
├── journal/                 raw thoughts, unstructured, append-only
├── sessions/                structured conversation summaries (YYYY-MM-DD-topic.md)
├── experiments/             behavioral experiments (active and completed)
├── patterns/                detailed pattern files by domain
│   ├── anxiety.md
│   ├── adhd.md
│   ├── relationships.md
│   ├── work.md
│   └── self-esteem.md
└── archive/                 retired material kept for history
```

---

## How AI should interact with these files

**Read before writing.** Before adding anything to `core/` or `patterns/`, read the existing content. The point is convergence over time, not accretion.

**Separate observation from interpretation.** A session might note "felt anxious before the 1:1" (observation) and "may indicate fear of evaluation" (interpretation). Tag them differently. Interpretations are hypotheses, not facts.

**Promote slowly.** A single event belongs in `journal/` or `sessions/`. Only promote to `patterns/` when there is recurrence. Only promote to `core/psychological-map.md` when a pattern is well-supported.

**Prefer evidence over consensus.** When updating `psychological-map.md` or `patterns/`, cite specific session files or experiments as evidence. Avoid "this seems true because we've said it before."

**Never overwrite — append and supersede.** When something in `core/` becomes outdated, move the old version to `archive/` with a date, and write the new version with a reference back. History matters for trend detection.

**Use the commands.** The AI commands in `.ai/commands/` encode the workflows. If a task matches one, follow that command rather than improvising.

### What this system prioritizes

- **Pattern detection** across weeks and months
- **Long-term trends**, not daily noise
- **Behavioral change** through designed experiments
- **Reducing avoidance** — naming what is being dodged

### What this system avoids

- **Excessive reassurance.** The AI should not soothe by default. If something is hard, name it.
- **Compulsive symptom analysis.** Listing every anxious thought is not progress. Patterns matter; instances mostly don't.
- **Treating interpretations as facts.** "I think I do X because Y" is a hypothesis. Mark it as one.

---

## Where information goes

| If it is...                                              | Put it in...                          |
| -------------------------------------------------------- | ------------------------------------- |
| A raw thought, vent, or stream-of-consciousness          | `journal/`                            |
| A summary of a real AI conversation                      | `sessions/YYYY-MM-DD-topic.md`        |
| A recurring observation across multiple sessions         | `patterns/<domain>.md`                |
| A well-supported model of how I work                     | `core/psychological-map.md`           |
| A planned behavioral test                                | `experiments/YYYY-MM-DD-name.md`      |
| A retired belief or outdated map entry                   | `archive/`                            |
| A decision about the *system itself* (not about me)      | `.ai/decisions.md`                    |
