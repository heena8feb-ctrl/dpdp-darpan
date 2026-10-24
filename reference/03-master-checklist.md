# Master checklist

Each check: **ID · what to test · red flags · law · effective · default severity.**
Result per check: `Aligned` · `Gap` · `Partial` · `Can't verify` · `N/A (reason)`.
Effective tags assume the 24 Oct 2026 snapshot — recompute against today's date.
"BP" = best practice, not a DPDP requirement.

---

## A. Scope and roles (SCOPE)

| ID | Test | Red flags | Law | Eff. | Sev. |
|---|---|---|---|---|---|
| SCOPE-01 | Is digital (or digitised) personal data processed? | Paper form later scanned/typed into a system is in scope | s.3(a) | 13 May 2027 | Info |
| SCOPE-02 | Offering goods/services to people in India from abroad? | Foreign entity assuming DPDP doesn't apply | s.3(b) | 13 May 2027 | High if missed |
| SCOPE-03 | Any reliance on the "publicly available" carve-out? | Scraped profiles, data published by third parties, "it's on LinkedIn" | s.3(c)(ii) | 13 May 2027 | High |
| SCOPE-04 | Data Fiduciary vs processor roles identified; joint fiduciaries named | Vendor deciding its own purposes (e.g. using data to train its model) — it's acting as a fiduciary | s.2, s.8(1)-(2) | 13 May 2027 | Medium |
| SCOPE-05 | Could the org be an SDF, or a Third Schedule platform? | High volume, sensitive data, social media/e-com ≥2 cr users, gaming ≥50 lakh | s.10, Rule 8, Rule 13 | 13 May 2027 | Advisory |
| SCOPE-06 | Lawful basis chosen for every purpose (consent or a specific s.7 use) | "Legitimate interest" (GDPR concept — doesn't exist in DPDP) | s.4, s.7 | 13 May 2027 | High |

## B. Notice (NOT)

| ID | Test | Red flags | Law | Eff. | Sev. |
|---|---|---|---|---|---|
| NOT-01 | Notice given **before or with** the consent request | Consent first, notice "available later"; notice only in footer | s.5(1) | 13 May 2027 | High |
| NOT-02 | Notice **standalone** and understandable on its own | Only a link to a 20-page privacy policy; notice merged into T&Cs | Rule 3(a) | 13 May 2027 | High |
| NOT-03 | **Itemised** list of personal data | "We collect your information", "personal details", "etc." | s.5(1)(i), Rule 3(b)(i) | 13 May 2027 | High |
| NOT-04 | **Specified purpose** for each item, with itemised goods/services/uses enabled | "To improve our services", "business purposes", "and other purposes" | s.5(1)(i), Rule 3(b)(ii) | 13 May 2027 | High |
| NOT-05 | How to **withdraw consent** — link + other means | No withdrawal route mentioned | s.5(1)(ii), Rule 3(c)(i) | 13 May 2027 | High |
| NOT-06 | How to **exercise rights** (access, correction, erasure, nomination, grievance) | Rights absent or "email us" with no address | s.5(1)(ii), Rule 3(c)(ii), Rule 14 | 13 May 2027 | High |
| NOT-07 | How to **complain to the Data Protection Board** | Board not mentioned | s.5(1)(iii), Rule 3(c)(iii) | 13 May 2027 | Medium |
| NOT-08 | Notice available in **English or any Eighth Schedule language**, at the user's choice | English only for a Hindi/regional-language audience; no language selector | s.5(3) | 13 May 2027 | Medium (High for vernacular audiences) |
| NOT-09 | **Clear and plain language** | Legalese, double negatives, long sentences, jargon ("pseudonymised telemetry") | Rule 3(b), s.6(3) | 13 May 2027 | Medium |
| NOT-10 | **DPO or contact person** details on the consent request | No contact named | s.6(3), s.8(9), Rule 9 | 13 May 2027 | Medium |
| NOT-11 | Recipients/sharing described (who gets the data, incl. processors by category) | "Trusted partners", "affiliates" with no description | BP (supports s.6(1) "informed"; s.11 access right) | — | Low |
| NOT-12 | Retention period or criteria stated | Nothing on how long data is kept | BP (supports informed consent; s.8(7)) | — | Low |
| NOT-13 | Cross-border processing disclosed where relevant | Offshore vendor/LLM not mentioned | BP (s.16) | — | Low |
| NOT-14 | Notice accessible (readable on mobile, screen-reader friendly, sufficient contrast) | Tiny grey text, image-only notice | BP (supports s.6(1) "informed") | — | Low |
| NOT-15 | Voice/IVR: notice delivered audibly before collecting data, with a way to hear it in another language and get it in writing | Notice only on website; recording starts silently | s.5, Rule 3 | 13 May 2027 | High |

## C. Consent validity (CON)

| ID | Test | Red flags | Law | Eff. | Sev. |
|---|---|---|---|---|---|
| CON-01 | **Clear affirmative action** | Pre-ticked boxes; "by continuing/using this site you agree"; silence or inactivity as consent; scroll-to-consent | s.6(1) | 13 May 2027 | Critical |
| CON-02 | **Specific** — separate consent per distinct purpose | One checkbox for service + marketing + sharing + profiling | s.6(1) | 13 May 2027 | Critical |
| CON-03 | **Unconditional / free** — service not conditioned on consent to unnecessary processing | "You must accept marketing to create an account"; app won't open without contacts permission | s.6(1) | 13 May 2027 | Critical |
| CON-04 | **Limited to necessary data** for the purpose | Asking for data the stated purpose doesn't need (see PUR) | s.6(1) and illustration | 13 May 2027 | High–Critical |
| CON-05 | **Informed** — notice elements present at the point of consent | See NOT-01 to NOT-10 | s.6(1), s.5 | 13 May 2027 | High |
| CON-06 | **Unambiguous** wording | "May", "might", "from time to time", "including but not limited to" | s.6(1) | 13 May 2027 | Medium |
| CON-07 | No clauses that waive statutory rights | "You agree not to complain", "you waive your right to erasure", "consent is irrevocable" | s.6(2) | 13 May 2027 | Critical |
| CON-08 | Consent request in clear, plain language, language choice offered | See NOT-08/09 | s.6(3) | 13 May 2027 | Medium |
| CON-09 | Consent captured **before** processing starts | Analytics/ad pixels or SDKs firing on page load; data sent before submit | s.6(1), s.4 | 13 May 2027 | High |
| CON-10 | **Consent records** — what notice version, what was consented, when, how, by whom; withdrawals logged | No consent log; can't tie consent to notice version | s.6(10) | 13 May 2027 | High |
| CON-11 | Consent obtained **by the right person** — parent for a child, guardian for a PwD | Child ticks box themselves | s.9(1), Rules 10–11 | 13 May 2027 | Critical |
| CON-12 | Consent manager integration (if used) — registered manager, consents/withdrawals honoured | Unregistered "consent platform" marketed as a Consent Manager | s.6(7)-(9), Rule 4 | 13 Nov 2026 | Medium |
| CON-13 | Third-party sourced data (bought lists, partner referrals) has a lawful basis that covers your purpose | "We got the list from a vendor who says it's opted in" | s.4, s.6, s.8(1) | 13 May 2027 | High |
| CON-14 | Consent is **refreshed** when purposes change | New purpose added silently to existing users | s.6(1) "specific", s.5 | 13 May 2027 | High |

## D. Withdrawal (WDR)

| ID | Test | Red flags | Law | Eff. | Sev. |
|---|---|---|---|---|---|
| WDR-01 | Withdrawal as **easy as giving** consent (same channel, similar steps) | One tap to consent, but withdraw only by email/letter/call centre; buried 5 menus deep | s.6(4) | 13 May 2027 | High |
| WDR-02 | Granular withdrawal per purpose | Only "delete my account" available | s.6(4), s.6(1) | 13 May 2027 | Medium |
| WDR-03 | Processing stops within reasonable time; processors told | No downstream propagation (CRM, ad audiences, vendors) | s.6(6) | 13 May 2027 | High |
| WDR-04 | Consequences of withdrawal explained neutrally | Confirm-shaming ("No, I don't care about my safety") | s.6(5), CCPA dark patterns | 13 May 2027 | Medium |
| WDR-05 | Erasure follows withdrawal unless law requires retention | Data kept "for analytics" after withdrawal | s.8(7) | 13 May 2027 | High |

## E. Purpose limitation and minimisation (PUR)

| ID | Test | Red flags | Law | Eff. | Sev. |
|---|---|---|---|---|---|
| PUR-01 | Each field maps to a stated purpose | Orphan fields (no stated use) | s.5, s.6(1) | 13 May 2027 | High |
| PUR-02 | Each field **necessary** for its purpose | DOB when age-band suffices; full address for a newsletter; father's name, religion, marital status for a retail account | s.6(1) | 13 May 2027 | High |
| PUR-03 | Optional fields clearly marked optional; form works without them | All fields `required`; asterisk on everything | s.6(1) "unconditional" | 13 May 2027 | Medium |
| PUR-04 | Device permissions limited to function, requested in context | Contacts, SMS, call logs, gallery, precise location at install time | s.6(1) illustration | 13 May 2027 | High–Critical |
| PUR-05 | No silent secondary use (profiling, model training, selling, ad audiences) | "We may use your data to improve our AI" with no separate consent | s.6(1) specific | 13 May 2027 | High |
| PUR-06 | Identity documents only where needed; masked where possible | Full Aadhaar number collected for delivery; PAN for a free trial | s.6(1); Aadhaar Act (overlay) | 13 May 2027 | High |
| PUR-07 | Free-text fields don't invite unnecessary data | "Tell us about yourself" on a service ticket form | BP | — | Low |
| PUR-08 | Inferred/derived data (scores, segments, voiceprints) disclosed and justified | Voice biometrics derived from call recordings without notice | s.5, s.6 | 13 May 2027 | High |

## F. Legitimate uses (LEG)

| ID | Test | Red flags | Law | Eff. | Sev. |
|---|---|---|---|---|---|
| LEG-01 | If relying on s.7, the specific clause fits the processing | Using s.7(a) for marketing; s.7(i) for non-employment data | s.7 | 13 May 2027 | High |
| LEG-02 | s.7(a) voluntary provision: user gave data for a specified purpose and hasn't objected; use stays within that purpose | Reusing a delivery phone number for promotions | s.7(a) | 13 May 2027 | High |
| LEG-03 | Over-consenting: consent asked where a legitimate use applies and withdrawal can't actually be honoured | "Consent" to statutory KYC retention that can't be withdrawn — misleading | s.7, s.6 | 13 May 2027 | Low–Medium |
| LEG-04 | Notice still given as good practice even under s.7 | — | BP | — | Advisory |

## G. Retention and erasure (RET)

| ID | Test | Red flags | Law | Eff. | Sev. |
|---|---|---|---|---|---|
| RET-01 | Defined erasure trigger per data category (purpose served / withdrawal) | "We retain data as long as necessary" with no criteria; "indefinitely" | s.8(7) | 13 May 2027 | High |
| RET-02 | Legal-retention exceptions identified and limited to that law's scope | Keeping everything 8 years "for tax" | s.8(7) proviso | 13 May 2027 | Medium |
| RET-03 | Third Schedule platforms: 3-year inactivity erasure + 48-hour warning | No inactivity deletion; no warning | s.8(8), Rule 8(1)-(2) | 13 May 2027 | High (if applicable) |
| RET-04 | Minimum 1-year retention of processing logs/traffic data, segregated and restricted | Logs deleted after 30 days; or logs reused for marketing | Rule 6, Rule 8(3) | 13 May 2027 | Medium |
| RET-05 | Processors erase on instruction; contract says so | No deletion clause with vendors | s.8(7), s.8(2) | 13 May 2027 | Medium |
| RET-06 | Backups, data lakes, analytics copies, recordings covered by erasure | Erased in app DB, kept in warehouse | s.8(7) | 13 May 2027 | Medium |
| RET-07 | Call/chat recordings have a retention period | Recordings kept forever | s.8(7) | 13 May 2027 | Medium |

## H. Children and persons with disability (CHD)

| ID | Test | Red flags | Law | Eff. | Sev. |
|---|---|---|---|---|---|
| CHD-01 | Age assurance appropriate to risk (age gate / declaration / verification) | No age question on a service attractive to under-18s; "13+" (US COPPA) logic | s.9(1), Rule 10 | 13 May 2027 | Critical |
| CHD-02 | Verifiable parental consent via Rule 10 routes | Child enters parent's email and clicks; OTP to child's phone | s.9(1), Rule 10 | 13 May 2027 | Critical |
| CHD-03 | No tracking, behavioural monitoring or targeted ads directed at children | Personalised feeds/ads for minors; analytics profiling | s.9(3) | 13 May 2027 | Critical |
| CHD-04 | No processing likely to harm a child's well-being | Public profiles, location sharing, contact with strangers, engagement loops | s.9(2) | 13 May 2027 | Critical |
| CHD-05 | Fourth Schedule exemption claimed correctly and only to the extent necessary | Edtech app claiming "educational institution" exemption for ad targeting | Rule 12 | 13 May 2027 | High |
| CHD-06 | PwD guardian consent verified (court / designated authority / local level committee) | Any family member accepted as guardian | s.9(1), Rule 11 | 13 May 2027 | High |

## I. Security (SEC)

| ID | Test | Red flags | Law | Eff. | Sev. |
|---|---|---|---|---|---|
| SEC-01 | Encryption / masking / tokenisation of personal data | Plaintext ID numbers; data in spreadsheets emailed around | s.8(5), Rule 6(a) | 13 May 2027 | Critical |
| SEC-02 | Access control (least privilege, MFA for admin) | Shared logins; everyone in support sees full records | Rule 6(b) | 13 May 2027 | High |
| SEC-03 | Logging, monitoring, review | No access logs | Rule 6(c) | 13 May 2027 | High |
| SEC-04 | Backups / continuity | — | Rule 6(d) | 13 May 2027 | Medium |
| SEC-05 | Security obligations in processor contracts | No DPA/security schedule with vendors | Rule 6(f), s.8(2) | 13 May 2027 | High |
| SEC-06 | Data in transit protected; forms over HTTPS; no personal data in URLs | Query-string emails/phones; HTTP form | Rule 6(a) | 13 May 2027 | High |

## J. Breach readiness (BRC)

| ID | Test | Red flags | Law | Eff. | Sev. |
|---|---|---|---|---|---|
| BRC-01 | Process to notify affected users without delay (content per Rule 7(1)) | No user-notification template | s.8(6), Rule 7(1) | 13 May 2027 | High |
| BRC-02 | Process to notify the Board without delay + detailed report within 72 hours | Only CERT-In process exists | s.8(6), Rule 7(2) | 13 May 2027 | High |
| BRC-03 | CERT-In 6-hour reporting aligned | — | CERT-In Directions 2022 | In force | Advisory (overlay) |
| BRC-04 | Processors must report breaches to you promptly (contract) | — | s.8(1), (6) | 13 May 2027 | Medium |

## K. Processors and sharing (PRC)

| ID | Test | Red flags | Law | Eff. | Sev. |
|---|---|---|---|---|---|
| PRC-01 | Valid contract with each processor | Free SaaS tools with personal data under click-through terms only | s.8(2) | 13 May 2027 | High |
| PRC-02 | Processor can't use data for its own purposes | Vendor ToS allows "improving our models/services" with your users' data | s.8(1)-(2) | 13 May 2027 | High |
| PRC-03 | Sharing with other Data Fiduciaries has its own lawful basis and is disclosed | Lead sharing with "partners"; dealer networks | s.4, s.6, s.11 | 13 May 2027 | High |
| PRC-04 | Can produce list of all fiduciaries/processors data was shared with (for access requests) | No data-flow map | s.11(1)(b) | 13 May 2027 | Medium |
| PRC-05 | Accuracy where data drives decisions or is shared | Stale data used for credit/eligibility decisions | s.8(3) | 13 May 2027 | Medium |

## L. Rights and grievance (RTS)

| ID | Test | Red flags | Law | Eff. | Sev. |
|---|---|---|---|---|---|
| RTS-01 | Published means to request access, correction, erasure | No self-service or request form | ss.11–12, Rule 14(1) | 13 May 2027 | High |
| RTS-02 | Published identifiers needed to make a request | Asking for excessive ID to process a request | Rule 14(1) | 13 May 2027 | Medium |
| RTS-03 | Grievance mechanism with published response period ≤ 90 days | No grievance officer; no timeline | s.8(10), s.13, Rule 14(3) | 13 May 2027 | High |
| RTS-04 | Nomination facility | Not offered | s.14, Rule 14 | 13 May 2027 | Medium |
| RTS-05 | Contact person published and included in every rights response | — | s.8(9), Rule 9 | 13 May 2027 | Medium |
| RTS-06 | Access response can list data, processing activities, recipients | — | s.11 | 13 May 2027 | Medium |

## M. Cross-border (XBT)

| ID | Test | Red flags | Law | Eff. | Sev. |
|---|---|---|---|---|---|
| XBT-01 | Destinations identified; none on a notified restricted list | — | s.16(1) | 13 May 2027 | Medium |
| XBT-02 | Sector localisation rules met (e.g. RBI payment data) | Payment data processed/stored abroad | s.16(2); RBI | In force (RBI) | High |
| XBT-03 | Rule 15 / Rule 13(4) requirements checked once specified | — | Rule 15, 13 | 13 May 2027 | Advisory |

## N. SDF (SDF) — only if notified or likely

| ID | Test | Law | Eff. | Sev. |
|---|---|---|---|---|
| SDF-01 | DPO based in India, reporting to board | s.10(2)(a) | 13 May 2027 | High |
| SDF-02 | Independent data auditor | s.10(2)(b) | 13 May 2027 | High |
| SDF-03 | DPIA + periodic data audit every 12 months; significant observations to Board | s.10(2)(c), Rule 13 | 13 May 2027 | High |
| SDF-04 | Algorithmic due diligence | Rule 13 | 13 May 2027 | High |
| SDF-05 | Localisation of specified data | Rule 13 | 13 May 2027 | High |

## O. Legacy data (LGC)

| ID | Test | Red flags | Law | Eff. | Sev. |
|---|---|---|---|---|---|
| LGC-01 | Existing users given a DPDP notice as soon as reasonably practicable | No plan to re-notify existing base | s.5(2) | 13 May 2027 | High |
| LGC-02 | Legacy data with no traceable consent identified and either re-consented, mapped to s.7, or erased | "We've always had this list" | s.4, s.8(7) | 13 May 2027 | High |

## P. Consent UX and dark patterns (UX) — see `07-dark-patterns-ux.md`

| ID | Test | Law | Eff. | Sev. |
|---|---|---|---|---|
| UX-01 | "Accept" and "Reject"/"Manage" equally prominent | s.6(1) free; CCPA interface interference | 13 May 2027 / In force (CCPA) | High |
| UX-02 | No confirm-shaming, nagging, false urgency around consent | CCPA Dark Patterns Guidelines 2023 | In force | Medium |
| UX-03 | No forced action (unrelated data or sign-up to proceed) | s.6(1) unconditional; CCPA forced action | In force (CCPA) | High |
| UX-04 | No trick questions (double negatives on opt-outs) | s.6(1) unambiguous; CCPA trick question | In force (CCPA) | High |
| UX-05 | Consent not hidden behind "Continue" CTAs mixing actions | s.6(1) | 13 May 2027 | High |

## Q. Adjacent-law flags (ADJ) — see `08-sector-overlays.md`
Flag as Advisory with source: SPDI Rules (until 13 May 2027), CERT-In Directions, RBI (payments,
digital lending, KYC), TRAI TCCCPR (commercial calls/SMS), Aadhaar Act, health (ABDM,
telemedicine), IRDAI, SEBI, CCPA dark patterns, Consumer Protection (E-Commerce) Rules, IT
Rules 2021, labour codes for HR data.
