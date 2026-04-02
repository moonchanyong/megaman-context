# megaman-context

Shared mode repository for `megaman`.

This repository contains reusable remote modes that can be synced into a `megaman`-enabled project.

Repository URL:

- `https://github.com/moonchanyong/megaman-context`

## Representative Modes

- `megaman-onboarding`
  - product onboarding mode for first-time `megaman` users
  - explains what `megaman` is, how the CLI flow works, and checks understanding with short teach-back questions
- `debugging`
  - bug-solving mode with a two-stage workflow
  - starts with quick triage, then escalates to deeper systematic debugging if the quick pass is not enough
  - users can skip the quick triage pass when they want
- `implementation`
  - delivery mode for code changes
  - uses `obra/superpowers` project-local skills and encourages subagent delegation when work can be split safely

## Reference Integration Modes

These are useful when teams want the original upstream operating pack without adding extra wrapper instructions.

- `superpowers`
  - source: `https://github.com/obra/superpowers`
  - projects the raw `obra/superpowers` skills into `.claude/skills` and `.agents/skills`
- `aidlc-workflows`
  - source: `https://github.com/awslabs/aidlc-workflows`
  - projects the raw AIDLC root `AGENTS.md` and supporting rule details into the repository

## Current Modes

- `megaman-onboarding`
- `debugging`
- `implementation`
- `aidlc-workflows`
- `superpowers`

Typical usage from a project that already ran `megaman init`:

```bash
megaman sync megaman-context
megaman mode list
megaman mode apply megaman-context/megaman-onboarding
```
