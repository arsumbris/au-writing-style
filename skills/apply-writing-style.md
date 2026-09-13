---
type: mcp.skill::au-mcp-sdk
name: apply-writing-style
description: Rewrites a note's prose into the active house writing voice, applying its writing-rules. Use when the human asks to restyle, reformat, tighten, or clean up a note, to apply the writing style, or to bring it up to the house standard. Do not use to write new content, for the discipline rules (those are au-rules), or on code, data, or quoted text.
---

# apply-writing-style

Rewrite the note so the reader parses it faster.
Use the chosen voice as the standard.

Keep every claim that matters.
Cut filler.
Add nothing the note does not say.

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

Hold what it means.
Let go of how it says it.

### 3. Rewrite coarse to fine

Work through the voice's rule groups from top to bottom.

**Shape the note**

Split it into beats.
Give each beat air and a label where needed.

**Break the lines**

Put one sentence and one fact on each line.
Keep those lines inside the beats you shaped.

A wall of one-per-line sentences is still hard to scan.
Shape the beats before breaking the lines.

**Cut the words**

Apply the plain-word and cut-word rules.
Keep every claim that matters.

### 4. Check the result

Read the rewrite against the rules.
Then compare it with the old note.

Check that every claim that matters still stands.

### 5. Report the changes

Group the changes by the rule they apply.

## Discipline

**Use judgment**

The voice is advice.
Skip a rule that does not fit the note.

**Follow the chosen voice**

Apply that profile's rules.
The rewrite must read better, beyond changes to formatting.

**Prefer a fresh reader**

A fresh reader catches words the writer would keep.
