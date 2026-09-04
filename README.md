# my-claude-skills

Personal collection of [Claude skills](https://docs.claude.com/en/docs/claude-code/skills) — small, reusable procedures (steps, output format, and rules) that Claude follows the same way every time instead of improvising from scratch on each request.

Each skill lives in its own folder under `skills/` as a `SKILL.md` file with YAML frontmatter (`name`, `description`) followed by the instructions.

## Skills

| Skill | What it does |
|---|---|
| [`email-triage`](skills/email-triage/SKILL.md) | Sweeps an inbox batch, sorts messages into fixed buckets (Urgent, Money & Subscriptions, Needs Reply, Needs Action, FYI, Can Ignore), drafts replies for anything a person is waiting on, and flags exact amounts/dates for anything money-related. |

## Using a skill

Point Claude (or another assistant that supports this format) at the `SKILL.md` file, or copy its contents into a custom skill / project instructions. The frontmatter `name` and `description` are what a skill-aware assistant uses to decide when to apply it; the body is the exact procedure to follow.

## Adding a new skill

1. Create a new folder under `skills/<skill-name>/`.
2. Add a `SKILL.md` with frontmatter (`name`, `description`) and the procedure: steps in order, a fixed output format, and any rules that should apply the same way every time.
3. Add a row to the table above.
