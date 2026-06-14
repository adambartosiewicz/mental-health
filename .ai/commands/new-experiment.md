# Command: new-experiment

## Purpose

Design a behavioral experiment to test a specific hypothesis about the user's psychology. Experiments turn vague self-narratives into falsifiable, time-boxed tests.

The system prefers experiments over speculation. When an interpretation in `psychological-map.md` or a pattern in `patterns/` is getting load-bearing, design an experiment rather than refining the interpretation further.

## When to invoke

- A pattern has been identified and there is a testable hypothesis about it.
- The user wants to *change* a behavior, not just understand it.
- An interpretation in the map has become load-bearing and needs to be checked against reality.

Do not run an experiment for things that are not testable in everyday life (e.g. "am I a good person").

## File to create

```
experiments/YYYY-MM-DD-<short-kebab-name>.md
```

Status starts at `active`. Update status when reviewed: `complete`, `paused`, `abandoned`.

## Template

```markdown
# Experiment: <Name>

**Status:** active
**Started:** YYYY-MM-DD
**Review date:** YYYY-MM-DD

## Hypothesis
<A single, concrete, falsifiable statement. "If I do X in situation Y, then Z will happen." Not "I want to feel better." Not "I want to be more social.">

## Why It Matters
<What pattern, open question, or map entry this connects to. Link to specific files in `patterns/`, `sessions/`, or sections of `psychological-map.md`. If you cannot link anything, the experiment is probably premature.>

## Procedure
<Exactly what will be done, when, and how often. Concrete enough that a stranger could execute it. Include the trigger ("when X happens"), the action ("I will do Y"), and the duration ("for two weeks").>

## Success Criteria
<What observable result would count as the hypothesis being supported? Be specific. Prefer behavioral evidence over feelings. If feelings are the measure, define how they'll be rated.>

## Failure Criteria
<What observable result would count as the hypothesis being disconfirmed — or as the experiment itself being too costly to continue? Define this BEFORE starting.>

## Review Date
<Date on which the experiment will be evaluated using `close-experiment`. Default: 2–4 weeks from start unless the protocol implies otherwise.>

## Notes during run
<Append-only log of observations made while the experiment is running. Dated entries. No interpretation here — that goes into the close-out review.>
```

## Rules

- **One hypothesis per experiment.** If there are two, run two — or pick.
- **Pre-register success and failure.** Both criteria must be written before the experiment starts. Post-hoc redefinition is how experiments turn into self-justification.
- **Time-box.** Open-ended experiments produce no learning.
- **Low cost preferred.** The smallest experiment that could move the question is the right experiment.
- **Cite the source.** The experiment file must link to the pattern, session, or map section that motivated it.
- **Log it.** Add an entry to `.ai/session-log.md` with `→ experiment:<name>`.
- **Prefer "engage more" experiments to "feel less" experiments.** The goal is a larger life, not lower anxiety.
