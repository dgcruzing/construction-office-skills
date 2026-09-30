---
name: variation-eot-draft
description: Draft a construction variation or extension of time notice with fact, entitlement pathway, time, and money kept in separate lanes. Use when the user says variation, VO, variation order, EOT, delay notice, extra work, direction to change, latent condition, or claim draft.
metadata:
  type: workflow
  version: "1.0"
  pack: construction-office-skills
  domain: construction-commercial
---

# Variation / EOT draft

Commercial artefact. Separate lanes or it becomes mush.

**Fact** — what happened, who said it, when, which document.
**Entitlement pathway** — which contract machinery *might* apply. No clause number unless the user supplied the contract extract.
**Time** — activities hit, days claimed only if calculated from supplied programme data.
**Money** — rates / hours / quantities only if supplied. Else `QUANTUM NOT PRICED`.

## Inputs required

- Contract family if known (AS 4000, AS 2124, AS 4902, ABIC, GC21, other)
- Direction / event date and how it arrived (site instruction, drawing rev, email, latent condition)
- Description of changed work or delay event
- Drawing / spec before vs after
- Programme activity IDs if any
- Cost build-up if any
- Notices already sent
- Diary / photo / RFI references

Read `references/au-construction-notes.md` when a contract family is named.

## Refuse list

- Do not invent clause numbers, notice periods, or time bars.
- Do not invent dollars, hours, or EOT days.
- Do not send to the superintendent or client.
- Do not waive rights or admit liability.
- Do not mix delay costs into the EOT days line. Keep two lines.
- Do not call it a "claim" in the subject if the user only asked for a notice draft and the contract uses "notice".

## Method

1. Classify — directed variation / constructive variation / EOT only / EOT + cost / late instruction / latent condition / UNKNOWN.
2. Write the fact chronology first (dated bullets).
3. Entitlement pathway in plain language plus `Clause: {supplied or UNKNOWN}`.
4. Time — impacted activities, float status only if given, days = UNKNOWN unless calculated from supplied dates.
5. Money — table of supplied rates. Subtotal only what was provided. Flag exclusions.
6. Records list — diary dates, photos, RFIs, instructions.
7. Add **Questions for PM** before anything would be issued.

If the source is only an information gap, stop and send the user to `rfi-drafter`.

## Output

Follow `assets/vo-eot-template.md`.

```
HOLD POINT — not issued
Not a payment claim. Not legal advice.
```

## Optional VET map

Only if asked. Change control + communications + lessons. No competency claim.

## Done when

- Four lanes exist and do not leak into each other.
- Every number has a source or is UNKNOWN.
- Issue block is explicit.
