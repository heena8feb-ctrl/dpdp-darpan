# Regulatory status snapshot — read first

**Status as at: 24 October 2026.** This is a snapshot. The DPDP regime is being phased in and
amended. Always run the freshness protocol below before relying on it.

## The instruments

| Instrument | Reference | Date | Status |
|---|---|---|---|
| Digital Personal Data Protection Act, 2023 | Act No. 22 of 2023 | Assent 11 Aug 2023 | Phased commencement (below) |
| Commencement notification for the Act | S.O. 843(E) | 13 Nov 2025 | Sets three phases |
| Digital Personal Data Protection Rules, 2025 | G.S.R. 846(E) | Notified 13 Nov 2025 (Gazette 13/14 Nov) | Phased commencement (below) |
| Corrigendum to the Rules | G.S.R. 892(E) | 10 Dec 2025 | Typographical fixes only, incl. commencement wording |
| DPDP (Removal of Difficulties) Order, 2026 | S.O. 5458(E) | Dated 5 Oct 2026 (Gazette reported 6 or 7 Oct) | Two wording fixes, no new duties (below) |
| Draft Rules (historical) | G.S.R. 02(E) | 3 Jan 2025 | Superseded by final Rules |

## Commencement phases

| Phase | Date | What is in force |
|---|---|---|
| 1 | **13 Nov 2025** | Act: ss.1(2), 2, 18–26 (Board), 35, 38–43, 44(1) and 44(3) (RTI Act amendment). Rules 1, 2, 17–21 (Board set-up and working). |
| 2 | **13 Nov 2026** | Act s.6(9) (consent manager registration) and related Board power; **Rule 4** + First Schedule (consent managers). |
| 3 | **13 May 2027** | Everything else: notice (s.5), consent (s.6), legitimate uses (s.7), general obligations incl. security, breach, erasure (s.8), children (s.9), SDFs (s.10), rights (ss.11–14), duties (s.15), cross-border (s.16), exemptions (s.17), penalties (s.33 and Schedule), s.44(2) (omits IT Act s.43A). Rules 3, 5–16, 22, 23. |

**Practical meaning today (Oct 2026):** most operational duties a form or app must meet —
notice, consent, withdrawal, security, breach reporting, erasure, children's data, rights — are
**not yet enforceable** and apply from **13 May 2027**. Reviews now are readiness reviews.
Building it right now is still the right call: products launched today will be live on that date,
and legacy consent will need a fresh notice (s.5(2)).

Until s.44(2) commences (13 May 2027), **IT Act s.43A and the SPDI Rules, 2011** remain the
relevant baseline for "sensitive personal data" (passwords, financial, health, biometric, sexual
orientation, medical records). Flag SPDI points as `In force (SPDI Rules – until 13 May 2027)`.
(Some commentators read the SPDI position differently — verify.)

## Pending or proposed — track, don't treat as law

- **Shortened timeline proposal.** In January 2026, MeitY reportedly proposed cutting the
  18-month window to 12 months (at least for Significant Data Fiduciaries), which would move
  the deadline to 13 Nov 2026. Comments closed 4 Feb 2026. **As of October 2026 no amending
  notification has been gazetted.** If one appears, every Phase 3 tag may shift.
- **Data Protection Board appointments.** MeitY invited applications for Chairperson and four
  Members on 6 May 2026. As of early October 2026 no appointments had been reported.
- **SDF notification.** No classes of Significant Data Fiduciary have been notified under s.10(1).
- **Startup exemption.** s.17(3) lets the Government exempt classes of startups from some
  provisions. **No such notification has been issued.** Don't tell users they're exempt.
- **Cross-border restrictions.** s.16(1) negative list: none notified. Rule 15 lets the Government
  set requirements; Rule 13(4) lets it restrict SDF transfers of specified data.
- **Board standards** for consent manager certification and other Board-issued guidance.

## What the Removal of Difficulties Order 2026 changed
1. s.9(1): "child or a person with disability" → "child or **of** a person with disability" —
   clarifies two cases: a parent consents for a child, a lawful guardian for a person with
   disability.
2. s.10(2)(c)(ii): "periodic audit" → "**periodic data audit**" for SDFs.
No change to commencement dates. The s.43 power to issue such orders lasts three years from
commencement.

## Freshness protocol
Run at the start of every review if web search is available. Send these together:
1. `DPDP Rules amendment` (and `DPDP Rules amendment [current month] [current year]`)
2. `MeitY DPDP notification [current year]`
3. `Data Protection Board of India chairperson appointed`
4. `DPDP 12 month compliance timeline notified`
5. `Significant Data Fiduciary notified DPDP`
6. Sector-specific if relevant, e.g. `RBI digital lending data [current year]`, `TRAI consent
   commercial communication [current year]`

Prefer, in order: e-Gazette / MeitY / India Code / Board → law-firm alerts → vendor blogs.
Vendor and consultancy blogs (consent-platform sellers especially) are useful leads but can
overstate urgency; confirm against an official or law-firm source.

Then:
- If you find a change, put it in the report's status banner, apply it to the effective-date tags,
  and cite the source.
- If you find nothing new, say "No changes found since the 24 Oct 2026 snapshot as of [today]".
- If you can't search, say "Couldn't check for updates; status is from the 24 Oct 2026 snapshot."
- If today is after **13 Nov 2026**: Rule 4 is in force; consent manager registration is live.
- If today is after **13 May 2027**: all Phase 3 duties are in force and penalties apply; change
  "From 13 May 2027" tags to "In force"; the SPDI Rules baseline falls away.
- If the snapshot is more than 60 days old, warn prominently.

## Official sources to send users to
- **MeitY** — meity.gov.in (Data Protection / DPDP section): the Act, Rules, FAQs, notifications.
- **e-Gazette of India** — egazette.gov.in: search G.S.R. 846(E), G.S.R. 892(E), S.O. 843(E),
  S.O. 5458(E) and anything newer.
- **India Code** — indiacode.nic.in: the Act's current consolidated text.
- **Data Protection Board of India** — its official site once operational (find it via MeitY).
- **CERT-In** — cert-in.org.in: incident-reporting directions.
- Sector regulators as relevant: rbi.org.in, trai.gov.in, irdai.gov.in, sebi.gov.in,
  abdm.gov.in / nha.gov.in, uidai.gov.in, consumeraffairs.nic.in (CCPA).

Never paste a deep URL you haven't seen in this session; name the site and what to search for.

## Disclaimer line (use in every report)
> This review reflects the DPDP Act, 2023 and DPDP Rules, 2025 as understood on [DATE] (status
> snapshot [SNAPSHOT DATE]; [update check result]). The regime is being phased in and may change.
> It is not legal advice. Verify against the current text on meity.gov.in, egazette.gov.in and
> indiacode.nic.in, and consult a qualified Indian data-protection lawyer before relying on it.
