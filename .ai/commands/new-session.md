# Command: new-session

## Purpose

At the end of a substantive conversation, capture it as a structured note in `sessions/` so that future-me and future-AI can reconstruct what happened and what was learned. Session files are **temporary working documents** — the important discoveries are expected to migrate into `psychological-map.md` over time.

## When to invoke

- The conversation surfaced something concrete: an observation, an insight, a felt shift, a stuck point.
- The user explicitly asks for a session summary.
- A pattern was named that might recur.

Do **not** invoke for short tactical exchanges or pure logistics.

## File to create

```
sessions/YYYY-MM-DD-<short-kebab-topic>.md
```

Use today's date. The topic should be 2–5 words, lowercase, kebab-case, descriptive enough to grep later. Examples: `pre-1on1-spike`, `saturday-flat-mood`, `partner-feedback-loop`.

If two sessions happen the same day on the same topic, append `-2`, `-3`, etc.

## Template

```markdown
# YYYY-MM-DD — <Topic Title>

## Context
<What was going on. The trigger or starting question. 2–5 sentences. Concrete details (who, when, where) when relevant.>

## Observations
<What was noticed — feelings, behaviors, body sensations, situations. Plain language. No interpretation here.>
- ...
- ...

## Insights
<What the conversation made clearer. These are interpretations and should be marked as such. Use phrases like "current hypothesis," "tentative read." Tag confidence in parens.>
- <insight> (confidence: low/medium/high)
- ...

## Open questions
<Things this session raised but did not resolve. Candidates for the Open Questions section of `psychological-map.md` if they recur.>
- ...

## Possible map updates
<Anything from this session that, if it recurs, should be considered for `patterns/` or `psychological-map.md`. Do not promote here — just flag.>
- ...

## Links
- Related sessions: <file>, <file>
- Related patterns: <file>
- Related experiments: <file>
- Related map sections: <section>
```

## Rules

- **Separate observations from insights.** The single most important rule of this template. An observation is something that happened. An insight is a story about what it means.
- **No reassurance language.** "And that's okay" / "this is normal" / "you're doing your best" do not belong in a session note. Just record.
- **Cite, don't repeat.** If a session is the third instance of a pattern, link to the prior two rather than restating.
- **Update the session log.** After writing the session file, add a one-line entry to `.ai/session-log.md`.
- **Flag, don't promote.** Even if the session screams "this is a core truth about me," only flag it in *Possible map updates*. Promotion happens via `update-map`, not here.
- **Sessions are temporary.** Treat them as evidence that may or may not migrate into the map. Most won't.
