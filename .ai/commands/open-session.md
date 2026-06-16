# Command: open-session

> **Output language:** Polish. This command prepares context for a substantive conversation. It does not create or update a session file by itself.

## Purpose

Open a working psychological session by loading the minimum context needed to conduct it responsibly:

- current authoritative model from `psychological-map.md`,
- repo operating rules from `.ai/context.md`,
- continuity from recent sessions,
- relevant domain patterns when the topic is known.

This is the **intake / context-loading** step. It prepares the conversation. If the conversation later produces material worth preserving, close it with `new-session`.

## When to invoke

- At the beginning of a substantive psychological conversation.
- When the user says they want to "open a session", "start a session", "prowadzić sesję", or similar.
- When the assistant needs context before responding to a topic that may touch anxiety, ADHD, work, relationships, self-esteem, avoidance, flatness, experiments, or map updates.

Do **not** invoke for short logistics, pure repository maintenance, or coding tasks unrelated to this repo's psychological content.

## Procedure

1. Read `psychological-map.md` in full.
2. Skim `.ai/context.md`.
3. Read `.ai/session-log.md` for the latest continuity.
4. Read the last 2-3 dated files in `sessions/`. Ignore `sessions/README.md` unless the workflow itself is unclear.
5. If the user gives a topic, map it to relevant pattern files and read them:
   - anxiety, fear, bugs, bedbugs, parasites, health anxiety, uncertainty, checking, safety -> `patterns/anxiety.md`
   - work start, procrastination, focus, transitions, motivation, ADHD -> `patterns/adhd.md` and/or `patterns/work.md`
   - competence, shame, wasted potential, self-judgment -> `patterns/self-esteem.md`
   - partner, friends, mask, closeness, social contact -> `patterns/relationships.md`
6. If the topic may involve an active experiment, inspect `experiments/`.
7. Start the session with a short context statement:
   - what context was loaded,
   - what active hypotheses or open questions are relevant,
   - one focused opening question.

## Opening response format

Keep the response short. Use this structure in Polish:

```markdown
Mam otwarty kontekst sesji.

**Załadowane:** `psychological-map.md`, `.ai/context.md`, `.ai/session-log.md`, <ostatnie sesje>, <wzorce jeśli dotyczy>.

**Aktywne tło:** <1-3 zdania o istotnych hipotezach / otwartych pytaniach, jako hipotezy, z cytatami do plików>.

Od czego zaczynamy: <jedno konkretne pytanie>
```

## Rules

- **Do not create a session file at opening.** Session files are created at the end by `new-session`, when there is something substantive to preserve.
- **Separate observation from interpretation** in the opening context.
- **Cite sources** when naming an active hypothesis about the user.
- **No reassurance language.** Do not open with soothing, praise, or "to normalne".
- **Name avoidance if it is visible**, but do not force the frame before there is material.
- **Ask before giving options** if the user appears to be venting.
- **Do not update `psychological-map.md` or `patterns/` from this command.**
- **If the topic is unclear**, ask one short clarifying question after loading the base context.
