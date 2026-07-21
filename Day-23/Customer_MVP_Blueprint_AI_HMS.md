# Customer & MVP Blueprint
## AI-Powered Hospital Management System (HMS)

**Companion document to:** Startup Validation Report — AI-Powered HMS (July 2026)
**Purpose:** Translate that report's findings into a concrete, buildable customer and product plan.

> **Convention (carried over from the Validation Report):** **[Fact]** = grounded in the prior report's cited research. **[Carried-forward assumption]** = an assumption already flagged in the Validation Report, reused here for consistency. **[New assumption]** = an assumption introduced in *this* document that has not yet been validated — treat these as hypotheses, not conclusions.

### Assumptions inherited from the Validation Report (do not re-derive — validate or correct these first)

- **[Carried-forward assumption]** Beachhead segment: independent small-to-mid hospitals and nursing homes, roughly **20–150 beds**.
- **[Carried-forward assumption]** Beachhead geography: **India**, used illustratively because it's where pricing/regulatory data was available — not confirmed as the founder's actual target market.
- **[Fact]** Pricing benchmark: small clinics ₹2,000–8,000/month; small-to-mid hospitals ₹8,000–25,000/month.
- **[Fact]** Competitive field is crowded — 20+ direct cloud-HMS competitors identified in India alone.
- **[Carried-forward assumption]** Founder-market fit is unverified — no founder background has been provided in either document.

Everything below is built on these. **If any of these five points is wrong, most of this blueprint needs to be re-run.**

---

## 1. Executive Summary

The Validation Report concluded that the AI-HMS opportunity is real but currently under-differentiated, and recommended narrowing to one segment, one wedge, and one geography before building or fundraising. This document does the narrowing: it defines exactly who the first customers should be, what job they're hiring the product to do, what the MVP should (and should not) contain, and what to do in the next 30 days to start testing it.

**The core output of this document in one line:** Build for the owner-operated 20–100 bed private hospital, sell to the owner-doctor and admin together, ship only registration + EMR + e-prescription + OPD billing first, and validate willingness-to-pay with 3–5 real pilots before writing another line of the "AI-powered" vision.

Nothing in this document should be read as confirmed customer insight — it is a structured *hypothesis set*, built from the Validation Report's secondary research and standard B2B healthcare software patterns. Section 11 exists specifically to test these hypotheses against real people.

---

## 2. Ideal Customer Profiles (ICPs)

| Attribute | **ICP 1 — Primary: Independent Small-Mid Hospital** | **ICP 2 — Secondary: Multi-Doctor Specialty Clinic** | ICP 3 — Deprioritized: Mid-Large Hospital (100–200+ beds) |
|---|---|---|---|
| Facility type | Owner-operated private hospital / nursing home | Multi-doctor clinic or small chain (2–10 locations) | Multi-specialty hospital, often part of a group |
| Bed count / scale | 20–100 beds | No beds, or day-care only | 100+ beds |
| Current tooling | Paper registers, Excel billing, or a legacy on-premise HMS | Mix of WhatsApp, Excel, basic scheduling apps | Established HIS, often enterprise-grade |
| Primary decision-maker | Owner-doctor (often also the senior clinician) | Founding doctor(s) or a practice manager | Procurement committee, IT head, CMO |
| Sales cycle | Weeks to a few months **[New assumption]** | Weeks **[New assumption]** | 6–18 months, RFP-driven **[Carried-forward assumption]** |
| Budget sensitivity | High — will compare against ₹10,000/year competitors | Very high — smallest facilities | Lower sensitivity, higher expectations |
| Why they're the right MVP target | Single decision-maker, real pain, fast to say yes or no, large addressable population (~40,000 such facilities in India per the Validation Report) | Good second wedge; more digitally comfortable, useful for telemedicine/patient-app testing later | Long sales cycles and entrenched incumbents make this a poor *first* target — revisit post-PMF |

