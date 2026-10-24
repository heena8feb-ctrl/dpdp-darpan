# Retention and erasure

## The DPDP rules
1. **Erase when the purpose is done or consent is withdrawn, whichever is earlier** — and have
   processors erase too — unless retention is necessary to comply with law. (s.8(7))
2. **Deemed end of purpose (Third Schedule platforms only):** e-commerce and social media
   intermediaries with ≥ 2 crore registered users in India, and online gaming intermediaries with
   ≥ 50 lakh, must treat the purpose as over after **3 years** without the user approaching them
   or exercising rights, and give a **48-hour warning** before erasure. (s.8(8), Rule 8)
3. **Minimum retention of logs/traffic data:** every Data Fiduciary keeps personal data,
   associated traffic data and processing logs for **at least one year** from processing, for
   the specified purposes (security investigation, compliance with Government information
   requests etc.), unless other law requires longer. (Rule 6, Rule 8(3) — verify exact scope.)
4. **Right to erasure on request** — unless retention is needed for the specified purpose or for
   legal compliance. (s.12)

All from 13 May 2027.

## How to review a retention statement
Good statements give, per data category: **trigger → period → what happens (delete/anonymise)
→ legal basis for any longer retention**.

| ❌ Weak | ✅ Better |
|---|---|
| "We keep your data as long as necessary." | "We delete your account details 90 days after you close your account, except invoices, which we keep for 8 years because tax law requires it." |
| "Data is retained indefinitely for business purposes." | "Marketing preferences are kept until you withdraw consent; then we stop within 7 days and delete within 30." |
| "Call recordings may be stored." | "Service-call recordings are kept for 90 days for quality and dispute resolution, then deleted." |

## Common legal retention drivers (verify current periods; don't over-extend)
| Law | What | Typical period |
|---|---|---|
| Companies Act, 2013 s.128 | Books of account and vouchers | 8 years from relevant financial year |
| CGST Act, 2017 s.36 | Accounts and records | 72 months from due date of annual return |
| Income-tax Act (and successor law) | Accounts and documents | Varies — verify |
| PMLA, 2002 + RBI KYC Master Direction | KYC and transaction records (regulated entities) | 5 years after relationship ends / transaction |
| CERT-In Directions 2022 | ICT system logs | 180 days, within India |
| Labour codes / state shops & establishments rules | Wage, attendance, leave registers | Varies by code/state — verify |
| Consumer warranty / product liability | Purchase and warranty records | Contract/limitation driven — justify |
Only the data the law actually requires can be kept for that law's period — not the whole profile.

## Retention patterns to recommend
- **Segregate** legally-retained data from active systems; restrict access; no reuse.
- **Anonymise** (irreversibly) for analytics instead of keeping identifiable data.
- **Propagate deletion** to processors, CRMs, ad platforms (custom audiences), data warehouses,
  backups (on their rotation cycle), call-recording stores, email marketing lists.
- **Log deletion events** (what, when, by whom) — without keeping the deleted content.
- **Inactivity policy** even if not a Third Schedule platform — best practice.

## Typical categories to cover in a schedule
Account/profile · contact details · identity documents / KYC · transaction and invoice records ·
service tickets · call/chat recordings and transcripts · marketing consents and preferences ·
cookies/analytics identifiers · device data and logs · location · uploaded files/photos ·
derived data (scores, segments, model features, voiceprints) · consent records (keep as long as
needed to prove consent — s.6(10); consent managers keep 7 years) · grievance/rights-request records.
