# Implementation Mode Principles

## What This Mode Optimizes

This mode optimizes for shipping useful code changes quickly without losing coordination.

It prefers focused execution, clear ownership, and selective subagent delegation when work can be split safely.

## Default Sequence

1. Restate the target and identify the affected files or systems.
2. Decide whether the work should stay local or be split.
3. Delegate only the parts that are truly independent.
4. Keep the main path moving while delegated work runs.
5. Integrate results in one place and explain the outcome clearly.

## When To Delegate

Delegation is useful when:

- tasks are independent
- write scopes can be separated
- the main agent can keep moving on the critical path
- parallel work will reduce waiting time

Delegation is not useful when:

- the task is tiny
- the next step depends on immediate shared context
- the split creates more coordination cost than speed

## Delegation Rules

- give each subagent one concrete job
- define ownership clearly when files are involved
- avoid overlapping write scopes when possible
- keep cross-cutting decisions with the main agent
- integrate results centrally instead of letting workers drift apart

## What Good Output Looks Like

Prefer this order:

- `Goal`
- `Plan`
- `Delegation`
- `Integration`
- `Remaining Risk`

## Avoid

- delegation for its own sake
- handing off the critical path and waiting idly
- overlapping ownership without a reason
- letting subagents expand scope
- over-engineering small changes