**[New assumption]** ICP 1 is the recommended primary beachhead because it combines a fast, single-owner sales cycle with a real (not theoretical) budget line. This should be the first thing tested in Section 11 — it is a hypothesis, not a confirmed finding.

---

## 3. Buyer Personas

These are **composite personas synthesized from industry research patterns**, not from primary interviews with real customers. Treat them as a starting hypothesis for Section 11, and expect them to be wrong in some details.

### Persona A — "Dr. Owner-Administrator" (Economic Buyer, ICP 1)
- **Role:** Owns and often actively practices at the hospital; makes the final purchase call.
- **Goals:** Protect margins, reduce billing leakage, avoid staff overload, stay compliant with government scheme requirements (e.g., ABDM empanelment).
- **Frustrations:** Doesn't have time to evaluate software deeply; burned before by vendors overselling and underdelivering; worried about downtime disrupting patient care.
- **Tech comfort:** Moderate — comfortable with WhatsApp and basic apps, not necessarily complex dashboards.
- **What they care about most:** Price predictability, minimal disruption during switch-over, a trusted local reference (another hospital owner who uses it).
- **Likely objections:** "Why should I trust a new vendor over [incumbent] who's cheaper?" / "What happens if you shut down in a year?"

### Persona B — "Hospital Operations Manager" (Champion / Influencer)
- **Role:** Non-clinical administrator who manages day-to-day operations and often evaluates vendors on the owner's behalf.
- **Goals:** Reduce administrative chaos, make reporting to the owner easier, minimize staff complaints.
- **Frustrations:** Stuck reconciling paper and spreadsheet data manually; blamed when billing errors surface.
- **Tech comfort:** Higher than the owner-doctor; often the one who actually runs demos.
- **What they care about most:** Ease of staff training, quality of implementation support, responsiveness when something breaks.

### Persona C — "Treating Doctor / Consultant" (Clinical User, Veto Power)
- **Role:** Uses the EMR and any AI assistance directly during consultations.
- **Goals:** See patients quickly, avoid clinical errors, not be slowed down by clunky software.
- **Frustrations:** Deeply skeptical of "AI" suggestions unless proven reliable; hates re-entering data; will revert to paper if the tool slows them down even slightly.
- **Tech comfort:** Varies widely by age/specialty — do not assume high comfort.
- **What they care about most:** Speed of the EMR/prescription flow above almost everything else in the first 90 days; AI trust comes later, after basic reliability is proven.
- **Note:** This persona can single-handedly kill adoption even if the owner has already paid — front-line clinical buy-in is a distinct risk from the purchase decision.

### Persona D — "Front-Desk / Nurse" (Daily End-User, Adoption Gatekeeper)
- **Role:** Registers patients, manages queues, handles first-line data entry.
- **Goals:** Move patients through quickly, avoid being blamed for queue delays.
- **Frustrations:** Least involved in the buying decision but most affected by a bad UI; highest-turnover role, meaning training must be repeatable, not one-time.
- **What they care about most:** Simplicity and speed of the registration/billing screens — this persona's daily friction is an underrated churn driver.

---

## 4. Customer Journey Map

