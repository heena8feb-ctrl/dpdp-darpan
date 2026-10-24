# Children (under 18) and persons with disability

Top-penalty area (up to ₹200 crore under the Schedule for s.9 breaches). From 13 May 2027.

## Who is a child
Anyone **under 18**. Not 13 (US COPPA) or 16 (GDPR default). A service with a "13+" age gate is
still processing children's data for users aged 13–17.

## Duties (s.9)
1. **Verifiable parental consent** before processing a child's personal data (s.9(1), Rule 10).
2. **No detrimental processing** — nothing likely to have a detrimental effect on a child's
   well-being (s.9(2)).
3. **No tracking, behavioural monitoring or targeted advertising directed at children** (s.9(3)).
4. Persons with disability who have a **lawful guardian**: verifiable consent of the guardian
   (s.9(1), Rule 11).

## Is the service likely to have child users?
Yes or probably if: education, gaming, social, streaming/entertainment, toys, school/coaching,
youth sports, kids' products, quiz/contest flows, influencer/creator apps, general consumer apps
without age signals. Ask, or assume "possible" and flag.

## Age assurance patterns (risk-based)
- **Low risk** (minimal data, no profiling, no public interaction): neutral age declaration
  (date of birth or "Are you 18 or older?" without hinting the "right" answer) + parental route.
- **Higher risk** (profiles, chat, UGC, location, payments, ads): stronger checks — existing
  verified account data, DigiLocker-style virtual token, payment-instrument check by an adult
  (verify acceptability) — plus default-private settings.
- Avoid age gates that tell the child what to enter, or allow instant retry after "under 18".

## Verifiable parental consent — Rule 10 routes
- Parent is already a **known adult user** of the Data Fiduciary with reliable identity/age
  details → link and confirm.
- Otherwise, verify the parent's identity and adulthood using details **voluntarily provided**
  or a **virtual token** mapped to them, issued by an entity entrusted by law or the Government
  (e.g. a Digital Locker service provider).
- The Rules' illustrations also cover a child who falsely claims to be an adult (verify details).
- ❌ Not verifiable: child types a parent's email and clicks a link; OTP to the child's own phone;
  "I confirm my parent agrees" checkbox.

## Fourth Schedule exemptions (Rule 12) — only to the extent necessary
Part A classes (illustrative — verify list): clinical/mental-health establishments and
healthcare professionals (health services); allied healthcare professionals; **educational
institutions** (educational activities, safety and tracking/monitoring for the child's safety);
**crèche/child-care** operators; **transport** providers for children of educational
institutions/crèches (tracking location for safety).
Part B purposes (illustrative — verify): exercising powers/functions under law; State
subsidies/benefits; **creating an email-only user account**; ensuring the child doesn't access
**detrimental information**; **confirming the Data Principal isn't a child**; real-time
location for safety.
Review: is the claimed exemption the actual purpose? An edtech app's **ad targeting** isn't
"educational activity".

## Persons with disability — Rule 11
Guardian must be lawful: appointed by a **court**, a **designated authority** under the Rights of
Persons with Disabilities Act, 2016, or a **local level committee** under the National Trust Act,
1999. Do due diligence on the appointment.

## Design checklist for child-facing products
- Default **private** profiles; no public discoverability.
- **No** personalised ads, behavioural profiling or engagement-optimising recommender built on
  child behaviour (s.9(3)).
- Analytics: aggregate/anonymous only; no cross-site tracking; no third-party ad SDKs.
- Location off by default unless a safety exemption applies.
- Chat/UGC: moderation and safety controls.
- Notices written for both the parent and (in simple language) the child.
- Easy parental dashboard to review, withdraw and delete.
