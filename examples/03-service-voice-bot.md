# Example 3 — Appliance service voice bot (inbound + outbound)

## Input (user described)
Inbound voice bot books service tickets: asks name, registered mobile, address, product serial
number, problem description. Opening line: "This call may be recorded for quality and training
purposes." After booking, the bot says: "Great news! You're eligible for an extended warranty
at 20% off — shall I add it?" Transcripts go to a US-hosted speech/LLM vendor. Outbound bot
calls customers whose warranty expires in 30 days to sell AMC plans.

## Expected review (abridged)
**Verdict: 🟠 Needs work**

- **Aligned / basis — LEG-02 (s.7(a)):** for a ticket the customer initiated, using their
  name, mobile, address, serial number and problem description to book and update the service
  can rest on voluntary provision for that purpose. A consent prompt isn't required for this
  part, but a notice is still needed for transparency (and recommended).
- **High — NOT-15 / NOT-04:** "quality and training purposes" is vague, and "training" could
  mean AI model training. Say what recordings and transcripts are used for and how long they
  are kept. If they're used to train models, ask separately.
- **High — CON-02 / PUR-05:** the in-call upsell is a separate marketing purpose bolted onto a
  service call. Ask first: "Would you like to hear about extended-warranty plans?" Pitch only on
  a yes, and record the consent.
- **High — Outbound AMC calls:** promotional calls need consent for marketing (s.6) plus TRAI
  TCCCPR compliance (DND scrub or recorded digital consent via DLT; correct number series —
  verify). Using purchase data collected for warranty to cold-sell AMC is a new purpose; s.7(a)
  doesn't cover it.
- **Medium — PRC-01/02, XBT-01:** the US vendor is a processor. You need a contract that bars
  training on your data, sets retention and deletion, and includes security and breach
  clauses. Disclose processing outside India. No country is currently restricted under s.16.
- **Medium — RET-07:** set a retention period for recordings and transcripts (e.g. 90 days),
  with longer retention only for disputes.
- **Medium — NOT-08:** offer Hindi and regional languages in the IVR, and send an SMS with the
  notice link.
- **Medium — PUR-08:** if voiceprints or speaker identification are derived, disclose this and
  get consent.
- **Advisory — BRC/CERT-In:** the vendor's incident timelines must support CERT-In's 6-hour
  reporting and the Board's 72-hour detailed report.

Rewritten opening and upsell lines: see `templates/consent-notice-template.md` §D.
