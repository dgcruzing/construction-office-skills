---
name: itp-holdpoint-check
description: Build or check a construction ITP hold-witness-review pack against spec, drawings, and the planned activity including pre-pour and inspection records. Use when the user says ITP, hold point, witness point, inspection test plan, pre-pour, pre-cover, inspection checklist, or what records before we pour.
metadata:
  type: workflow
  version: "1.0"
  pack: construction-office-skills
  domain: construction-quality
---

# ITP / hold-point check

Quality gate before cover-up. The skill produces a checklist the inspector can stand on, not a quality essay.

## Inputs required

- Activity (e.g. ground slab pour, membrane, first-fix hydraulic, fire-stopping)
- Spec section + drawing refs
- Existing ITP if any
- Who holds authority (builder QA / client / certifier / superintendent)
- Planned date/time of the activity
- Records already available (tickets, test results, photos, set-out)

## Point types (use these words only)

- **H — Hold** — do not proceed until signed
- **W — Witness** — invite the party; may proceed if they decline *in writing*
- **R — Review** — document check, not necessarily on site
- **S — Surveillance** — random / ongoing

If the project ITP uses different letters, copy the project letters and map them once at the top.

## Refuse list

- Do not invent spec clauses or acceptance criteria. Quote or mark UNKNOWN.
- Do not waive a hold point.
- Do not say "looks fine". Either the record exists or it is OPEN.
- Do not mix trades in one ITP unless the user supplied a combined pack.
- Do not sign.

## Method

1. Name the activity and the cover-up risk (what becomes inaccessible).
2. Build rows in process order — materials → set-out → prep → inspection → test → cover → as-built.
3. Each row needs — what / criteria / record / point type / who signs / status.
4. Status = `CLOSED` only if the user provided the record. Otherwise `OPEN` or `N/A`.
5. List **blockers** separately (missing ticket, expired cert, no reo inspection booked).
6. If no project ITP exists, draft a starter ITP and label it `DRAFT — not approved`.

Load `references/typical-hold-points.md` only when the user has no ITP and needs a starter list. Prefer the project ITP always.

## Output

Follow `assets/itp-checklist.md`.

```
HOLD POINT — not approved / not signed
```

## Optional VET map

Only if asked. Quality planning (ITP), assurance (hold points), control (records). No competency claim.

## Done when

- Every row has point type + record type + signer role.
- OPEN items are listed as blockers.
- No invented criteria.
