# Example 4 — Leave portal for factory workers

## Input (user described)
Mobile web portal for blue-collar employees. Login with employee ID + mobile OTP. Fields:
leave type, dates, reason (free text), medical certificate upload for sick leave >2 days.
Manager approves in-app. HR analytics team wants to use leave data to predict attrition.

## Expected review (abridged)
**Verdict: 🟠 Needs work**

- **Aligned — LEG-01 (s.7(i)):** leave administration is an employment purpose, so no consent
  checkbox is needed. Don't add "I consent" boxes the employee can't meaningfully refuse; give
  a clear notice instead.
- **High — PUR-05 / CON-14:** attrition prediction is arguably beyond "employment purposes"
  under s.7(i) and has individual impact. Options: use aggregated or anonymised data only; or
  run it as a separately justified purpose with notice, plus a DPIA-style review (best
  practice). Don't make individual decisions from it without transparency.
- **Medium — PUR-02/07:** the free-text "reason" invites health details. Replace it with leave
  categories. Let managers see "medical leave" but not the certificate. Restrict certificate
  access to HR.
- **Medium — SEC-02:** role-based access, so a manager sees only their own team.
- **Medium — NOT-08:** this workforce is likely to prefer Hindi or a regional language. Offer
  language choice, and an audio or assisted option at kiosks.
- **Medium — RET-01:** set retention for certificates (e.g. delete after the leave is settled
  plus an audit period) separately from statutory leave registers (labour codes/state rules —
  verify).
- **Advisory:** the OTP SMS vendor is a processor and needs a contract.
