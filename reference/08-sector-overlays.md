# Sector and adjacent-law overlays

DPDP sits on top of other laws. s.16(2): any law providing a higher degree of protection or
restriction on cross-border transfer continues to apply. s.38: DPDP is in addition to other
laws and prevails on conflict. Flag these as **Advisory** with the source, and tell the user to
check the regulator's current text — these change often. Don't present them as DPDP findings.

## Cross-cutting
| Law / direction | What to flag | Status |
|---|---|---|
| **IT Act s.43A + SPDI Rules, 2011** | Sensitive personal data (passwords, financial info, health, biometrics, sexual orientation, medical records): written consent, privacy policy, purpose limitation, reasonable security (e.g. IS/ISO/IEC 27001 or approved code) | In force until s.44(2) DPDP commences (13 May 2027) — verify |
| **CERT-In Directions (28 Apr 2022, under IT Act s.70B)** | Report specified cyber incidents to CERT-In within **6 hours** of noticing; keep ICT logs for **180 days within India**; sync clocks to NTP; VPN/cloud/VPS providers keep subscriber data for 5 years | In force |
| **IT (Intermediary Guidelines and Digital Media Ethics Code) Rules, 2021** | Intermediaries: grievance officer, user-data retention after account deletion (180 days for investigation), privacy policy | In force |
| **Consumer Protection Act 2019 + CCPA Dark Patterns Guidelines 2023** | 13 dark patterns (see `07-dark-patterns-ux.md`) | In force |
| **Consumer Protection (E-Commerce) Rules, 2020** | E-commerce disclosures, grievance officer, no manipulation | In force |

## Financial services
| Law / direction | What to flag |
|---|---|
| **RBI — Storage of Payment System Data (2018)** | Payment system data stored only in India (processing abroad allowed with data returned within the specified window — verify). Overrides DPDP's permissive cross-border default. |
| **RBI Digital Lending Directions, 2025** (consolidating the 2022 guidelines) | Lenders/LSPs/DLAs must **not access phone resources like files and media, contact list, call logs, telephony functions**; one-time access to camera, microphone, location only for onboarding/KYC with explicit consent; data collection need-based with prior explicit consent; borrower can deny, restrict, revoke and ask for deletion; data stored in India; disclose data-sharing with third parties. Verify current text. |
| **RBI KYC Master Direction + PMLA** | KYC record retention (5 years after relationship ends); permitted KYC methods (V-CIP, DigiLocker, offline Aadhaar) |
| **Credit Information Companies (Regulation) Act, 2005** | Credit information sharing with CICs |
| **SEBI — Cybersecurity and Cyber Resilience Framework (CSCRF), 2024** | Regulated entities' security and data controls |
| **IRDAI Information and Cyber Security Guidelines, 2023** (and later updates) | Insurers and intermediaries; health and policyholder data; data localisation of records in India (verify) |
| Account Aggregator (RBI NBFC-AA framework) | Consent artefacts for financial data sharing — an established consent-manager model |

## Identity
| Law | What to flag |
|---|---|
| **Aadhaar Act, 2016** (and regulations) | Don't collect/store the full Aadhaar number unless legally permitted; prefer **masked Aadhaar**, offline e-KYC XML/QR, or DigiLocker; authentication only by permitted entities; never display full number; don't make Aadhaar mandatory where the law doesn't. |
| PAN / passport / voter ID | Collect only when legally or functionally needed; mask in UI; encrypt at rest. |

## Health
| Source | What to flag |
|---|---|
| ABDM **Health Data Management Policy** (NHA) | Consent-based health data exchange via ABHA; consent artefacts |
| **Telemedicine Practice Guidelines, 2020** | Patient consent, record-keeping by practitioners |
| Clinical Establishments Act / state rules; Mental Healthcare Act, 2017 (confidentiality) | Medical records confidentiality and retention |
| Note | DPDP s.7(f)-(g) covers emergencies/epidemics; ordinary health apps still need consent. |

## Telecom, marketing calls and messages
| Source | What to flag |
|---|---|
| **TRAI Telecom Commercial Communications Customer Preference Regulations (TCCCPR), 2018** (and amendments) | Promotional calls/SMS only to customers who haven't opted out via DND / or with recorded **digital consent** via registered consent templates on DLT; registered headers and templates; promotional vs transactional/service classification; 140/160-series numbering (verify). Highly relevant to **outbound sales calls and voice bots** (e.g. AMC/extended-warranty upsell). |
| **Telecommunications Act, 2023** | Consent for specified messages; user protection measures (rules evolving — verify) |
| WhatsApp Business policy (platform rule, not law) | Opt-in required before business-initiated messages |

## Employment / HR
| Source | What to flag |
|---|---|
| DPDP **s.7(i)** | Employment purposes don't need consent — but scope it properly (see `04`) |
| Labour codes (Code on Wages, IR Code, Social Security Code, OSH Code — in force from 21 Nov 2025) and state rules | Statutory registers and retention; verify current state rules |
| Background verification | Candidate consent; criminal-record checks are sensitive — limit and justify |
| Employee monitoring | Proportionate to protecting the employer; tell employees |

## Education
| Source | What to flag |
|---|---|
| DPDP s.9 + Fourth Schedule | Children's data; educational-institution exemption is purpose-limited |
| UGC / AICTE / state rules on student records | Record retention |

## Gaming
| Source | What to flag |
|---|---|
| **Promotion and Regulation of Online Gaming Act, 2025** (and rules) | Real-money gaming ban; registration of e-sports/social games; verify current position |
| DPDP Third Schedule | Online gaming intermediaries ≥ 50 lakh users: 3-year inactivity erasure |

## AI and automated processing
- No AI-specific Indian statute as at the snapshot. MeitY has issued AI governance guidelines and
  advisories (verify latest); IT Rules amendments on synthetically generated content/deepfake
  labelling may apply to generative features (verify).
- DPDP still applies to personal data in prompts, training sets, outputs and logs.
- SDFs: Rule 13 algorithmic due diligence.
