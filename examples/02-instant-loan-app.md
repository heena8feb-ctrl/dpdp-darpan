# Example 2 — Instant-loan app onboarding

## Input (user described)
Onboarding asks for: PAN, full Aadhaar number, selfie, bank statement upload. On first launch
the app requests access to contacts, SMS, call logs, gallery and precise location; it won't
proceed if any are denied. The privacy policy says data is shared with "lending partners and
collection agencies" and "retained for 10 years". The consent screen says: "I authorise
QuickRupee to access my device data for credit assessment and recovery."

## Expected review (abridged)
**Verdict: 🔴 Significant gaps**

Key findings:
- **Critical — PUR-04 / CON-03 / CON-04 (s.6(1) and its illustration):** contacts, SMS, call
  logs and gallery aren't necessary for a loan application, and making them a condition of
  proceeding makes the consent invalid. **Sector overlay — RBI Digital Lending Directions:**
  lenders, LSPs and digital lending apps must not access files and media, the contact list or
  call logs. One-time camera, mic or location access is allowed only for onboarding/KYC, with
  explicit consent (verify the current text).
- **Critical — CON-07 / PUR-05:** using "device data for recovery" points to contacting a
  borrower's contacts. That is an unrelated purpose, and it harms third parties who never
  consented.
- **High — PUR-06 + Aadhaar overlay:** collecting the full Aadhaar number. Use masked Aadhaar
  or DigiLocker/offline e-KYC via the regulated entity's permitted KYC methods.
- **High — RET-01/02:** a blanket 10-year retention. Map it to the actual laws (e.g. KYC/PMLA:
  5 years after the relationship ends) per data category, and delete the rest.
- **High — PRC-03 / NOT-11:** "lending partners and collection agencies" aren't named.
  Disclose the lender (RE) and the LSP roles. Collection agencies are processors under a
  contract, limited to the borrower's own contact details.
- **High — NOT-02–07:** there is no standalone notice, withdrawal route or grievance period.
  RBI also requires a grievance officer for digital lending.
- **Advisory — XBT-02:** payment data and lending data must be stored in India (RBI).

Rewrite approach: at onboarding, ask only for KYC data via permitted methods. Request camera
access just in time for the selfie, with a reason. Use account-aggregator consent for bank
statements instead of uploads where available. Ask for location once, optionally, for fraud
checks.
