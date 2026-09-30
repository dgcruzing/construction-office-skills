---
name: meeting-minutes-actions
description: Turn a construction site, PCG, toolbox, kick-off, or client meeting into minutes plus an action register with owner and due date. Use when the user says minutes, toolbox talk, PCG, kick-off, site meeting, coordination meeting, or extract actions from a transcript or notes.
metadata:
  type: workflow
  version: "1.0"
  pack: construction-office-skills
  domain: construction-pm
---

# Meeting minutes + action register

Produce minutes the office can file and an action table a PM can chase. Do not write a narrative essay.

## Inputs required

Collect before drafting. Mark anything missing as `UNKNOWN`.

- Meeting type (toolbox / site coord / PCG / kick-off / client / other)
- Date, time, location or call link
- Project name + number
- Chair
- Attendees (name + company + role)
- Apologies
- Source (transcript, notes, recording summary, email chain)
- Prior action register if supplied

## Refuse list

- Do not invent attendees, decisions, or commitments.
- Do not assign an owner unless the source names one. Use `OWNER UNASSIGNED`.
- Do not set a due date unless spoken or already in the register. Use `DATE UNASSIGNED`.
- Do not send the minutes. Stop at draft.
- Do not convert a commercial claim into a "decision" unless someone with authority said it.

## Method

1. Separate the source into **decisions**, **information**, and **actions**. Drop small talk.
2. One decision = one bullet. Include who decided if stated.
3. One action = one row. Verb + object + object location (drawing / area / spec) if given.
4. Carry forward open actions from a prior register. Mark `OPEN`, `DONE`, or `SUPERSEDED`. Do not silently drop them.
5. Flag risks or programme items mentioned, even if no action was assigned — put them under **Watch items**.
6. If the source is messy, list **Clarifications needed** instead of guessing.

## Output

Follow `assets/minutes-template.md`. Keep it short.

After the minutes, add:

```
HOLD POINT — not issued
Distribution list: UNKNOWN unless supplied
```

## Optional VET map

Only if asked. Map to BSBPMG422-style evidence — meeting record, action follow-up, quality/comms control. One line per element. No competency claim.

## Done when

- Every action row has Owner and Due columns filled with a value or `UNASSIGNED`.
- Decisions and actions are not mixed.
- No invented names or dates.
