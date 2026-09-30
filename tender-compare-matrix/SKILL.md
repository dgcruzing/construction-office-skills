---
name: tender-compare-matrix
description: Build a construction tender or quote comparison matrix covering price, exclusions, programme, insurances, bonds, and qualifications without picking a winner. Use when the user says tender compare, bid tab, quote matrix, compare subcontractors, compare builders, or tender assessment.
metadata:
  type: workflow
  version: "1.0"
  pack: construction-office-skills
  domain: construction-commercial
---

# Tender compare matrix

Apples vs apples. Highlight gaps. Do not award.

## Inputs required

- Trade / package name
- Tender documents issued (drawings rev, spec, programme, BoQ)
- Each bidder return (price schedule, cover letter, qualifications)
- Closing date
- Evaluation criteria if the client has them

If only lump sums arrived and no BoQ, say so and compare at cover-letter level plus exclusions.

## Refuse list

- Do not pick a winner or recommend award unless the user explicitly asks for a *recommendation after* the matrix, and even then label it `RECOMMENDATION — not an award`.
- Do not invent line items a bidder omitted — mark `NOT PRICED` / `MISSING`.
- Do not normalise by silently adding numbers. Show an **adjusted** column only when the user supplies the adjustment rule.
- Do not hide a qualification in a footnote. Put it on the matrix.
- Do not send to bidders.

## Method

1. Build a common WBS / BoQ spine from the *issued* documents, not from the cheapest bidder.
2. One column per bidder.
3. Rows — lump sum, key BoQ lines, provisional sums, PC items, prelims, exclusions, inclusions, programme weeks, start constraint, insurances, bond / security, validity period, qualifications, non-conformances to the tender.
4. Flag **non-conforming** returns at the top (late, wrong spec, missing schedule).
5. Money as stated in the return currency. Note GST treatment if given.
6. End with **Gaps to close before award** — questions, not scores, unless a scoring sheet was supplied.

## Output

Follow `assets/tender-matrix.md`. Prefer a markdown table. If a spreadsheet is requested and an xlsx skill exists in the harness, use it — still keep this schema.

```
HOLD POINT — not an award recommendation unless separately requested
```

## Optional VET map

Only if asked. Procurement evidence + evaluation record. No competency claim.

## Done when

- Every missing line is visible as MISSING / NOT PRICED.
- Qualifications are in the matrix, not buried.
- No winner is selected by default.
