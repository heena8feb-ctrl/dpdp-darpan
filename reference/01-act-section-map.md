# DPDP Act, 2023 — section map for reviewers

Paraphrased for review work. Quote the official text (India Code) when precision matters.
Effective dates: see `00-regulatory-status.md`. Most of Chapters II–IV apply from 13 May 2027.

## Key definitions (s.2)
- **Personal data** — any data about an individual who is identifiable by or in relation to it.
- **Digital personal data** — personal data in digital form.
- **Data Principal** — the individual the data relates to. For a **child** (under 18), includes
  the parent or lawful guardian. For a **person with disability** who has a lawful guardian,
  includes the guardian acting on their behalf.
- **Data Fiduciary** — whoever, alone or with others, decides the purpose and means of processing.
- **Data Processor** — processes personal data on behalf of a Data Fiduciary.
- **Significant Data Fiduciary (SDF)** — a Data Fiduciary notified by the Government under s.10.
- **Consent Manager** — a person registered with the Board who acts as a single point of contact
  for Data Principals to give, manage, review and withdraw consent through an accessible,
  transparent, interoperable platform.
- **Processing** — any wholly or partly automated operation on digital personal data, including
  collection, recording, organisation, structuring, storage, adaptation, retrieval, use,
  alignment or combination, indexing, sharing, disclosure, restriction, erasure or destruction.
- **Personal data breach** — unauthorised processing, or accidental disclosure, acquisition,
  sharing, use, alteration, destruction or loss of access, that compromises confidentiality,
  integrity or availability.
- **Child** — under 18.
- **Specified purpose** — the purpose in the notice given to the Data Principal.
- **Board** — Data Protection Board of India.

Note: DPDP has **no separate "sensitive personal data" category** (unlike the SPDI Rules or
GDPR). Sensitivity matters through children's data, SDF factors, security safeguards and sector
law.