| Stage | Customer Actions | Thoughts / Emotions | Pain Points | Startup's Opportunity |
|---|---|---|---|---|
| **Awareness** | Hears about digitization (peer hospital, ABDM mandate, industry event, referral) | "Do we actually need this now, or can it wait?" | Information overload — 20+ vendors claim similar things | Be specific about *who* you serve (not generic "AI-powered HMS for all hospitals") |
| **Consideration** | Compares 2–4 vendors, asks peers, checks pricing | "Which of these is actually different, and which will still exist in 2 years?" | Hard to tell products apart; pricing pages inconsistent across the market | Transparent, simple pricing; a specific case study from a similar-sized hospital |
| **Evaluation / Trial** | Requests a demo, maybe a pilot | "Will my staff actually use this? Will it slow us down?" | Demos often oversell; real-world workflow fit is unclear until hands-on | Offer a real (not scripted) pilot with the actual target persona (front desk + doctor), not just the owner |
| **Purchase Decision** | Owner-doctor commits budget | "Am I making a mistake switching from what we know, even if it's bad?" | Switching-cost inertia is very real — see Validation Report Section 14 | Make the migration path explicit and low-risk (e.g., phased cutover, data migration support included) |
| **Onboarding / Migration** | Data migration, staff training | Anxiety about disruption to live patient care | Highest-risk moment for churn — a bad first two weeks can end the relationship | White-glove onboarding for at least the first 10 customers; do not treat this as self-serve at MVP stage |
| **Adoption** | Staff use it daily | Frustration if the tool is even slightly slower than the old process | Front-desk/nurse resistance if UI isn't fast | Measure daily active usage per role, not just facility-level signup |
| **Renewal / Expansion** | Owner decides whether to continue, add modules, or refer others | "Was this worth it? Would I recommend it?" | No clear reason to expand without proven ROI | Ask for a case study/reference at renewal, not before — earn it first |

---

## 5. Customer Pain Points (Mapped to Persona, for Product Prioritization)

| Pain Point | Whose Pain | Product Relevance |
|---|---|---|
| Manual OPD billing errors / revenue leakage | Owner-doctor, Ops Manager | **Must-have** driver — directly ties to Section 9 |
| Slow, paper-based patient history lookup during consultation | Treating Doctor | **Must-have** — this is the moment that determines clinical adoption |
| Long queues from slow manual registration | Front-desk/Nurse | **Must-have** — daily friction that drives silent abandonment |
| No visibility into today's patient volume / revenue at a glance | Owner-doctor, Ops Manager | **Should-have** — a simple dashboard, not a BI suite |
| Compliance/ABDM empanelment pressure | Owner-doctor | **Must-have** (if India-confirmed) — increasingly a forced-adoption trigger, not optional |
| Fear that AI will recommend something clinically wrong | Treating Doctor | Product implication: **AI features must be opt-in and clearly explainable in v1**, not default-on |
| Fear of vendor lock-in / data loss if the startup fails | Owner-doctor | Product implication: **make data export easy and advertise it** — counterintuitively builds trust |

---

## 6. Buying Triggers

| Trigger | Why It Matters | How to Target It |
|---|---|---|
| ABDM / government scheme empanelment deadline | Converts a "nice to have" into a compliance requirement — the single strongest forcing function currently visible **[Fact, from Validation Report]** | Lead GTM messaging with compliance readiness for facilities facing empanelment deadlines |
| Discovered billing/revenue leakage (e.g., after an audit) | Creates urgency and a quantifiable ROI story | Target hospitals recently audited or newly NABH-accreditation-seeking |
| Opening a second branch/location | Standardization becomes necessary, not optional | Watch for expansion announcements in local health-business news |
| Bad experience with current vendor (support failure, price hike, downtime) | Switching intent already exists — lowest-resistance prospect | Build relationships with regional HMS resellers/consultants who hear about churn first |
| New hospital leadership / ownership transition | New decision-makers often want to "modernize" as a signal | Track ownership changes via local business/medical association news |
| Peer hospital visibly digitizing | Social proof pressure among owner-doctors in the same city/network | Case studies and referrals matter disproportionately here |
| Patient complaints about lost records / long waits | Reputational pain becomes a felt problem for the owner | Messaging that ties the product directly to patient experience, not just back-office efficiency |

**[New assumption]** These triggers are inferred from the pain points and market dynamics already established in the Validation Report, not confirmed by direct customer conversations — validate which trigger is actually most common before building marketing around it.

---

## 7. Jobs-To-Be-Done (JTBD) Analysis

Using the format: *"When [situation], I want to [motivation], so I can [outcome]."*

