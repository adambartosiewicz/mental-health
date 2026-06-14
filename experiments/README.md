# Experiments

## Purpose

Behavioral experiments — small, time-boxed, pre-registered tests of specific hypotheses about how I work. Experiments are how interpretations become knowledge.

## Update rules

- Create experiment files via the `new-experiment` command — see `.ai/commands/new-experiment.md`.
- Close experiment files via the `close-experiment` command — see `.ai/commands/close-experiment.md`.
- Filename: `YYYY-MM-DD-<short-kebab-name>.md`. The date is when the experiment **starts**.
- **Pre-register success and failure criteria.** Both must be written before the experiment begins. Post-hoc redefinition is how this system turns into self-justification.
- **Time-box.** Every experiment has a review date.
- **One hypothesis per experiment.** If there are two, run two — or pick.
- Status field on every file: `active`, `complete`, `paused`, `abandoned`.
- An abandoned experiment still gets a close-out write-up. *Why it was abandoned* is real data.

## Template summary

The full template lives in `.ai/commands/new-experiment.md`. Required sections:

- Hypothesis
- Why It Matters
- Procedure
- Success Criteria
- Failure Criteria
- Review Date

Close-out sections (appended via `close-experiment`):

- Result
- What Worked
- What Didn't
- Lessons Learned
- Psychological Map Updates (proposals only — actual map edits happen via `update-map`)

## What this directory is NOT

- Not a goal list. Goals are aspirations; experiments are tests with falsifiable outcomes.
- Not a habit tracker. A habit attempt without a hypothesis and pre-registered criteria is not an experiment.
