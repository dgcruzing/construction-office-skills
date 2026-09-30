# Construction Office Skills Pack

Repo: https://github.com/dgcruzing/construction-office-skills  
License: MIT

Eight portable Agent Skills for construction managers, PMs, and site/office staff.

Format: open Agent Skills (`SKILL.md` + `assets/` + optional `references/`).
Same folders run in Claude Code, Cursor, Grok Bot / Grok Build, Codex, Copilot, OpenCode.

These are **jobs**, not personas. One skill = one artefact. Human hold-point on every send / commercial commit.

## Skills

| Folder | Job | Trigger examples |
|---|---|---|
| `meeting-minutes-actions` | Minutes + action register | toolbox, PCG, kick-off, site meeting |
| `rfi-drafter` | One-question RFI pack | RFI, clarification, drawing conflict |
| `daily-site-diary` | Daily diary / site report | diary, daily report, labour and plant |
| `inbox-triage` | Classify + one next action | inbox, email pack, what do I do with this |
| `itp-holdpoint-check` | ITP / hold-witness-review | ITP, pre-pour, hold point, inspection |
| `variation-eot-draft` | VO / EOT draft (fact vs claim) | variation, EOT, delay notice, extra work |
| `ncr-punch-writer` | NCR / punch / defect | NCR, punchlist, defect, snag |
| `tender-compare-matrix` | Tender comparison matrix | tender compare, quote matrix, bid tab |

## Install

Copy each folder into the harness skills directory. Folder name must match the `name:` field.

```text
Claude Code     ~/.claude/skills/<name>/SKILL.md
                <project>/.claude/skills/<name>/SKILL.md
Cursor          ~/.cursor/skills/<name>/SKILL.md
                <project>/.cursor/skills/<name>/SKILL.md
Grok Build      <project>/.grok/skills/<name>/SKILL.md
Grok Bot        paste SKILL.md → save as private skill
Shared drop     ~/.agents/skills/<name>/SKILL.md
```

Or symlink the whole pack:

```bash
ln -s /path/to/construction-office-skills/rfi-drafter ~/.claude/skills/rfi-drafter
```

Do not install all eight into a harness you use for unrelated work. Scope them to the project repo.

## House rules baked into every skill

- Separate **fact / interpretation / recommendation**.
- No invented quantities, clause numbers, dates, attendees, or dollars.
- Missing input → `UNKNOWN` + a question. Never fill the gap.
- Never send mail, never commit cost, never sign a variation.
- Output uses the template in `assets/` unless the user supplies their own form.
- Optional last section maps the artefact to VET/BSBPMG422 evidence if asked.

## Swap-in points

Replace the placeholders in each `references/project-defaults.md` (or delete that file and paste your real):

- contract form (AS 4000 / AS 2124 / ABIC / GC21 / bespoke)
- project name, number, superintendent / client
- RFI / NCR / VO numbering prefix
- diary distribution list
- hold-point authority matrix

## Author

Built for transferable office/site work. Tighten templates against your real Word/Notion forms before first live job.
