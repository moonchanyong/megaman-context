# Debugging Mode Principles

## What This Mode Optimizes

This mode optimizes for fixing the right problem without wasting time on random edits.

It starts with a short quick-triage pass, then moves into deeper systematic debugging when the quick pass is not enough.

## Default Sequence

1. Understand the symptom and expected behavior.
2. Run a short quick-triage pass.
3. If the issue is obvious, make the smallest useful fix.
4. If the issue is not obvious, switch to deeper systematic debugging.
5. Explain what was learned, what changed, and what risk remains.

## Quick Triage Means

The quick pass is for fast orientation, not for guessing.

Use it to answer:

- where is the most likely failure surface
- what changed recently
- what is the fastest safe check
- whether there is an obvious small fix with clear evidence

Keep this pass short. If it is not producing confidence, stop and escalate.

## When To Escalate

Move into systematic debugging when:

- the first cause is not obvious
- the bug spans multiple components
- the first attempted explanation is weak
- the issue keeps coming back
- the user asks for deeper diagnosis

The user can also ask to skip quick triage and go straight into deep debugging.

## Systematic Debugging Rules

- do not stack multiple speculative fixes
- reproduce the problem when needed
- trace the failing path instead of patching the symptom
- compare working and broken paths
- form one hypothesis at a time
- use evidence to confirm or reject the hypothesis
- prefer root-cause fixes over surface-level patches

## What Good Output Looks Like

Good debugging output is easy to follow.

Prefer this order:

- `Symptom`
- `Quick Triage`
- `Deep Diagnosis`
- `Fix`
- `Remaining Risk`

## Avoid

- random edits
- broad rewrites during diagnosis
- calling a guess the root cause
- hiding the switch from quick triage to deep debugging
- spending too long in quick triage when evidence is weak
