# Regulatory Compliance Assessment: YouTube

> **Type:** Outside-in regulatory compliance posture review
> **Subject:** YouTube (Google LLC / Alphabet Inc.), with a focus on privacy, children's data, and age assurance
> **Date:** September 29, 2026
> **Basis:** Publicly available information only. No internal systems, policies, or audit reports were reviewed.

---

## 1. Purpose, Scope, and Limitations

This document is a companion to the earlier Data Privacy Audit and the PIA of YouTube's AI age estimation system. It maps YouTube's exposure against the main regulatory regimes that apply to its data practices and identifies where compliance is established, contested, or still developing.

**Important limitations**

- This is not a certification or a legal opinion. A finding that an area is "under scrutiny" does not mean a violation has occurred.
- Regulatory positions change quickly. Dates and status reflect public sources available on the assessment date and should be verified against primary sources (regulator websites, official journals) before being relied on.
- YouTube's actual compliance controls are not visible from outside. Ratings describe **regulatory exposure**, not confirmed non-compliance.

**Status legend**

| Status | Meaning |
|---|---|
| Established | A regulator or court has already acted, so the issue is documented |
| Under scrutiny | Active investigation, information request, or credible complaint |
| Gap risk | No public action, but a structural tension with the rules exists |
| Upcoming | Obligation announced or proposed, not yet fully in force |
| Aligned (reported) | Public reporting indicates YouTube has taken compliance steps |

---

## 2. Executive Summary

| Regime | Jurisdiction | Status | Exposure |
|---|---|---|---|
| COPPA and amended COPPA Rule | United States | Established | High |
| Australia Social Media Minimum Age law | Australia | Aligned (reported) | Medium |
| Digital Services Act (minors, recommender systems) | European Union | Under scrutiny | High |
| GDPR and ePrivacy | EU / EEA | Under scrutiny / Gap risk | High |
| EU KIDS Act (proposal, September 2026) | European Union | Upcoming | High |
| UK Online Safety Act and Children's Code | United Kingdom | Gap risk | Medium-High |
| DPDP Act and Rules, 2025 | India | Upcoming | High |
| State privacy and biometric laws | United States | Gap risk | Medium |

**Key takeaways**

1. The strongest documented compliance history is in **children's data**: a record 2019 FTC settlement and a $30 million class settlement approved in January 2026.
2. The dominant theme across regimes is **age assurance**. Nearly every regulator now expects platforms to know or reasonably estimate user age, while privacy law limits the data that can be collected to do so.
3. The **EU** is the most active enforcement front, with the Commission examining YouTube's age assurance and recommender system under the Digital Services Act.
4. **India's DPDP Rules** create a new, stricter children's-data standard (under 18, verifiable parental consent, no behavioral tracking or targeted advertising directed at children) that takes full effect around May 2027.
5. YouTube's response in Australia, signing out under-16 users, shows the platform will comply with hard age limits when required, which raises the question of consistency elsewhere.

---

## 3. Regime-by-Regime Assessment

### 3.1 United States: COPPA

**Requirement.** Operators of child-directed services, or those with actual knowledge that they collect data from children under 13, must obtain verifiable parental consent before collecting personal information, which includes persistent identifiers used for tracking.

**Public record**

- 2019: YouTube and Google settled with the FTC and the New York Attorney General for $170 million ($136 million and $34 million) over allegations of collecting children's data, including tracking identifiers, without parental consent.
- January 2026: final approval of a $30 million class settlement covering U.S. children under 13 who watched child-directed content between July 2013 and April 2020.
- December 2025: Disney agreed to a $10 million penalty over failing to label YouTube videos as made for kids. This was a creator-side case, but it demonstrates that the labeling system YouTube relies on can fail.

**Compliance model and weak points**

- YouTube requires creators to designate content as made for kids and applies restrictions (for example, limited data collection and no personalized ads) to that content.
- The model depends heavily on creator self-declaration, which is the pattern the Disney case exposed.
- The FTC amended the COPPA Rule in 2025. Public commentary places the compliance deadline for most new requirements in April 2026. Check the current rule text for retention, separate consent for third-party disclosure, and security program requirements.

**Assessment:** Established issue with ongoing structural risk. Exposure: **High**.

**Control checklist**

- [ ] Automated detection of child-directed content, not only self-declaration
- [ ] Documented data retention limits for children's data
- [ ] Separate consent flow for any third-party disclosure
- [ ] Written information security program covering children's data
- [ ] Periodic audit of made-for-kids designation accuracy

