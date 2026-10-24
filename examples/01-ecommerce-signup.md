# Example 1 — E-commerce signup form

## Input (user pasted)
```
Create your ShopKart account
Full name*  | Mobile*  | Email*  | Date of birth*  | Gender*  | Pincode*
[✓] Keep me updated with exciting offers via SMS, email & WhatsApp
[✓] I agree to the Terms & Conditions and Privacy Policy
[ CREATE ACCOUNT ]
By signing up you agree that ShopKart and its partners may contact you.
```
Facebook and Google ad pixels load on the page.

## Expected review (abridged)

> **Regulatory status as at 24 Oct 2026:** … most duties apply from 13 May 2027 … No changes found.

**Verdict: 🔴 Significant gaps**
**Fix these first:** 1) Untick and split the marketing box. 2) Remove the "partners may contact
you" line, or turn it into a separate optional consent naming the partners. 3) Add a standalone
notice with itemised data and purposes, a withdrawal route and rights.

| ID | Sev. | Check | Law | Effective | What we saw | Why it matters | Fix |
|---|---|---|---|---|---|---|---|
| F1 | Critical | CON-01 | s.6(1) | 13 May 2027 | Marketing box pre-ticked | No clear affirmative action, so the consent is invalid | Untick by default |
| F2 | Critical | CON-02 | s.6(1) | 13 May 2027 | SMS, email and WhatsApp in one box | Not specific | One box per channel (or one marketing box with channel toggles) |
| F3 | Critical | CON-03 / UX-05 | s.6(1) | 13 May 2027 | "By signing up you agree that ShopKart and its partners may contact you" | Sign-up conditioned on partner contact; partners unnamed | Remove; add optional "☐ Share my details with [named partner] for [purpose]" |
| F4 | High | NOT-02–07 | s.5, Rule 3 | 13 May 2027 | Only a Privacy Policy link | No standalone, itemised notice; no withdrawal, rights or Board info | Add notice per template A |
| F5 | High | PUR-02/03 | s.6(1) | 13 May 2027 | DOB and gender mandatory | Not necessary to create an account | Make optional with a stated purpose, or drop. Ask "Are you 18+?" if age matters |
| F6 | High | CON-09 | s.6(1) | 13 May 2027 | Ad pixels load before any choice | Tracking before consent | Load ad pixels only after opt-in via a cookie choice |
| F7 | Medium | NOT-08 | s.5(3) | 13 May 2027 | English only | Language choice required | Add a language selector |
| F8 | Medium | CHD-01 | s.9 | 13 May 2027 | No age signal; DOB collected but not used to gate | Under-18 users possible | Use an 18+ check; route minors to parental consent or block |
| F9 | Advisory | ADJ | TRAI TCCCPR | In force | SMS/WhatsApp promotions | DLT consent template / DND rules | Register consent template; honour DND |
| F10 | Advisory | SCOPE-05 | Rule 8, Third Schedule | 13 May 2027 | E-commerce platform | If ≥2 crore users: 3-year inactivity erasure + 48-hour warning | Confirm user count |

**Rewritten controls**
```
☐ Send me offers by SMS
☐ Send me offers by email
☐ Send me offers on WhatsApp
[Create account]
```
Small print under the button: *"We use your name, mobile and pincode to create your account and
deliver orders. [How we use your data] · हिन्दी"*

Open questions: What does the Privacy Policy say about retention? Who are the "partners"? Is DOB
used anywhere?
