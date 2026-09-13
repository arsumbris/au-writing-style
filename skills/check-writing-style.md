---
type: mcp.skill::au-mcp-sdk
name: check-writing-style
description: Audits a note's prose against the active house writing voice and reports where it breaks the writing-rules, rule by rule, without rewriting. Use when the human asks to check, audit, or review a note against the writing style, to find style violations, or to see whether it holds the house standard. Do not use to fix or rewrite a note (that is apply-writing-style), for the discipline rules (those are au-rules), or on code, data, or quoted text.
---

# check-writing-style

Report where the note breaks the chosen voice's rules.
Do not rewrite it.

Read for rule breaks, even in prose you agree with.
Prefer a fresh reader.
You skim past a line you would have written yourself.

## Steps

### 1. Choose the voice

Use the first available profile:

1. The profile the human specifies for this task
2. The active injected profile identified by the launch context
3. [[core-profile::au-writing-style]]

Find profiles with `au_instances_of {ofType: "writing-profile::au-writing-style", resolve: true}`.

Read the chosen profile and only its effective `rules`, in order.
Read any missing rule bodies in full.

### 2. Read the whole note

Read the note before marking rule breaks.

### 3. Mark each rule break

For every line of prose that breaks a rule, record:

- The line
- The rule it breaks
- The fix

### 4. Report the findings

Group findings by rule so repeated breaks read as one pattern.
Put clear breaks before judgment calls, worst first within each group.

Distinguish the two:

- Clear breaks include an em-dash or two facts on one line
- Judgment calls include an adjective that may add nothing
- Use the same distinction for other findings

## Discipline

**Use judgment**

The voice is advice.
Skip a rule that does not fit the note.

**Stop at the report**

`apply-writing-style` makes the fix.
