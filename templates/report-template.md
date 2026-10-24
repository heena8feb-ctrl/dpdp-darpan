# Report template

Use this structure. Drop sections that don't apply (say "N/A" in one line rather than padding).

---

# DPDP Darpan review — [what was reviewed]

> **Regulatory status as at [TODAY]:** DPDP Act 2023 and DPDP Rules 2025 (G.S.R. 846(E)) are
> being phased in. Board provisions in force since 13 Nov 2025; consent-manager rules from
> 13 Nov 2026; notice, consent, security, breach, erasure, children's data and rights from
> **13 May 2027**. [Update-check result: e.g. "No changes found in a search on [date]" /
> "New: … (source)" / "Couldn't check for updates — snapshot dated 24 Oct 2026."]

## Verdict: [🔴 Significant gaps | 🟠 Needs work | 🟢 Largely aligned (on what's visible)]
[1–2 sentences on the overall picture.]

**Fix these first**
1. …
2. …
3. …

Findings: [n] Critical · [n] High · [n] Medium · [n] Low · [n] Advisory

## Scope and assumptions
- Reviewed: [artefact, version/date, screens/fields seen]
- Data Fiduciary: [org] · Processors: [known vendors]
- Data Principals: [customers / employees / candidates / children possible?]
- Sector overlays: [list or none]
- Assumptions: [each assumption stated]
- Not visible: [backend, contracts, security, retention jobs…]

## Data inventory
| # | Data element | Mandatory? | Purpose stated | Basis (consent / s.7 clause) | Necessary? | Shared with | Retention stated |
|---|---|---|---|---|---|---|---|

## Findings
| ID | Sev. | Check | Law | Effective | What we saw | Why it matters | Fix |
|---|---|---|---|---|---|---|---|
| F1 | Critical | CON-01 Affirmative action | s.6(1) | 13 May 2027 | "Marketing updates ☑" pre-ticked | Pre-ticked box isn't a clear affirmative action, so the consent isn't valid | Untick by default; separate checkbox per purpose |

Sort by severity, then by user journey order. Quote the exact text you're flagging.

## Rewritten notice and consent text
[Ready-to-paste text built from `consent-notice-template.md`. Include: short standalone notice,
separate checkboxes, withdrawal line, rights, Board line, contact, language selector note.
Offer a Hindi line if the audience suggests it, marked "have a qualified translator check".]

## Proposed retention schedule
| Data category | Trigger | Period | Then | Legal basis for longer retention |
|---|---|---|---|---|

## Open questions (these decide compliance but weren't visible)
1. …

## Sector and adjacent-law flags
- [Law — what to check — status]

## Readiness roadmap (for plans/PRDs)
- **Before launch:** …
- **Before 13 May 2027:** …
- **Best practice:** …

---

### Verify current rules
This review reflects the DPDP Act, 2023 and DPDP Rules, 2025 as understood on **[TODAY]**
(status snapshot 24 Oct 2026; [update-check result]). The regime is being phased in, timelines
may be shortened by notification, and the Data Protection Board may issue standards and
guidance. **This is not legal advice.** Before relying on it, check:
- **MeitY** (meity.gov.in) — the Act, Rules, FAQs and latest notifications
- **e-Gazette** (egazette.gov.in) — search "Digital Personal Data Protection" for any new notification
- **India Code** (indiacode.nic.in) — the Act's current text
- **Data Protection Board of India** — guidance once operational
- [Sector regulator(s) flagged above]
…and consult a qualified Indian data-protection lawyer for decisions with legal consequences.
