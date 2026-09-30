---
name: rfi-drafter
description: Draft a single-question construction RFI with drawing and spec references, options, and date information is needed. Use when the user says RFI, request for information, clarification, drawing clash, spec conflict, or needs a question sent to the superintendent, architect, or consultant.
metadata:
  type: workflow
  version: "1.0"
  pack: construction-office-skills
  domain: construction-pm
---

# RFI drafter

One RFI = one question. Information only. If the source is actually a variation, stop and say so — hand off to `variation-eot-draft`.

## Inputs required

- Project name / number
- Raised by (name + company)
- Location / area / grid / level
- Drawing number + revision
- Spec section / clause if known
- What is unclear (quote the conflict in the source documents)
- Date information is needed by
- Suggested options if the site already has them
- Related RFI / VO / NCR numbers if any

## Refuse list

- Do not invent drawing revisions or spec clause numbers. Write `UNKNOWN` and ask.
- Do not request a design change dressed as clarification. Call that a variation pathway.
- Do not put two unrelated questions in one RFI. Split them.
- Do not assert entitlement, cost, or time in the question body.
- Do not send the RFI.

## Method

1. State the **documented condition** (drawing X rev Y says A; spec Z says B; site condition is C).
2. State the **gap** in one sentence.
3. Ask **one** closed or bounded question.
4. Offer **options** only if they were supplied or are obvious alternatives already on the drawings. Label them A/B/C. Do not recommend unless asked.
5. State the **need-by date** and what is blocked (pour, order, shop drawings, hold point).
6. List attachments. If photos or mark-ups are missing, put them under **Missing attachments**.

Read `references/au-construction-notes.md` only when the user names a contract family or asks whether this is an RFI or a VO.

## Output

Follow `assets/rfi-template.md`.

Closing block:

```
HOLD POINT — not issued
Number: assign from project register
```

## Optional VET map

Only if asked. Quality planning / assurance artefact (information control, RFI register). No competency claim.

## Done when

- One question only.
- Every document reference is copied from the source or marked UNKNOWN.
- Blocked work and need-by date are explicit or marked UNASSIGNED.
