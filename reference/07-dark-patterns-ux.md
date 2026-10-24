# Consent UX and dark patterns

Two sources of rules:
1. **DPDP s.6(1)** — consent must be free, specific, informed, unconditional, unambiguous, by
   clear affirmative action (from 13 May 2027).
2. **Guidelines for Prevention and Regulation of Dark Patterns, 2023** — issued by the
   **Central Consumer Protection Authority (CCPA)** under the Consumer Protection Act, 2019
   (notified 30 Nov 2023). **In force now** for platforms offering goods/services in India.
   They list 13 specified dark patterns. The CCPA has since pushed e-commerce platforms to
   self-audit for dark patterns (verify latest advisories).

## The 13 CCPA dark patterns — and how they show up in consent flows
| Pattern | Consent/data example |
|---|---|
| False urgency | "Accept now or lose your discount in 30 seconds" |
| Basket sneaking | Extra data-sharing add-on pre-selected at checkout |
| Confirm shaming | "No thanks, I don't want to stay safe" on a decline button |
| Forced action | Must share contacts / sign up for newsletter / download app to proceed |
| Subscription trap | Consent to recurring marketing easy to give, very hard to cancel |
| Interface interference | Big coloured "Accept all", tiny grey "Manage" link; reject button styled as disabled |
| Bait and switch | Asked for email "to send your receipt", then used for marketing |
| Drip pricing | (Pricing — not usually consent-related) |
| Disguised advertisement | Ad dressed as a privacy setting or survey |
| Nagging | Repeated pop-ups asking to enable tracking after a refusal |
| Trick question | "Untick this box if you don't want to not receive offers" |
| SaaS billing | (Billing — not usually consent-related) |
| Rogue malware | (Malware — out of scope here; flag if spotted) |

## Consent UX rules of thumb (to recommend)
- **Equal choice:** "Accept" and "Reject" (or "Only necessary") at the same level, same size,
  same visual weight, same number of clicks.
- **Unticked by default.** Every optional purpose has its own unticked checkbox or toggle.
- **Separate the action from the consent.** "Create account" ≠ "I agree to marketing". Use a
  separate tick for each optional purpose; the main button only completes the service.
- **Just-in-time permissions:** ask for camera/location/contacts when the feature needs it, with
  a one-line reason; the feature still works partially if declined where possible.
- **Layered notice:** short standalone notice at the point of collection (Rule 3 content), with a
  link to the full privacy policy for detail.
- **Remember choices;** don't re-ask after a refusal for a reasonable period.
- **Withdrawal mirror:** wherever a consent was given (banner, settings, checkbox), withdrawal is
  available in the same place with the same effort.
- **Language selector** visible near the notice (English + Eighth Schedule languages).
- **Accessible:** readable contrast, screen-reader labels on checkboxes, no image-only text.

## Cookie / tracker banners
- No non-essential cookies, pixels, SDKs or session replay before consent.
- "Strictly necessary" really means necessary for the service the user asked for (session,
  security, load balancing, cart) — not analytics or ads.
- Granular categories (analytics, personalisation, advertising) with descriptions.
- "Reject all" on the first layer.
- A persistent "Privacy settings" link to change choices.
- Consent recorded (s.6(10)).
