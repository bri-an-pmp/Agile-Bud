# Agile-Bud

Turns a rough product idea into a backlog item a developer can estimate and implement.

The public description is the whole product today: there is no app, API, or model host in this repo. Agile-Bud is a skill file. Point an assistant that loads `SKILL.md` at a feature idea and it writes a ticket with a user story, acceptance criteria, and a developer handoff.

## What you get

- A title and a paste-ready description for Jira, Linear, or monday.com
- Assumptions called out instead of invented requirements
- A developer handoff: scope, non-goals, affected surfaces, permissions, edge cases, and how to verify

## What this repo does not include

- A hosted model or a chat UI
- Ticket creation in Jira or any other tracker
- Implementation of the feature being described

## Use it

1. Load [`SKILL.md`](./SKILL.md) as a skill, or paste it into the assistant's instructions.
2. Describe the feature, who it is for, and the pain it removes.
3. Paste the result into the backlog. Confirm anything marked `[confirm]`.

## Layout

| Path | Purpose |
| --- | --- |
| `SKILL.md` | Instructions and output contract |
| `examples/share-links.md` | Sample ticket produced by the skill |
