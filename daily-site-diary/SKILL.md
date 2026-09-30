---
name: daily-site-diary
description: Build a construction daily site diary or daily report from notes, voice dump, photos, or labour-plant lists. Use when the user says diary, daily report, site report, labour and plant, weather delay, deliveries, or write up today on site.
metadata:
  type: workflow
  version: "1.0"
  pack: construction-office-skills
  domain: construction-pm
---

# Daily site diary

A diary is a contemporaneous record. Precision beats prose. If a number was not given, write `UNKNOWN` — never estimate.

## Inputs required

- Project, date, shift, author
- Weather (am/pm) and site condition
- Labour by trade and company (count)
- Plant on site (type + idle/working if known)
- Work performed by area
- Deliveries
- Visitors / consultants / client / certifier
- Delays / disruptions / waiting
- Safety / incidents / permits / isolations
- Photos or photo filenames
- Instructions received on site

## Refuse list

- Do not invent headcount, hours, quantities, or plant hours.
- Do not diagnose blame for a delay. Record what was observed.
- Do not turn a diary into a variation claim. Point to `variation-eot-draft` if extra work or delay is described.
- Do not omit an incident if the source mentions one.
- Do not send or file. Draft only.

## Method

1. Date-stamp everything as the source date. If the user is writing next morning, say `Recorded {now} for shift {date}`.
2. Labour and plant as tables. Subcontractors named if given.
3. Work performed = area + activity + constraint. Example: `L2 grid C-D — formwork to soffit — waiting reo inspection`.
4. Delays get start/finish if known, else `duration UNKNOWN`.
5. Photo list must include what each photo is supposed to show. If files exist but captions do not, list filenames under **Uncaptioned photos**.
6. Instructions from superintendent / client go in their own section with who said them. These are gold in a dispute.

## Output

Follow `assets/diary-template.md`.

```
HOLD POINT — not issued to distribution
```

## Optional VET map

Only if asked. Quality record + communications + lessons (if a delay/incident is recorded). No competency claim.

## Done when

- Date and author present.
- Every quantity is sourced or UNKNOWN.
- Delays and instructions are isolated from general narrative.