---

### 3.2 Australia: Social Media Minimum Age

**Requirement.** Under the Online Safety Amendment (Social Media Minimum Age) Act 2024, age-restricted platforms must take "reasonable steps" to prevent Australians under 16 from holding accounts. Maximum penalties are reported at A$49.5 million. The law took effect on December 10, 2025, and the regulator (eSafety) lists YouTube among the covered services.

**Public record**

- YouTube initially argued against inclusion, then announced it would comply, automatically signing out users under 16 from December 10, 2025. Viewers can regain access when they turn 16.
- The framework limits how age can be proven: reporting indicates platforms may not require government ID as the sole method, and privacy obligations under the Privacy Act 1988 apply in parallel.
- eSafety's March 2026 compliance update criticized certain weak industry practices in general terms, such as letting users revise a stated age using a low-confidence method, or allowing repeated attempts with the same method. These points were not specific to YouTube but describe what regulators are testing.

**Assessment:** Aligned (reported), with ongoing monitoring obligations. Exposure: **Medium**.

**Control checklist**

- [ ] More than one age assurance method, with escalation rather than repeated retries
- [ ] Protection against immediate re-registration by removed users
- [ ] Privacy Act and Australian Privacy Principles review of the age assurance data flow
- [ ] Measures to limit wrongful removal of adult accounts

---

### 3.3 European Union: Digital Services Act (DSA)

**Requirement.** As a very large online platform, YouTube must assess and mitigate systemic risks, including risks to minors, and ensure a high level of privacy, safety, and security for minors. The DSA also prohibits targeted advertising to minors based on profiling. The Commission's July 2025 guidelines on protecting minors recommend high standards of design and privacy by default, and caution against recommender systems that rely on behavioral data so extensive that it captures all or most of a minor's activity.

**Public record**

- October 10, 2025: the Commission sent information requests to YouTube (alongside Snapchat, Apple App Store, and Google Play) about its age assurance system and, for YouTube specifically, its recommender system following reporting about harmful content reaching minors.
- In 2026 the Commission has issued preliminary findings against other platforms on minors-related and design issues, showing that the enforcement pipeline is active. No public preliminary finding against YouTube on this topic was identified in the sources reviewed.

**Assessment:** Under scrutiny. Exposure: **High**, given potential fines under the DSA and the direction of enforcement.

**Control checklist**

- [ ] Documented, current systemic risk assessment covering minors
- [ ] Recommender settings for minors that limit reliance on extensive behavioral data
- [ ] No profiling-based advertising to users known or estimated to be minors
- [ ] Evidence that age assurance measures are effective and proportionate
- [ ] Complete responses to Commission information requests

---

### 3.4 European Union: GDPR and ePrivacy

**Requirement.** Lawful basis for processing, purpose limitation, data minimization, transparency, restrictions on profiling and on special-category or biometric data, consent for accessing information on a user's device, and a DPIA for high-risk processing.

**Points of exposure**

- **Age inference as profiling.** Using viewing and search behavior to infer age is large-scale profiling. A DPIA, a clear lawful basis, and purpose limitation are needed. Whether age estimation from behavior is proportionate is an open regulatory question.
- **Biometric verification.** Selfie-based age verification can approach biometric processing. Where it is used to uniquely identify a person, stricter rules apply. Age estimation without identification is treated differently, so the exact design matters.
- **Ad-blocker detection.** Privacy advocates have argued that client-side detection scripts require consent under the ePrivacy rules because they access information on the user's device. This is a legal-interpretation dispute, not an established violation.
- **Embedded players and pre-consent data flows.** Data transmitted to Google from embedded videos before user interaction is a recurring consent question.

**Assessment:** Under scrutiny (ad-blocker detection, age assurance) and gap risk (profiling, embeds). Exposure: **High**.

**Control checklist**

- [ ] Current DPIA for age estimation and for recommendation profiling
- [ ] Documented lawful basis for each processing purpose
- [ ] Legal opinion on client-side detection under ePrivacy
- [ ] Privacy-enhanced embed mode as default
- [ ] Retention schedule for verification data with verified deletion

---

### 3.5 European Union: KIDS Act (Proposal)

