# Data inventory and retention schedule templates

## Data inventory
| # | Data element | Source (user / device / third party / inferred) | Mandatory? | Purpose stated to user | Basis (consent / s.7(x) / exemption) | Necessary for that purpose? | Recipients (processors / other fiduciaries) | Location (India / abroad) | Retention stated | Notes |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | Full name | User | Yes | Account creation | s.7(a) | Yes | Cloud host (processor) | India | Until account closure | — |
| 2 | Date of birth | User | Yes | "To personalise" | Consent? | ❓ Age band may suffice | — | — | Not stated | PUR-02 |

Include hidden and automatic data: device IDs, IP, cookies, SDK data, location, call recordings,
transcripts, voice features, uploaded documents, derived scores and segments.

## Retention schedule
| Data category | Trigger to start the clock | Retention period | Action at end | Longer retention required by | Owner | System(s) |
|---|---|---|---|---|---|---|
| Account profile | Account closed | 90 days | Delete | — | Product | App DB, CRM |
| Invoices | Financial-year end | 8 years | Delete | Companies Act s.128 / CGST s.36 (verify) | Finance | ERP |
| Processing logs | Date of processing | 1 year (min.) | Delete | DPDP Rule 6 / 8(3); CERT-In 180 days | IT | Log store |
| Marketing consent record | Consent withdrawn | [period needed to prove consent] | Delete | s.6(10) burden of proof | Marketing | CMP |

## Data-flow map (for plans/PRDs)
Collection point → first storage → processors (name, purpose, location) → other fiduciaries →
analytics/warehouse copies → backups → deletion route.
