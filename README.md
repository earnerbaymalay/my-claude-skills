# my-claude-skills

Personal collection of Claude skills — small, written-down procedures that Claude follows the same way every time instead of improvising fresh on each request.

## How skills work

A skill is basically: *"here's exactly how I want you to do this recurring task,"* saved once instead of re-explained every time. Each one is a `SKILL.md` file with three parts:

- **Steps** — the exact order of operations, followed the same way every run.
- **Format** — the fixed shape of the output (sections, structure), so it looks the same every time instead of drifting.
- **Rules** — the judgment calls made consistently: what to do when something's unsure, what never gets invented, what gets flagged instead of guessed at.

That last part is the one people usually skip and shouldn't — steps and format are easy, but the rules are what stop the output from being slightly different (or slightly wrong) each time you ask.

Every `SKILL.md` starts with YAML frontmatter:

```yaml
---
name: skill-name
description: "One line describing what this handles and when to use it"
---
```

The `description` matters more than it looks — it's what a skill-aware assistant reads to decide *when* to reach for this skill on its own, so write it as a trigger ("use this when X"), not a summary of what it does.

## Using a skill

- **Claude (Skills feature, e.g. Cowork or Claude.ai):** paste a `SKILL.md`'s content in and ask Claude to save it as a skill, or point Claude at this repo and ask it to adopt one.
- **Any other assistant with custom instructions / system prompts:** paste the body (steps/format/rules) in as project or custom instructions — the format is plain enough to work anywhere.
- Treat everything in this repo as a starting point, not a finished template — the real value is in running a skill against one of your own real examples and tightening the rules based on what breaks. That's how `email-triage` below got built.

## Adding a new skill

1. Create a new folder: `skills/<skill-name>/`.
2. Add a `SKILL.md` inside it with:
   - Frontmatter — `name` (kebab-case, matches the folder name) and `description` (a one-line trigger sentence).
   - **Steps** — the order of operations, always the same.
   - **Format** — the exact output shape, no variation.
   - **Rules** — what to do when unsure, what never to invent, what to flag rather than guess.
3. Test it on one real example before committing it — a skill that's never touched real input usually has at least one rule that doesn't survive contact with reality. Fix that first.
4. Add a row to the table below.

## Skills

| Skill | What it does |
|---|---|
| [`email-triage`](skills/email-triage/SKILL.md) | Sweeps an inbox batch, sorts messages into fixed buckets (Urgent, Money & Subscriptions, Needs Reply, Needs Action, FYI, Can Ignore), drafts replies for anything a person is waiting on, and flags exact amounts/dates for anything money-related. |