**Status.** In September 2026 the European Commission proposed the EU KIDS Act. Public descriptions say it combines safety-by-design requirements across risky digital services with a minimum-age framework for social media and video-sharing platforms, including YouTube, and a European approach to age assurance. Reporting describes a graduated approach for under-15s and a requirement for very large platforms to seek Commission authorization before rolling out new features that could affect children.

**Assessment:** Upcoming. This is a **proposal**, not law, and its final content may change during the legislative process. Exposure: **High** if adopted as described, because it would affect product design, age assurance, and feature launches.

**Preparation checklist**

- [ ] Monitor the legislative process and any amendments
- [ ] Map current features against likely safety-by-design requirements
- [ ] Build a review process for new features that could affect children
- [ ] Align age assurance design with the expected European approach

---

### 3.6 United Kingdom: Online Safety Act and Children's Code

**Requirement.** The Online Safety Act places duties on services likely to be accessed by children, including highly effective age assurance for certain harmful content. The Age-Appropriate Design Code expects high-privacy defaults and limits on profiling of children.

**Points of exposure**

- Whether YouTube's age estimation and appeal methods meet the "highly effective" standard, and whether they do so in a privacy-proportionate way.
- Defaults for users identified as children, including recommender and advertising settings.

**Assessment:** Gap risk. No public enforcement action against YouTube specifically was identified in the sources reviewed. Exposure: **Medium-High**.

**Control checklist**

- [ ] Documented assessment against the regulator's age assurance guidance
- [ ] Children's risk assessment kept current
- [ ] High-privacy defaults for identified children

---

### 3.7 India: DPDP Act, 2023 and DPDP Rules, 2025

**Requirement.** The Rules were notified in mid-November 2025 (sources cite November 13 or 14) and phase in over about 18 months. Full obligations for data fiduciaries, including consent notices, security safeguards, breach notification, retention and erasure, and verifiable parental consent, are expected to apply around mid-May 2027. Sources differ slightly on exact dates, so verify against the official gazette.

**Children's data provisions (as publicly described)**

- A child is anyone under 18.
- Verifiable parental or guardian consent is required before processing a child's personal data.
- Behavioral tracking and targeted advertising directed at children are restricted, with limited exemptions such as certain health, education, and safety purposes.
- Breach notification to the Data Protection Board is required, with a 72-hour reporting element in public summaries.
- Penalties for violations of children's data obligations are reported at up to INR 200 crore.

**Points of exposure**

- The 18-year threshold is higher than the 13 used under COPPA, so a global design built around 13 will not meet Indian requirements.
- Verifiable parental consent for a very large consumer platform is operationally difficult, and the verification method itself involves collecting parent identity data.
- Whether YouTube could be designated a Significant Data Fiduciary, which would add audit and DPIA duties.

**Assessment:** Upcoming, with a defined deadline. Exposure: **High** because of the higher age threshold, the tracking ban, and the size of the potential penalty.

**Control checklist**

- [ ] India-specific age and consent design for users under 18
- [ ] Verifiable parental consent mechanism that minimizes additional data collection
- [ ] Removal of behavioral tracking and targeted advertising for under-18 users in India
- [ ] Breach response process aligned to the 72-hour requirement
- [ ] Consent notices in the required languages

---

### 3.8 United States: State Privacy and Biometric Laws

**Points of exposure**