| Persona | Functional JTBD | Emotional JTBD | Social JTBD |
|---|---|---|---|
| Owner-Administrator | "When patient volume grows, I want to stop losing revenue to manual billing errors, so I can keep margins healthy without hiring more admin staff." | "I want to feel confident my hospital isn't quietly bleeding money." | "I want my hospital to be seen as modern and compliant among peer facilities." |
| Ops Manager | "When I report to the owner, I want accurate numbers without manually reconciling spreadsheets, so I can spend less time on data entry and more on operations." | "I don't want to be blamed for errors caused by a broken process." | — |
| Treating Doctor | "When I'm mid-consultation, I want instant access to a patient's history, so I don't waste time or risk a clinical mistake." | "I want to trust the tool enough to not double-check everything it shows me." | "I don't want to look incompetent in front of a patient because the system is slow." |
| Front-Desk/Nurse | "When a patient walks in, I want to register them in under a minute, so the queue doesn't build up." | "I don't want to be the reason patients are angry in the waiting room." | — |
| Patient (indirect) | "When I visit a new doctor, I want my past records available, so I don't have to repeat my history or redo tests." | "I want to feel like the hospital has its act together." | — |

**Product implication:** The MVP's single most important job to nail is the **Treating Doctor's functional JTBD** (fast, reliable patient history access) — if clinicians don't trust the speed and accuracy of this flow, no amount of owner-level ROI messaging will drive adoption.

---

## 8. MVP Feature List

Directly extending the Validation Report's MVP scope (Section 16) with product-level detail:

| Feature Area | Detail |
|---|---|
| Patient registration & scheduling | Walk-in and booked appointments, calendar view, duplicate-patient detection |
| EMR & e-prescription | Structured patient history, prescription templates, basic drug-interaction warnings (rules-based, not AI-generated — see Section 9 for why AI is deferred) |
| OPD billing | Invoice generation, payment tracking (cash/card/UPI), daily collection summary |
| Doctor dashboard | Today's queue, one-click access to a patient's full history |
| Role-based access | Separate views/permissions for owner, admin, doctor, front-desk |
| Patient communication | SMS/WhatsApp appointment reminders and prescription delivery |
| ABDM/ABHA-ready ID linking | **[Carried-forward assumption — India only]** Patient ID creation/linking compliant with national health ID standards |
| Basic admin dashboard | Today's patient count, revenue snapshot — deliberately simple, not a full BI suite |

---

## 9. MoSCoW Prioritization

| Priority | Features | Rationale |
|---|---|---|
| **Must Have** | Patient registration & scheduling · EMR & e-prescription · OPD billing · Doctor dashboard · Role-based access · ABDM/ABHA ID linking (if India-confirmed) | These directly address the Must-have pain points in Section 5 and the core JTBD in Section 7. Without these, there is no viable product. |
| **Should Have** | WhatsApp/SMS reminders · Basic admin dashboard · Simple daily/weekly reports | High value, but the product is usable without them on day one of a pilot |
| **Could Have** | Manual lab report upload/view (not full lab-instrument integration) · Basic pharmacy stock tracking · Simple video telemedicine | Real value, but adds scope risk — only pull forward if a specific pilot customer's workflow requires it |
| **Won't Have (v1)** | AI clinical decision support · Predictive analytics/BI · Multi-branch/enterprise management · Insurance claims automation · Marketplace/ecosystem integrations · Full IPD/OT workflows | Explicitly deferred per the Validation Report's roadmap (Phase 2+) — building these before proving the Must-haves work is the single most common failure mode in this category |

**Why AI is deliberately excluded from v1:** Section 7's JTBD analysis shows the doctor persona's dominant need is *speed and trust in the basics*, not AI novelty. Section 14 of the Validation Report also flags AI clinical liability as a high-severity risk. Shipping AI clinical assistance only after core reliability is proven with real users reduces both product risk and legal exposure — this is a deliberate sequencing decision, not a scope cut for its own sake.

---

