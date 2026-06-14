# Command: close-experiment

## Purpose

Review a completed (or abandoned) experiment. Extract the learning. Feed it back into `patterns/` and, when warranted, propose updates to `psychological-map.md`.

## When to invoke

- The experiment's review date has arrived.
- The experiment's failure criteria were tripped.
- The user decided to stop, regardless of the original timeline.

Even an abandoned experiment gets a close-out. "We abandoned this and why" is a real finding.

## Procedure

1. Open the experiment file in `experiments/`. Read the original hypothesis, success criteria, failure criteria, and run notes.
2. Compare the run notes against the pre-registered success/failure criteria. Do not redefine them now.
3. Decide the result.
4. Append the close-out section (below) to the experiment file. Update the status field to `complete` (or `abandoned`).
5. If the experiment produces a candidate update to `patterns/` or `psychological-map.md`, flag it in the close-out — do not write directly to those files here. Promotion goes through `update-map`.
6. Log it in `.ai/session-log.md` with `→ experiment:<name> closed`.

## Template (append to the experiment file)

```markdown
---

## Closed: YYYY-MM-DD

## Result
<Supported / Not supported / Inconclusive / Abandoned. One paragraph stating what actually happened against the pre-registered criteria. No relitigating the criteria. No "well, kind of.">

## What Worked
<Parts of the protocol that produced real signal or felt sustainable. Be specific.>

## What Didn't
<Parts of the protocol that broke down, were skipped, or produced no signal. Be specific. Include avoidance: if a step was repeatedly dodged, name it.>

## Lessons Learned
<What is now believed more strongly, less strongly, or differently because of this experiment. Distinguish lessons about *the user* from lessons about *the experiment design*.>

## Psychological Map Updates
<Concrete proposals for `patterns/` or sections of `psychological-map.md`. For each, state: which file/section, what entry to add/change, what evidence supports it. These are proposals — actual edits happen via `update-map`.>

- Proposal: ...
- Proposal: ...
```

## Rules

- **No moving the goalposts.** The success/failure criteria were defined upfront. They are the criteria.
- **An honest negative result is a finding.** "Hypothesis not supported" is as valuable as confirmation. Do not soften it.
- **Abandonment counts.** Record why it was abandoned (boredom, drift, life circumstances, fear). The reason is often the most useful artifact of the experiment.
- **Do not promote to `psychological-map.md` from this command.** Stage proposals only.
- **Check against the success metric.** If the experiment "succeeded" by making life smaller (more avoidance, less engagement), that is not actually success.
