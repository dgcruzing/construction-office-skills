---
name: ncr-punch-writer
description: Write a construction NCR, punch item, or defect notice with clause or drawing reference, evidence required, disposition, and close-out status. Use when the user says NCR, non-conformance, punchlist, snag, defect, defective work, or close-out item.
metadata:
  type: workflow
  version: "1.0"
  pack: construction-office-skills
  domain: construction-quality
---

# NCR / punch writer

Defect first. Money later. Disposition is a status machine, not a vibe.

## Status machine

`OPEN` → `DISPOSITION SET` → `REWORK / USE-AS-IS / REJECT` → `VERIFY` → `CLOSED`

Do not jump to CLOSED without a listed verification record.

## Inputs required

- Location (grid / level / room / element)
- What is non-conforming (observed)
- What it should have been (drawing / spec / ITP / approved sample)
- How found (ITP, walk, client, certifier, photo)
- Photos
- Trade / subcontractor if known
- Severity (safety / waterproof / structural / finish / documentation)

## Refuse list

- Do not invent the required standard. Quote or UNKNOWN.
- Do not approve use-as-is. That is a named authority decision.
- Do not price the defect unless asked and rates are supplied — then hand a pointer to `variation-eot-draft` if backcharge is the path.
- Do not close from a photo description alone unless the user says the verifier accepted it.
- Do not send.

## Method

1. One defect per NCR unless the user explicitly wants a punch *list* — then one row per defect, same fields.
2. Observed vs required in two blocks. No blending.
3. Evidence now vs evidence to close.
4. Disposition options listed; selected only if the user or ITP owner chose one.
5. Recurrence note if the same defect appeared before (only if the source says so).

## Output

Follow `assets/ncr-template.md`. For a punch walk, also emit the register table at the top of that file.

```
HOLD POINT — not issued / not closed
```

## Optional VET map

Only if asked. Quality control + corrective action + lessons learned. No competency claim.

## Done when

- Observed and required are separate.
- Status is valid on the machine.
- Close-out evidence is named, not implied.