## 10. Pricing Assumptions

**These are hypotheses to test in Section 11, not final pricing.**

| Stage | Structure | Illustrative Range | Basis |
|---|---|---|---|
| Pilot (first 3–5 customers) | Free or heavily discounted, 90 days, in exchange for structured feedback and a case-study commitment | ₹0–2,000/month | **[New assumption]** — standard practice for early design partners; the goal is usage data, not revenue |
| Starter (solo/small clinic, post-pilot) | Flat monthly subscription, core features only | ₹2,000–5,000/month | Anchored to Validation Report's clinic pricing benchmark (₹2,000–8,000/month) |
| Growth (ICP 1: 20–100 bed hospital) | Flat or per-bed subscription, core + Should-have features | ₹8,000–15,000/month | Anchored to Validation Report's hospital pricing benchmark (₹8,000–25,000/month), priced at the lower-to-mid end to account for being a new, unproven vendor |
| Add-ons (later phases) | Priced separately once built — telemedicine, AI modules, pharmacy/lab | Not yet defined | Deliberately undefined at MVP stage — pricing AI/advanced features before they exist and are validated would be premature |

**Key risk flagged explicitly:** competitors were found offering flat annual fees as low as ₹10,000/year. Pricing at or above the "Growth" range above requires a genuinely felt differentiation (see Validation Report Section 9) — otherwise this becomes a pure price competition the startup is not positioned to win as a new entrant.

---

## 11. Customer Validation Plan

| Phase | Goal | Method | Sample Size | Success Signal |
|---|---|---|---|---|
| **A — Problem Interviews** | Confirm pain points and ICP assumptions are real, not assumed | Structured 20–30 min interviews with owner-doctors and ops managers in target segment | 10–15 | At least 60–70% independently describe the Section 5 pain points unprompted |
| **B — Concept & Pricing Test** | Test whether the *specific* MVP concept (not just "an HMS") resonates, and get an honest pricing reaction | Clickable prototype walkthrough + direct pricing question | 5–8 | At least 3–4 give a specific, plausible price they'd pay (not a vague "sounds good") |
| **C — Pilot Program** | Test real-world usage across all four personas, not just the buyer | 90-day pilot at 3–5 facilities with defined metrics (see below) | 3–5 facilities | Daily active usage by front-desk and doctor personas, not just the owner logging in once |
| **D — Paid Conversion Test** | Confirm willingness to pay in practice, not just in interviews | Convert at least 1–2 pilot facilities to a paying contract before pilot ends | 1–2 conversions minimum | A facility pays *before* being asked to renew — this is the strongest signal in the whole plan |

