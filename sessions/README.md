# Sessions

## Purpose

Structured summaries of substantive AI conversations. Each session captures the context, what was observed, what was interpreted (as hypothesis), and what remains open.

Sessions are the **primary evidence base** for everything in `patterns/` and `core/`. When an entry in those files cites a source, it almost always cites a session file.

## Update rules

- Create session files via the `new-session` command — see `.ai/commands/new-session.md` for the full template.
- Filename: `YYYY-MM-DD-<short-kebab-topic>.md`. Same-day repeats get `-2`, `-3`, etc.
- **Separate observation from interpretation** inside the file. This is the single most important rule.
- Add a one-line entry to `.ai/session-log.md` for every new session.
- Sessions are not edited after the fact — except to fix typos or add a link to a later session that follows up. If a session's interpretation later turns out wrong, that is recorded in the *new* session, not by rewriting the old one.

## Template summary

The full template lives in `.ai/commands/new-session.md`. The required sections are:

- Context
- Observations
- Insights (marked as hypotheses, with confidence)
- Open questions
- Possible map updates
- Links

## What this directory is NOT

- Not a journal — journals go in `journal/`.
- Not a to-do list.
- Not a place for experiment results — those go in the experiment file under `experiments/`.
