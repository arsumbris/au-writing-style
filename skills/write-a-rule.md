---
type: mcp.skill::au-mcp-sdk
name: write-a-rule
description: Authors one new writing-rule note in the house voice, capturing something you keep correcting by hand as one reusable move. Use when the human wants to add a writing rule, turn a recurring correction into a rule, or extend the voice with a new move. Do not use to rewrite a note (that is apply-writing-style), to audit one (that is check-writing-style), or for the discipline rules (those are au-rules).
---

# write-a-rule

Capture a recurring correction as one reusable `writing-rule`.

The title names the move.
The body explains how to make it.

A rule becomes active when a profile's `rules` field names it.
Writing and bundling are separate steps.

## Steps

### 1. Name one move

"start with the point" names one move.
"start with the point and cut the hedging" names two.

If the title needs an "and", split it into two rules.

### 2. Read the craft and an example

Read the `writing-rule` docstring with `au_type {name: "writing-rule", repo: "au-writing-style"}`.

Read [[say it plain::au-writing-style]] as the example.
Use its shape to write your own content.

### 3. Write the rule

Write the note in `rules/` in the intended authoring repo.
Match the body shape you just read.

In a consuming repo, claim `type: writing-rule::au-writing-style`.
The example's local type claim belongs to its own repo.

### 4. Check the rule

Read the new file's diagnostics.
Expect zero.

Check that the rule appears in `au_instances_of {ofType: "writing-rule::au-writing-style"}`.

### 5. Bundle the rule

**Choose the profile**

Find profiles with `au_instances_of {ofType: "writing-profile::au-writing-style", resolve: true}`.
Choose the intended profile.

Read the profile and its outgoing references before editing it.

**Add the reference**

Use the profile's existing form.
Put the rule in its intended apply order.

Resolve the reference from the profile's repo.
Qualify the rule's owner when crossing repos.

**Check delivery**

Check the profile's diagnostics and generated launch output.
An unbundled rule stays inert.

### 6. Report the result

Name the rule you wrote.
State whether you bundled it.

## Discipline

**Keep examples generic**

Use a before-and-after example about writing.
"check and verify and confirm" becomes "check".

Keep real notes out of the example.

**Write in the voice**

The rule is a house note.
It follows the voice it joins.