## Chapter I — Preliminary
- **s.3 Application.** Applies to processing of digital personal data within India — whether
  collected digitally or collected offline and then digitised — and to processing outside India
  if it is connected with offering goods or services to Data Principals in India.
  **Does not apply** to: processing by an individual for a personal or domestic purpose; personal
  data made publicly available by the Data Principal herself or by someone under a legal
  obligation to publish it. (The public-data carve-out is narrow — data published by third
  parties, or data whose public status is unclear, isn't covered. Verify before relying on it.)

## Chapter II — Obligations of Data Fiduciary
- **s.4 Grounds.** Process only for a lawful purpose, with **consent** (s.6) or for a
  **legitimate use** (s.7).
- **s.5 Notice.**
  - (1) Every consent request must be accompanied or preceded by a notice telling the Data
    Principal: the personal data and the purpose; how to exercise rights under s.6(4)
    (withdrawal) and s.13 (grievance); how to complain to the Board.
  - (2) Where consent was given **before commencement**, give such a notice as soon as reasonably
    practicable; processing may continue until consent is withdrawn.
  - (3) The Data Principal must be able to access the notice in **English or any language in the
    Eighth Schedule** to the Constitution (22 languages).
  - Rule 3 adds format and content detail — see `02-rules-2025-map.md`.
- **s.6 Consent.**
  - (1) Consent must be **free, specific, informed, unconditional and unambiguous**, given by a
    **clear affirmative action**, signifying agreement to processing for the **specified purpose**
    and **limited to the personal data necessary** for that purpose. The Act's illustration: a
    telemedicine app asking consent for personal data **and** access to the phone's contact
    list — consent for the contact list is invalid because it isn't necessary.
  - (2) Any part of a consent that infringes the Act, its Rules or any other law is invalid to
    that extent. Illustration: consenting not to complain to the Board is invalid.
  - (3) Every consent request must be in **clear and plain language**, available in English or an
    Eighth Schedule language, and give contact details of a DPO (where applicable) or another
    authorised person who can answer questions.
  - (4) The Data Principal can **withdraw consent at any time**, with **ease comparable to the
    ease with which it was given**.
  - (5) Consequences of withdrawal are borne by the Data Principal; withdrawal doesn't affect the
    legality of processing before it.
  - (6) On withdrawal, the Data Fiduciary must, within a reasonable time, stop processing (and
    have processors stop) unless processing without consent is required or authorised by law.
  - (7)–(9) Consent may be given, managed, reviewed or withdrawn through a **Consent Manager**,
    who is accountable to the Data Principal and must be registered with the Board.
  - (10) Where consent is the basis, the **Data Fiduciary bears the burden of proving** a notice
    was given and consent was obtained → keep consent records.
- **s.7 Certain legitimate uses** — no consent needed. See `04-legitimate-uses-exemptions.md`.
- **s.8 General obligations.**
  - (1) The Data Fiduciary is responsible for compliance, including for processing by its
    processors, regardless of any contract or the Data Principal's own failure.
  - (2) Engage or involve a processor **only under a valid contract**.
  - (3) Ensure **completeness, accuracy and consistency** where data is likely to be used to make
    a decision affecting the Data Principal or disclosed to another Data Fiduciary.
  - (4) Implement appropriate **technical and organisational measures**.
  - (5) Protect data with **reasonable security safeguards** to prevent breach, including by
    processors. (Rule 6.)
  - (6) On a personal data breach, **intimate the Board and each affected Data Principal**.
    (Rule 7.)
  - (7) **Erase** personal data (and have processors erase it) when consent is withdrawn or as soon
    as it is reasonable to assume the specified purpose is no longer served — whichever is
    earlier — unless retention is necessary for legal compliance.
  - (8) The purpose is **deemed no longer served** if the Data Principal doesn't approach the Data
    Fiduciary for the purpose or exercise rights for a prescribed period. (Rule 8, Third Schedule.)
  - (9) **Publish business contact information** of a DPO (if applicable) or a person who can
    answer questions about processing. (Rule 9.)
  - (10) Establish an **effective grievance redressal mechanism**. (Rule 14.)
- **s.9 Children and persons with disability.**
  - (1) Obtain **verifiable consent of the parent** before processing a child's data, and of the
    **lawful guardian** before processing data of a person with disability. (Rules 10, 11.)
  - (2) Don't process in a way likely to cause any **detrimental effect on a child's well-being**.
  - (3) Don't undertake **tracking or behavioural monitoring** of children or **targeted
    advertising directed at children**.
  - (4) Classes of Data Fiduciaries or purposes may be exempted from s.9(1) and s.9(3) as
    prescribed (Rule 12, Fourth Schedule).
  - (5) If the Government is satisfied a Data Fiduciary processes children's data in a
    verifiably safe manner, it may notify an age above which that Data Fiduciary is exempt from
    s.9(1)/(3). No such notification as at the snapshot (verify).
- **s.10 Significant Data Fiduciaries.**
  - Notified based on factors such as volume and sensitivity of data, risk to Data Principals'
    rights, impact on sovereignty and integrity of India, risk to electoral democracy, security
    of the State, public order.
  - Must: appoint a **DPO based in India**, responsible to the board of directors, as the point of
    contact for grievances; appoint an **independent data auditor**; carry out **Data Protection
    Impact Assessments** and **periodic data audits**; other measures as prescribed (Rule 13).

## Chapter III — Rights and duties of Data Principal
- **s.11 Right to access information** — a summary of personal data being processed and the
  processing activities; identities of all other Data Fiduciaries and processors it was shared
  with, with a description of what was shared; other prescribed information. (Limited exception
  for sharing with authorised investigative bodies.)
- **s.12 Right to correction and erasure** — correct, complete, update; erase unless retention is
  necessary for the specified purpose or legal compliance.
- **s.13 Right of grievance redressal** — readily available means; respond within the prescribed
  period (Rule 14: max 90 days). The Data Principal must exhaust this before approaching the
  Board.
- **s.14 Right to nominate** — someone to exercise rights on death or incapacity.
- **s.15 Duties of Data Principal** — comply with law; don't impersonate; don't suppress material
  information when providing data for identity documents etc.; don't file false or frivolous
  grievances; give only verifiably authentic information when seeking correction. Penalty up to
  ₹10,000.

## Chapter IV — Special provisions
- **s.16 Cross-border transfer** — allowed except to countries the Government restricts by
  notification (negative list; none notified as at the snapshot). Any other law giving a higher
  degree of protection or restriction (e.g. RBI payment-data localisation) continues to apply.
- **s.17 Exemptions** — see `04-legitimate-uses-exemptions.md`.

## Chapters V–VIII — Board, appeals, penalties
- **ss.18–26** Board constitution. **s.27** powers (inquiries, directions). **s.28** procedure,
  digital office. **s.29** appeal to TDSAT (Appellate Tribunal) within 60 days. **s.31**
  mediation. **s.32** voluntary undertaking. **s.33** penalties per the Schedule, considering
  nature, gravity, duration, type and nature of data, repetition, gain or loss avoided,
  mitigation, proportionality. **s.34** penalties go to the Consolidated Fund.
- **s.37** Government may order blocking of a Data Fiduciary's platform after repeated
  penalties, on Board reference.
- **s.38** Act is in addition to other laws; prevails over them on conflict.
- **s.44** Amendments: (2) omits **IT Act s.43A** (from 13 May 2027); (3) amends **RTI Act
  s.8(1)(j)** (in force from 13 Nov 2025).

## The Schedule — maximum penalties (per instance; "up to")
| # | Breach of | Up to |
|---|---|---|
| 1 | Reasonable security safeguards (s.8(5)) | ₹250 crore |
| 2 | Breach intimation to Board/Data Principals (s.8(6)) | ₹200 crore |
| 3 | Additional obligations for children (s.9) | ₹200 crore |
| 4 | SDF additional obligations (s.10) | ₹150 crore |
| 5 | Duties of Data Principal (s.15) | ₹10,000 |
| 6 | Voluntary undertaking accepted by Board (s.32) | Up to the amount applicable to the breach |
| 7 | Any other provision of the Act or Rules | ₹50 crore |

Use these only to explain relative weight. Never predict an actual fine.
