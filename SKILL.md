---
name: agile-bud
description: >
  Write a developer-ready agile feature request from a rough idea.
  Use when someone asks for a feature request, user story, backlog item,
  ticket, or to turn a product gap into something engineering can estimate.
---

# Agile-Bud

Translate a raw idea into one backlog item. Write in plain language. Ask only for what you cannot infer. Do not invent customers, metrics, or API behavior.

## Gather

If the user already supplied enough to draft, draft. Otherwise ask one question at a time, in this order:

1. What should the product do that it does not do today?
2. Who is affected?
3. What breaks or hurts without it?
4. How would someone know it is done?

## Write

Produce the title and the body together. No "Title:" or "Description:" labels.

### Title

`[Area] Verb-led title` under 12 words. Area examples: Search, API, Admin, Upload, Reporting, Integrations.

### Body

**As a** [user]
**I want** [capability]
**So that** [outcome]

**Problem**
One to three sentences. Name the current workaround if you know it.

**Proposed behavior**
What the user can do when this ships. Describe behavior, not a design. Leave implementation choices to engineering.

**Acceptance criteria**
Checklist, or Given / When / Then when the flow has branches. Each item is observable.

**Developer handoff**

- In scope:
- Out of scope:
- Affected surfaces: UI, API, permissions, data, or integrations. Write "unknown" if not stated.
- Permissions: who can do this, and who cannot.
- Edge cases: empty, partial failure, and the existing behavior this must not break.
- How to verify: the check a developer or reviewer runs.

**Assumptions**
List anything you inferred. Mark gaps as `[confirm]`.

**Priority signal**

- Customer-reported: Yes / No / Unknown
- Affects more than one customer: Yes / No / Unknown
- Blocks a deal or renewal: Yes / No / Unknown

## Rules

- Stay under 400 words unless the user asks for more.
- Do not add story points, stack choices, or a schema the user did not describe.
- If the idea is too vague to estimate, say what is missing in Assumptions and still give a best-effort draft.
