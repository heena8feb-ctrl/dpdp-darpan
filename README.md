# DPDP Darpan 🪞

**A Claude skill that holds your forms, app flows and data plans up to India's Digital Personal
Data Protection Act.**

*Darpan* (दर्पण) means mirror. Show it a signup form, a consent banner, a voice-bot script, an
HR portal or a whole PRD, and it returns:

- a dated **regulatory status banner** (what's in force today, what's coming, what's only proposed)
- a **verdict** and the top three fixes
- a **data inventory** — every field, its purpose, its lawful basis and whether it's necessary
- **graded findings** (Critical → Advisory), each with a check ID, section or rule, effective date and a concrete fix
- **rewritten notice and consent text**, ready to paste (with a Hindi option)
- a proposed **retention schedule**
- **sector flags** (RBI, TRAI, CERT-In, Aadhaar, health, insurance, labour, CCPA dark patterns)
- a **"verify current rules" footer** pointing to MeitY, the e-Gazette and India Code

## Why it always points to the current rules
The DPDP Act, 2023 and DPDP Rules, 2025 are being phased in:

| Date | What starts |
|---|---|
| 13 Nov 2025 | Board provisions |
| 13 Nov 2026 | Consent managers (Rule 4) |
| 13 May 2027 | Notice, consent, security, breach reporting, erasure, children's data, rights, penalties |

Amendments, removal-of-difficulties orders and a proposal to shorten the timeline have all
appeared since. The skill carries a dated snapshot, searches for updates when it can, and says
plainly when it can't.

## What it checks
Scope and roles · notice (s.5, Rule 3) · consent validity (s.6) · withdrawal · purpose
limitation and minimisation · legitimate uses (s.7) · retention and erasure (s.8(7), Rule 8) ·
children and persons with disability (s.9, Rules 10–12) · security (Rule 6) · breach readiness
(Rule 7) · processors and sharing · rights and grievance (Rule 14) · cross-border · SDF duties ·
legacy data · consent UX and dark patterns · sector overlays.

There are 100+ checks in total, each with a test, common red flags, the legal reference, an
effective date and a default severity.

## Install
Copy the `dpdp-darpan/` folder into your Claude skills directory, or upload it as a skill in
Claude's settings. Then ask, for example:

> "Run a DPDP check on this signup form" · "Is our IVR script DPDP-ready?" · "Review this
> consent text" · "Gap-check our lead-gen data plan for India"

## Structure
```
dpdp-darpan/
├── SKILL.md                         # workflow, rules, grading
├── reference/
│   ├── 00-regulatory-status.md      # dated snapshot + freshness protocol (read first)
│   ├── 01-act-section-map.md
│   ├── 02-rules-2025-map.md
│   ├── 03-master-checklist.md       # all checks with IDs
│   ├── 04-legitimate-uses-exemptions.md
│   ├── 05-retention-erasure.md
│   ├── 06-children-and-pwd.md
│   ├── 07-dark-patterns-ux.md
│   ├── 08-sector-overlays.md
│   └── 09-input-playbooks.md
├── templates/                       # report, notice/consent, clause library, inventory
├── examples/                        # five worked reviews
└── evals/evals.json                 # test prompts with expectations
```

## Keeping it current
Update `reference/00-regulatory-status.md` whenever MeitY notifies something new: change the
"Status as at" date, the phase table and the pending list. Every other file reads its effective
dates from there.

## Disclaimer
DPDP Darpan is a review aid, not legal advice. It can be wrong or out of date. Verify against
the official text and consult a qualified Indian data-protection lawyer before relying on it.