- State comprehensive privacy laws (for example, California's CCPA/CPRA) give rights over sensitive personal information and inferences and require opt-outs from sale or sharing of data for cross-context behavioral advertising.
- Biometric privacy laws (for example, Illinois BIPA) require notice and written consent before collecting biometric identifiers, which is relevant if selfie-based verification is used in those states.
- Several states have passed or are considering age-appropriate design and age verification laws, some of which face constitutional challenges.

**Assessment:** Gap risk. Exposure: **Medium**, with variation by state.

**Control checklist**

- [ ] State-by-state applicability matrix
- [ ] Biometric consent flow for any selfie-based verification
- [ ] Honoring of opt-out preference signals

---

## 4. Cross-Cutting Compliance Themes

### 4.1 The age assurance dilemma

| Pressure toward more age data | Pressure toward less age data |
|---|---|
| Australian minimum-age law | GDPR data minimization |
| EU DSA and proposed KIDS Act | Australian rule against ID as sole method |
| UK Online Safety Act | Biometric privacy laws |
| India DPDP (verifiable parental consent) | Purpose limitation on derived inferences |

A compliant design has to satisfy both columns at once. The most defensible approach is layered age assurance with a privacy-preserving option at each step, immediate deletion of verification data, and strict purpose limitation.

### 4.2 Inconsistent age thresholds

| Jurisdiction | Relevant threshold |
|---|---|
| United States (COPPA) | Under 13 |
| European Union (proposed KIDS Act) | Under 15, graduated (proposal) |
| Australia | Under 16 |
| India (DPDP) | Under 18 |

Maintaining a single global age model is unlikely to satisfy all of these. Region-specific age logic is a compliance requirement, not just a product choice.

### 4.3 Reliance on creators for compliance

Both children's-data enforcement and labeling cases show that compliance depends partly on creator behavior. Platform-side detection and audit are needed to reduce that dependency.

---

## 5. Consolidated Gap Register

| ID | Gap or risk | Regimes affected | Priority |
|---|---|---|---|
| G1 | Creator self-declaration as primary child-content control | COPPA, DSA, DPDP | High |
| G2 | Verification path relying on ID, selfie, or card | GDPR, BIPA, Australia (ID-only rule), DPDP | High |
| G3 | Retention and deletion of verification data not publicly verifiable | GDPR, DPDP, COPPA | High |
| G4 | Behavioral inference of age without published accuracy or bias audits | GDPR, DSA, UK | High |
| G5 | Recommender reliance on extensive behavioral data for minors | DSA, UK Code | High |
| G6 | Single-threshold age design across jurisdictions | All | Medium-High |
| G7 | Client-side detection and pre-consent data flows | ePrivacy/GDPR | Medium |
| G8 | Readiness for KIDS Act and DPDP full-effect dates | EU, India | Medium-High |
| G9 | Limited public transparency on compliance metrics | DSA, general | Medium |

---

## 6. Recommended Compliance Roadmap

**Phase 1: Immediate (0-3 months)**
1. Publish accuracy and error-rate results for age estimation and commission an independent audit.
2. Confirm and publicly document deletion of ID, selfie, and card data after verification.
3. Provide at least one non-ID, non-biometric verification path in every region.
4. Complete and file current DPIAs for age estimation and recommender profiling.

**Phase 2: Near term (3-9 months)**
5. Build region-specific age logic (13, 15, 16, and 18 thresholds as applicable).
6. Reduce reliance on creator self-declaration through platform-side detection and audits.
7. Review recommender settings for minors against the DSA guidelines.
8. Prepare India-specific parental consent and tracking restrictions ahead of the May 2027 date.

**Phase 3: Ongoing**
9. Track the EU KIDS Act through the legislative process and prepare a feature-review process for children-affecting launches.
10. Publish regular transparency reports covering age assurance, appeals, and children's data enforcement.
11. Re-run this assessment whenever a regulator acts or a threshold changes.

---

## 7. Regulatory Watchlist

| Item | What to watch |
|---|---|
| EU Commission DSA proceedings | Any move from information requests to formal proceedings or preliminary findings involving YouTube |
| EU KIDS Act | Amendments to age thresholds, scope, and the authorization requirement for new features |
| India DPDP full-effect date | Final operational guidance, verification mechanisms, Significant Data Fiduciary designations |
| Australian eSafety enforcement | Compliance reviews and any action on age assurance quality |
| COPPA Rule enforcement | First enforcement under the amended Rule requirements |
| Ad-blocker detection complaints | Any regulator or court ruling on the ePrivacy question |

---

## 8. Sources

- European Commission (October 10, 2025): information requests to Snapchat, YouTube, Apple App Store, and Google Play on protection of minors under the DSA
- European Commission: policy page on protecting and empowering young people online, describing the DSA provisions and the September 2026 KIDS Act proposal
- Euronews (September 2026): reporting on the proposed EU Kids Act and under-15 restrictions
- European Parliament follow-up document: Commission commentary on recommender-system recommendations in the minors guidelines
- NBC News, Bloomberg, TechRadar, and others: coverage of YouTube's compliance with the Australian under-16 law from December 10, 2025
- Legal and industry commentary on Australia's "reasonable steps" standard and eSafety's March 2026 compliance update
- Press Information Bureau (India) and law-firm and consultancy summaries: DPDP Rules, 2025 notification, phased timeline, and children's data provisions
- News coverage of the 2019 FTC/New York settlement, the January 2026 $30 million class settlement, and the December 2025 Disney COPPA penalty

*Prepared as an educational, public-information analysis. Not legal advice. Verify dates and requirements against primary sources.*
