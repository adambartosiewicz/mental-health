# Command: analyze-pattern

## Purpose

Sweep the whole repository — `sessions/`, `journal/`, `experiments/`, `patterns/`, `psychological-map.md`, and contextually `references/` — and identify recurring psychological patterns. Output a structured analysis the user can review.

This is the **detection** step. It does not write to `psychological-map.md` or to the domain pattern files. Promotion happens later, deliberately, through `update-map` or by editing the relevant `patterns/<domain>.md`.

## Procedure

1. Read all of `sessions/` and `journal/`. Take note of recurring words, situations, body responses, triggers, time-of-day effects.
2. Cluster recurrences into candidate patterns. A candidate needs **at least 3 instances on distinct days**.
3. For each candidate, gather:
   - direct evidence (sessions/journal that show the pattern)
   - **counter-evidence** (sessions/journal where the pattern would be expected but did not appear)
4. Cross-reference against existing entries in `patterns/` and `psychological-map.md`. Mark each candidate as `new`, `confirms existing`, `extends existing`, or `contradicts existing`.
5. If a reference in `references/` happens to describe a similar shape, **note the framing but do not let it substitute for evidence**. The user's own data is the only thing that counts toward promotion.
6. Produce the report below.

## Output format

For every detected pattern, output:

```markdown
### Pattern: <short name>

- **Description:** <one-paragraph plain description of the pattern>
- **Evidence:**
  - `sessions/2026-05-18-...md` — <one-line note>
  - `journal/...` — <one-line note>
  - ...
- **Counter-evidence:**
  - <situations or sessions where the pattern would have been expected but did not appear>
  - <if there is none, say so explicitly — that is itself a finding>
- **Confidence:** low / medium / high
  - Justify in one sentence. Confidence should reflect breadth of evidence, not strength of feeling.
- **Possible experiments:**
  - <one or two behavioral tests that could move the question>
- **Relation to existing map:** new / confirms / extends / contradicts <entry>
- **Relevant references (framing only):** <if any reference applies — do not treat as evidence>
```

End the report with a short **Promotion recommendation** section that suggests, for each pattern: keep watching, add to `patterns/`, add to `psychological-map.md`, or design an experiment.

## Rules

- **Counter-evidence is mandatory.** A pattern reported without an honest search for counter-examples is not a finding.
- **Confidence is calibrated.** "I feel sure" is not high confidence. High confidence requires breadth across time and contexts.
- **Name avoidance patterns explicitly.** If something is being systematically *not* discussed, that is itself a pattern worth flagging.
- **Do not write to `psychological-map.md` or `patterns/` from this command.** Output only.
- **Frameworks ≠ evidence.** A reference that fits beautifully is not a reason to promote anything.
