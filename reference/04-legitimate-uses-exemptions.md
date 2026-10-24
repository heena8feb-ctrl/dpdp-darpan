# When consent is NOT the basis — legitimate uses (s.7) and exemptions (s.17)

Check this before flagging "missing consent". DPDP has **no general "legitimate interest"**
ground (that's GDPR). If processing isn't covered by a specific s.7 clause or an exemption, it
needs consent.

## s.7 — Certain legitimate uses (from 13 May 2027)
A Data Fiduciary may process personal data without consent:

| Clause | Use | Review notes |
|---|---|---|
| 7(a) | For the **specified purpose for which the Data Principal voluntarily provided** the data, where she hasn't indicated she doesn't consent to its use | Classic example: a buyer gives a phone number to receive a purchase receipt or delivery update. Covers that use only — **not** marketing, profiling or sharing for other purposes. The purpose must be clear from context. |
| 7(b) | By the **State or its instrumentalities** to provide a subsidy, benefit, service, certificate, licence or permit, where the person previously consented to such a benefit or the data is in a government database | Government/PSU flows. Rule 5 + Second Schedule standards. |
| 7(c) | By the **State** performing a function under law, or in the interest of sovereignty, integrity or security of India | Government only. |
| 7(d) | To fulfil a **legal obligation to disclose information to the State** or its instrumentalities | E.g. statutory reporting. |
| 7(e) | To comply with a **judgment, decree or order** of a court/tribunal in India, or under foreign law relating to contractual/civil claims | Litigation holds, court orders. |
| 7(f) | To respond to a **medical emergency** involving threat to life or immediate threat to health | Narrow, real emergencies. |
| 7(g) | To provide **medical treatment or health services during an epidemic**, outbreak or other threat to public health | |
| 7(h) | To ensure **safety of, or provide assistance or services to, individuals during a disaster** or breakdown of public order | |
| 7(i) | For the purposes of **employment** or those related to safeguarding the employer from loss or liability — e.g. preventing corporate espionage, maintaining confidentiality of trade secrets, IP or classified information, or providing any service or benefit sought by an employee | Covers core HR administration of **employees**: payroll, attendance, leave, benefits the employee asks for, security monitoring proportionate to protecting the employer. **Watch for:** candidates/applicants (not yet employees — generally need consent or 7(a)); family members' data (nominees, dependants — consider 7(a)/consent); intrusive monitoring beyond what protects the employer; reuse of HR data for unrelated purposes (e.g. marketing, AI training) — needs another basis. |

### Patterns
- **Necessary-for-service data** often fits 7(a) if the user hands it over for that service and
  the purpose is obvious. Many product teams still collect consent for clarity — fine, but don't
  make the service conditional on consent to *additional* purposes.
- **Statutory retention** (tax, KYC, labour) isn't consent-based; erasure is deferred by the
  s.8(7) "required by law" exception — don't pretend consent can be withdrawn for it.
- **A notice is still good practice** under s.7 so users know what happens (and supports
  transparency for access requests).

## s.17 — Exemptions
### s.17(1) — Chapter II (except s.8(1) and (5)), Chapter III and s.16 don't apply where processing is:
- (a) necessary for **enforcing any legal right or claim**;
- (b) by a **court, tribunal or body** with judicial/quasi-judicial/regulatory/supervisory functions,
  where necessary for those functions;
- (c) in the interest of **prevention, detection, investigation or prosecution of offences**;
- (d) of **non-residents' personal data** processed in India under a contract with a person
  outside India (outsourcing/BPO-style processing);
- (e) necessary for an approved **scheme of compromise, arrangement, merger, amalgamation,
  reconstruction, division or transfer** of undertakings;
- (f) for ascertaining **financial information and assets of a person who has defaulted** on a
  loan or advance from a financial institution, consistent with other law on information sharing.
Note: security safeguards (s.8(5)) and overall responsibility (s.8(1)) still apply.

### s.17(2) — the Act (wholly or partly) doesn't apply to:
- (a) processing by notified **State instrumentalities** for sovereignty, security, public order etc.;
- (b) processing for **research, archiving or statistical purposes**, if not used to make any
  decision specific to a Data Principal and carried out per prescribed standards (Rule 16 +
  Second Schedule).

### s.17(3) — startups
The Government **may** notify classes of Data Fiduciaries, including **startups**, exempt from
s.5, s.8(3), s.8(7), s.10 and s.11. **No such notification has been issued as at the snapshot.**
Never tell a user they're exempt because they're a startup or DPIIT-recognised.

### s.17(4) — State
For the State and its instrumentalities, s.8(7) and s.12(3) don't apply, and s.17(2)(a)
instrumentalities have wider exemptions (verify).

### s.17(5) — Government may, within five years of commencement, declare that any provision won't
apply to specified Data Fiduciaries for a period (verify).

## Quick decision tree
1. Is it the user's own data voluntarily given for a clear, specific purpose, used only for that? → s.7(a) possible.
2. Is it employee data used for employment administration or protecting the employer? → s.7(i) possible.
3. Is there a statutory duty to disclose/retain? → s.7(d) or s.8(7) proviso.
4. Emergency, epidemic, disaster? → s.7(f)–(h).
5. Legal claim, court, crime prevention, outsourced non-resident data, M&A, defaulter info? → s.17(1).
6. Research/statistics with no individual decisions, per standards? → s.17(2)(b).
7. Otherwise → **consent** with full notice.
