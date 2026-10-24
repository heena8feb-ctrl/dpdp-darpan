# Playbooks by input type

Use the matching playbook to know where to look. Always still run the master checklist.

## 1. Web or app form (signup, lead, contact, checkout, warranty registration)
Look at: every field and its `required` state; default checkbox states; the CTA label; text
around the CTA; links to policy/terms; hidden fields (UTM, device ID, referrer); what fires on
page load (pixels, chat widgets, session replay); success/thank-you page (upsells, more data).
Typical gaps: bundled consent in the CTA ("By clicking Submit you agree to T&C, privacy policy
and receive offers"); marketing pre-ticked; DOB/gender/address not needed; phone number reused
for WhatsApp promotions; no withdrawal route; no language option.
Key checks: NOT-01–10, CON-01–04, CON-09, PUR-01–03, UX-01–05, RET-01.

## 2. Mobile app onboarding and permissions
Look at: OS permission prompts and their timing; in-app pre-permission screens; what happens if
denied; SDK list (analytics, ads, attribution, crash, session replay); account creation;
notification opt-in; background location.
Typical gaps: contacts/SMS/call-log/gallery access unrelated to function; all permissions at
first launch; app blocks use if declined; third-party SDKs collect device IDs before consent.
Key checks: PUR-04, CON-03, CON-09, CHD-01 (if app store rating/audience suggests minors),
XBT (SDK vendors abroad), sector: RBI digital lending if lending.

## 3. Cookie / tracker banner
See `07-dark-patterns-ux.md` → Cookie banners. Key checks: CON-01, CON-02, CON-09, UX-01,
WDR-01, CON-10.

## 4. Privacy notice / policy document
Check Rule 3 elements are present in a **standalone** notice at collection (a policy alone isn't
enough). Check rights section (access, correction, erasure, nomination, grievance with ≤90-day
period), contact person/DPO, Board complaint line, retention per category, recipients,
cross-border, children's section, language availability, version/date, no rights waivers.
Flag GDPR/US-copied language that doesn't fit DPDP: "legitimate interests", "data controller",
"sell/share under CCPA", "age 13", "supervisory authority".
Key checks: NOT-*, RTS-*, RET-01, CON-07, SCOPE-06.

## 5. Consent text alone (a checkbox or a paragraph)
Rewrite-first review. Check: affirmative action; one purpose per checkbox; itemised data and
purpose (or a link to a standalone notice that has them); withdrawal route; plain language.
Return 2–3 rewrite options (short / standard / with Hindi line).

## 6. Voice bot, IVR or call-centre script
Look at: the opening line (identity of caller/company, purpose, recording disclosure, AI
disclosure); when data is first captured (name, phone, address, serial number, payment);
whether a notice is given audibly before capture; how consent for anything beyond the service
request (e.g. sales offers, recording for training) is asked; how the caller can refuse or
withdraw ("say 'stop'"); whether an SMS/WhatsApp/email copy of the notice is sent; language
choice (IVR menu); recording and transcript retention; voiceprint/biometrics; vendor (voice AI
platform, telephony, LLM) roles and locations; outbound calls: DND/TCCCPR status, consent
record for promotional calls.
Typical gaps: recording starts before disclosure; "this call may be recorded for quality and
training purposes" used as blanket consent; transcripts sent to an offshore LLM vendor
undisclosed; upsell pitched on a service call without consent for marketing; no retention for
recordings.
Note: a service request the customer initiated (new ticket, status check) can rest on s.7(a)
for that purpose; **outbound sales offers** (AMC, extended warranty) are a **separate purpose**
needing consent (and TRAI compliance).
Key checks: NOT-15, NOT-08, CON-02, PUR-05, PUR-08, RET-07, PRC-01–02, XBT-01, ADJ (TRAI).

## 7. Chatbot or LLM feature
Look at: what users are told before typing; whether chat content is used for model training or
product improvement; vendor (LLM provider) terms — retention, training on inputs, region;
logs and transcripts retention; PII redaction before sending to the model; human review of
chats; children using the bot; outputs containing other people's personal data.
Typical gaps: "Chats may be used to improve our services" with no opt-out; vendor retains
prompts 30+ days abroad without disclosure; no redaction of card/ID numbers.
Key checks: NOT-04, PUR-05, PRC-02, XBT-01, RET-01, SEC-01, CHD-03.

## 8. HR / employee / candidate flow
Distinguish: **candidates** (pre-employment — consent or s.7(a)); **employees** (s.7(i) for
employment purposes); **dependants/nominees** (consider s.7(a)/consent; minimise); **contract
and blue-collar workers** (same rules — and language/literacy matter more: offer Hindi/regional
language and audio/assisted options).
Look at: login identifiers (employee ID, mobile OTP); what's visible to managers; health data in
leave requests (minimise — "medical leave" without diagnosis); biometrics for attendance;
monitoring tools; retention after exit; use of HR data for analytics/AI.
Key checks: LEG-01, PUR-02, PUR-08, SEC-02, RET-01, NOT-08, ADJ (labour codes).

## 9. Marketing / CRM / lead data plan
Look at: sources (website, events, partners, bought lists, social lead ads); consent evidence per
source; channels (email, SMS, WhatsApp, calls, ads custom audiences); sharing with dealers/
partners; enrichment; lookalike audiences; suppression lists; retention of cold leads.
Typical gaps: bought lists without proof of consent for your purpose; uploading customer lists
to ad platforms without consent; dealers re-using leads; no global unsubscribe.
Key checks: CON-13, PRC-03, PUR-05, WDR-03, RET-01, ADJ (TRAI, WhatsApp policy).

## 10. AI/ML training dataset or analytics plan
Look at: data sources and their original purposes; whether training is a new purpose (needs
consent or a valid exemption); s.17(2)(b) research/statistical exemption conditions (no
individual decisions, Second Schedule standards); "publicly available" scraping (s.3(c)(ii) is
narrow); anonymisation quality; memorisation/leakage risk; children's data in the corpus;
retention of training copies; vendor training on your data.
Key checks: SCOPE-03, PUR-05, CON-14, CHD-03, RET-06, PRC-02.

## 11. Offline form being digitised (paper, kiosk, event)
Digitised data is in scope (s.3). Check that the paper/kiosk form carries the notice and
separate consent ticks, a language option, and a withdrawal route that's practical for that
audience (phone/SMS/WhatsApp, not only a website). Scanning/data-entry vendors are processors.

## 12. Whole data-collection plan / PRD / data-flow diagram
Build the full inventory and a data-flow map (collection → storage → processors → sharing →
deletion). Run the entire checklist. Add a **readiness roadmap**: what must be fixed before
launch, what before 13 May 2027, and what's best practice.