**Sample discovery questions for Phase A** (starting point, not a fixed script):
1. Walk me through how a patient gets registered and billed today, start to finish.
2. What's the last time a billing or record-keeping mistake actually cost you money or a patient complaint?
3. What software have you tried before, and why did you stop using it (or why haven't you started)?
4. If I could fix one thing about your current process tomorrow, what would move the needle most?
5. What would make you say no to a new vendor, even if the product looked good?

**Pilot success metrics to define in writing before Phase C begins:** % reduction in billing errors, average registration time, daily active users by role, and a direct end-of-pilot question: *"Would you pay for this starting next month?"*

---

## 12. Startup Risks (Product & Customer-Specific)

| Risk | Why It Matters Here Specifically |
|---|---|
| Pilot hospitals are relationship-driven, not representative of cold market demand | Free pilots often say yes to be polite — Phase D's paid-conversion test exists specifically to catch this |
| Feature creep during pilots | Each pilot facility will ask for its own custom feature; without discipline, the MVP scope from Section 9 will silently expand |
| Loss of the internal champion (Ops Manager or Owner) mid-pilot | Small hospitals have thin management — losing the one person driving adoption internally can kill a pilot with no fallback |
| Doctor-level resistance surviving the sale | The owner can approve a purchase; the treating doctor can still quietly refuse to use it — see Persona C |
| Building for one hospital's idiosyncratic workflow | A pilot success that only works because it was custom-built for one facility does not generalize — watch for this explicitly during Phase C |
| Data migration failure during onboarding | Directly tied to the Validation Report's cited ~4.7% integration-failure statistic — this is a known, not hypothetical, failure mode in this category |
| Underpricing to win pilots, then struggling to raise prices later | Anchoring too low in Section 10 to win the first few logos can make the eventual "Growth" tier price increase feel like a bait-and-switch |

---

## 13. Founder Action Sheet

A practical, checkable list — not aspirational, meant to be worked through directly.

**Customer discovery**
- [ ] Identify 15–20 target hospitals/clinics matching ICP 1 in your actual target city/region
- [ ] Get 10–15 completed Phase A interviews (Section 11) — do not skip to building before this
- [ ] Write down every objection raised, verbatim — these will shape messaging later

**Competitive & pricing groundwork**
- [ ] Get live demos from 3 of the competitors named in the Validation Report (or local equivalents)
- [ ] Document their actual pricing, not just listed pricing — ask what a real hospital your size would pay
- [ ] Identify one specific, defensible reason a target customer would choose you over them

**Product scoping**
- [ ] Confirm the Must-Have list in Section 9 with at least 5 interviewees before building
- [ ] Build a clickable prototype (not production code) for Phase B testing
- [ ] Explicitly decide: is AI in the v1 pitch deck/marketing at all, or fully deferred to Phase 2 messaging?

**Compliance & legal**
- [ ] Confirm ABDM/ABHA requirements with a compliance consultant if targeting India — do not self-diagnose this
- [ ] If any AI clinical-assistance feature is planned even for later phases, get a legal read on liability exposure now, not when it's built

**Pilot recruitment**
- [ ] Recruit 3–5 design-partner facilities with a written pilot agreement (scope, duration, success metrics)
- [ ] Get at least a soft, written pricing commitment before the pilot ends
- [ ] Plan white-glove onboarding — do not treat pilot onboarding as self-serve

**Founder-market fit (unresolved from the Validation Report)**
- [ ] Honestly document the team's actual healthcare/health-IT experience and relationships
- [ ] If a gap exists, decide now whether to close it via a co-founder, advisor, or design-partner network — before scaling spend on sales or product

---

## 14. 30-Day MVP Execution Roadmap

This is a **build-and-test** roadmap, distinct from the Validation Report's discovery-focused 30-day plan — assumes Phase A discovery interviews are already underway or complete.

| Week | Focus | Deliverables |
|---|---|---|
| **Week 1** | Finalize scope & design | Confirm ICP 1 and the Must-Have list (Section 9) with real interview data; wireframe the four core flows: registration, EMR/prescription, billing, doctor dashboard |
| **Week 2** | Build core clinical & registration flow | Working (even if rough) registration → EMR → e-prescription flow; internal test with a mock patient load |
| **Week 3** | Build billing, dashboard, and access control | OPD billing, doctor dashboard, role-based access; run Phase B concept/pricing test in parallel using the prototype |
| **Week 4** | Pilot onboarding | Onboard 1–3 pilot facilities (start smaller than the full 3–5 to control quality); live data entry with founder/team physically present or on-call; daily check-ins with front-desk and doctor users specifically |

**End-of-30-days checkpoint:** at least one facility actively using the Must-Have flow with real patients, documented usage by role (not just owner login), and a concrete list of what broke — this list becomes the Week 5+ priority backlog, not new feature requests from Section 8's Could-Have/Won't-Have lists.

---

*This document is a structured planning artifact built on the Validation Report's secondary research and standard product/UX frameworks (ICP, persona, JTBD, MoSCoW, customer journey mapping). It contains no new primary market research — every persona, trigger, and pricing figure marked [New assumption] must be tested against real customers via Section 11 before being treated as fact.*
