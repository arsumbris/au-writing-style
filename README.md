---
type: au.engine.readme::au-engine
tldr: Reusable writing style profiles and three skills to apply, check and extend them. Includes a default profile focused on scannability.
---

# Repo Overview

> Work in progress and not thoroughly tested.
> Expect breaking changes.

## What this is

`au-writing-style` gives agents reusable writing style profiles.
Each profile selects rules that guide how the agent writes.

The default `core-profile` focuses on scannability.
It helps readers find the point quickly through clear structure and whitespace.
Its rules favor short sentences and plain words.

## How to use this

Depend on `au-writing-style`.
Select a profile in your agent launch to load its rules at session start.

Load the skills your task needs:

| Skill | Use |
| --- | --- |
| apply-writing-style | Rewrite a note to the chosen style |
| check-writing-style | Report rule breaks without rewriting |
| write-a-rule | Turn a recurring correction into a reusable rule |

Apply and check use the profile you specify, otherwise the active injected profile.
With neither, they use `core-profile`.

## How to extend this

Create your own `writing-profile::au-writing-style` in your package.
Reuse existing rules or write `writing-rule::au-writing-style` notes for your own guidance.
Each profile selects at least one rule.

Use `core-profile` as an example of bundling rules and loading them at session start.
The rules are guidance, so adapt them to the writing.
