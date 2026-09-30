---
name: inbox-triage
description: Classify a construction office email, letter, or message pack and return severity, artefact type, one next action, and an unsent draft. Use when the user says triage, inbox, what do I do with this, email pack, letter from superintendent, or sort these messages.
metadata:
  type: workflow
  version: "1.0"
  pack: construction-office-skills
  domain: construction-pm
---

# Inbox triage

Sort first. Draft second. Never send.

## Inputs required

- The raw message(s) or a summary plus attachments list
- Project
- Today's date
- Known registers (RFI / VO / NCR) if the user pastes them
- Who the user is (site manager, PM, admin)

## Severity

| Code | Meaning | Typical clock |
|---|---|---|
| S1 | Safety, structural, stop-work, statutory | same shift |
| S2 | Time-bar / notice / hold-point blocker / payment schedule | this week, often days |
| S3 | Normal commercial or information | register + draft |
| S4 | FYI / spam / already closed | file or ignore |

If a contract notice period is unknown, still flag S2 when the text looks like a notice, direction, or claim. Do not invent the bar date.

## Artefact type

Pick one primary, plus secondary tags.

`RFI` `DIRECTION` `VARIATION` `EOT` `NCR` `PROGRAMME` `PAYMENT` `INSURANCE` `WHS` `MEETING` `TENDER` `ADMIN` `UNKNOWN`

If it is an RFI, next skill = `rfi-drafter`.
If it is extra work or delay = `variation-eot-draft`.
If it is a defect = `ncr-punch-writer`.
If it is a meeting = `meeting-minutes-actions`.

## Refuse list

- Do not send, reply-all, or file.
- Do not promise dates, dollars, or entitlement in the draft.
- Do not merge unrelated emails into one action.
- Do not downgrade a notice to S3 because the tone is polite.

## Method

1. One card per source message.
2. Quote the trigger sentence (the bit that makes it S1/S2).
3. One next action. Verb + artefact + owner-role + by-when.
4. Draft reply only if a reply is actually required. Mark `UNSENT`.
5. List attachments that must travel with the next artefact.

## Output

Follow `assets/triage-card.md`. For a pack, emit a table first then cards for S1/S2 only.

```
HOLD POINT — no message sent
```

## Done when

- Every item has S-code + artefact type + exactly one next action.
- Drafts contain no invented commitments.
