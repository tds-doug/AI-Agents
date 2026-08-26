# Nell's Legal Knowledge Base

Cross-project legal research repository. Nell consults this before searching the
web and updates it after each research task. This is her persistent memory for
verifiable legal frameworks, compliance requirements, and jurisdictional rules.

**Format:** Topic entries by jurisdiction/framework. Each entry includes concise
findings, authoritative sources (with URLs and dates), volatility notes, and
related task references.

---

## Jurisdictions & Frameworks (index)

- European Union (GDPR, ePrivacy, etc.)
- United States (Federal: FTC, COPPA; State: CCPA/CPRA, others)
  - California: CCPA/CPRA, CIPA (wiretap litigation), Automatic Renewal Law
    (CARL), Age-Appropriate Design Code Act (CAADCA, enjoined in part), Unruh
    Civil Rights Act (accessibility), CalOPPA (baseline privacy-policy
    content law, no revenue threshold)
  - Florida: Florida Digital Bill of Rights (FDBR), FDUTPA, Florida
    Telephone Solicitation Act (FTSA), Florida Security of Communications Act
    (FSCA, wiretap litigation), HB 3 (Online Protections for Minors)
- United Kingdom (GDPR retained post-Brexit, ICO guidance)
- Canada (PIPEDA, AODA, others)
- Australia (Privacy Act, APPs)
- App Store Policies (Apple, Google — updated regularly)
  - Apple: App Tracking Transparency (Guideline 5.1.2), Privacy Nutrition
    Labels / Privacy Manifests, In-App Purchase (Guideline 3.1.1, US external
    payment links post-Epic v. Apple)
- International (data localization, export controls, etc.)

---

## Topics (alphabetical — add as researched)

(This section will grow as Nell researches legal domains. Each entry below is a
template; entries will be filled in after research.)

### Accessibility — WCAG 2.2 Level AA (Web) & California Unruh Act (Mobile Apps)

**Jurisdictions:** USA (ADA Title III applies to public-facing apps; California
Unruh Civil Rights Act adds state-law exposure), EU (EN 301 549), Canada
(AODA), others.

**Key findings:**
- WCAG 2.2 published by W3C 2023-10-05; latest version operative.
- Level AA is common legal requirement in EU, parts of USA.
- Color contrast ratio 4.5:1 for normal text (WCAG Level AA).
- Keyboard navigation, screen reader support, alt-text, captions mandatory.
- **California Unruh Civil Rights Act (Cal. Civ. Code §51):** state
  anti-discrimination law that plaintiffs' firms have used aggressively
  against websites *and mobile apps* alleged to be inaccessible to
  screen-reader/assistive-tech users. California courts have applied it to
  apps that serve California residents regardless of where the business is
  headquartered. Complaints typically cite WCAG 2.1/2.2 Level AA as the
  benchmark for "accessible," even though WCAG itself is not directly
  incorporated into the statute. Statutory damages: minimum **$4,000 per
  violation** (Cal. Civ. Code §52) plus actual damages and attorney's fees —
  this fee-shifting/statutory-damages combination is what drives high litigation
  volume; California generates more digital accessibility lawsuits than any
  other state.
  - *Robles v. Domino's Pizza LLC*, 913 F.3d 898 (9th Cir. 2019) — held
    Domino's website **and mobile app** must be accessible under Title III of
    the ADA, reasoning that the ADA's "nexus" requirement is satisfied where
    the app/site is a means of accessing the physical restaurant's goods and
    services; by extension, an ADA violation typically supports an Unruh Act
    claim as well (Unruh incorporates ADA violations as per se Unruh
    violations).
    - Verify current citation/status before citing in advice: found via
      secondary sources, not yet independently confirmed against a primary
      case-law database (e.g., Justia/Court Listener/official 9th Cir.
      opinion) as part of this research pass.
  - *Thurston v. Midvale Corp.*, 39 Cal. App. 5th 634 (2019) — California
    Court of Appeal found a restaurant's inaccessible website violated both
    the ADA and the Unruh Act.
    - Same verification caveat as above — cite only after confirming against
      a primary source.
- No verified authoritative source found (as of this research pass)
  establishing that Apple App Store review itself imposes an independent WCAG
  compliance *requirement* for approval; Apple's Accessibility Nutrition
  Labels (App Store Connect) let developers *disclose* supported accessibility
  features but this is a disclosure mechanism, not a confirmed legal
  mandate — do not conflate the two without further verification.

**Sources:**
- W3C WCAG 2.2: https://www.w3.org/WAI/WCAG22/quickref/
- ADA.gov Title III guidance: https://www.ada.gov/
- EN 301 549 (EU): European Commission
- Accessibility.Works, "Latest Unruh Act Rulings": https://www.accessibility.works/blog/unruh-act-website-compliance-california-website-accessibility/
- Level Access, "Unruh Civil Rights Act: A Business Compliance Guide": https://www.levelaccess.com/compliance-overview/california-unruh-civil-rights-act-compliance/
- ADA Title III (Seyfarth), background on CA accessibility bill activity: https://www.adatitleiii.com/2023/06/new-california-assembly-bill-on-website-accessibility-could-result-in-a-lawsuit-tsunami/

**Date researched:** 2026-07-17 (Unruh Act portion added; WCAG portion
refreshed, originally undated).
**Volatility:** WCAG updates every ~3 years; re-check annually for new
version. Unruh Act litigation volume and theories shift frequently — treat the
two case citations above as **leads requiring primary-source verification**,
not confirmed-verified precedent, until independently checked against an
official reporter or court database.
**Related tasks:** TASK-Nell-1 (deep-dive: iPhone apps in CA/FL, 2026-07-17)

---

### Copyright & Open Source License Compliance

**Key findings:**
- GPL (v2, v3) is copyleft: derivative works must be released under same
  license.
- MIT, Apache 2.0 are permissive: allow proprietary derivatives if license text
  is included.
- SPDX: standard for expressing license combinations.
- Mixing incompatible licenses can create legal liability.

**Sources:**
- GitHub License Chooser: https://choosealicense.com/
- SPDX Licenses: https://spdx.org/licenses/
- FSF: https://www.fsf.org/
- OSI: https://opensource.org/

**Date researched:** [will update]
**Volatility:** Low (licenses are stable).
**Related tasks:** [will link]

---

### GDPR — Data Protection (EU)

**Key findings:**
- Applies if processing personal data of EU residents, regardless of developer
  location.
- Legal bases: consent, contract, legal obligation, legitimate interest, vital
  interest, public task.
- Data subject rights: access, rectification, erasure ("right to be forgotten"),
  restriction, portability, objection.
- Retention: must be necessary and limited (no indefinite storage).
- Breach notification: within 72 hours to authority; "without undue delay" to
  affected individuals.
- Subprocessor liability: responsible for any processor you hire.
- Fines: up to 4% of annual global turnover or €20M, whichever is higher.

**Sources:**
- GDPR Official Text: https://gdpr-info.eu/
- ICO Guidance (UK): https://ico.org.uk/
- CNIL Guidance (France): https://www.cnil.fr/

**Date researched:** [will update]
**Volatility:** Moderate (court interpretations evolve; Schrems II changed
  transfer mechanisms).
**Related tasks:** [will link]

---

### Privacy Policy, Tracking & In-App Purchase — App Store Requirements (Apple / iPhone apps)

**Key findings:**
- Apple requires a privacy policy URL for all apps; must disclose data
  collection, use, sharing, and retention practices; must comply with
  applicable law (GDPR, CCPA, etc.).
- **Privacy Nutrition Labels** ("App Privacy" details, App Store Connect):
  developers must declare every category of data collected — tracking data,
  data linked to identity, and non-linked/anonymized data. Must match actual
  app behavior; Apple's automated tooling can detect SDK signatures, so
  under-disclosure (e.g., declaring "no data collected" while shipping an
  analytics SDK) is a live rejection/enforcement risk, not just a
  representation risk.
- **Privacy Manifests** (introduced 2024, strict enforcement by 2026): apps
  and third-party SDKs must declare "required reason" API usage and data
  practices in a manifest file; inconsistency between manifest, privacy
  policy, and nutrition label is a common rejection reason.
- **App Tracking Transparency (ATT) — Guideline 5.1.2** (in force since iOS
  14.5, April 2021, still controlling): apps must use the
  AppTrackingTransparency framework and show the system permission prompt
  (with a developer-supplied purpose string) before tracking a user or
  device across other companies' apps/websites, or before accessing the
  device's advertising identifier (IDFA). Any such tracking must also be
  declared in the App Privacy label and may only occur if permission is
  granted. On-device-only linkage that never leaves the device and can't
  identify the user/device is not "tracking" under this rule. Apps may not
  manipulate or coerce consent to the ATT prompt.
- **In-App Purchase — Guideline 3.1.1 (US storefront changes, 2025 court
  order):** Historically, Guideline 3.1.1 barred apps from linking out to
  external payment methods for digital goods/services, and required Apple's
  IAP (with Apple's commission). On April 30, 2025, Judge Yvonne
  Gonzalez Rogers (N.D. Cal., the Epic Games v. Apple injunction enforcement
  proceeding) found Apple in willful violation of the 2021 injunction. Apple
  subsequently updated the guideline: **on the US storefront only**, apps may
  now include buttons, external links, or other calls to action pointing to
  external purchase mechanisms/pricing, without the special "External
  Purchase Link" entitlement previously required, and without paying Apple's
  commission on those external transactions. This carve-out applies to the US
  storefront only — outside the US, Guideline 3.1.1's external-link
  restrictions and Apple's commission structure still generally apply (subject
  to separate developments in the EU under the Digital Markets Act, which is
  a distinct legal basis not yet researched in depth here). Apple is
  appealing; **re-verify current status before relying on this for a live
  release**, since the case is contested and the guideline could change again.

**Sources:**
- Apple App Store Review Guidelines: https://developer.apple.com/app-store/review/guidelines/
- Apple App Privacy Policy requirement: https://developer.apple.com/app-store/app-privacy-policy-on-the-app-store/
- Apple, App Privacy Details: https://developer.apple.com/app-store/app-privacy-details/
- Apple Developer, User Privacy and Data Use (ATT): https://developer.apple.com/app-store/user-privacy-and-data-use/
- Apple Developer Documentation, AppTrackingTransparency: https://developer.apple.com/documentation/apptrackingtransparency
- AppleInsider, "Apple's App Store Guidelines updated to reflect court order over external purchases" (2025-05-02): https://appleinsider.com/articles/25/05/02/apples-app-store-guidelines-updated-to-reflect-court-order-over-external-purchases
- Frankfurt Kurnit Klein & Selz, "Court Finds Apple Violated Order, Resulting in Key Changes for iOS External Purchase Methods": https://fkks.com/news/court-finds-apple-violated-order-resulting-in-key-changes-for-ios-external-purchase-methods

**Date researched:** 2026-07-17 (refreshed; original entry undated).
**Volatility:** High — Apple updates App Store Review Guidelines frequently,
and the 3.1.1 external-payment carve-out is the subject of active, ongoing
litigation (Epic v. Apple enforcement appeal); confirm current guideline text
and litigation posture before advising on either tracking consent flows or
payment-link implementation.
**Related tasks:** TASK-Nell-1 (deep-dive: iPhone apps in CA/FL, 2026-07-17)

---

### COPPA — Children's Online Privacy Protection Act (USA, Federal)

**Jurisdictions:** USA, federal (16 CFR Part 312; 15 U.S.C. §§6501–6505).

**Key findings:**
- Applies to operators of websites/online services **directed to children
  under 13**, and separately to any operator (regardless of stated audience)
  that has **actual knowledge** it is collecting personal information from a
  child under 13.
- "Directed to children" is a multi-factor test under 16 CFR §312.2 —
  subject matter, visual content, use of animated characters/child-oriented
  activities or incentives, music, language, presence of child models or
  celebrities, empirical evidence of actual/intended audience composition,
  etc. It is not satisfied or avoided by a developer's own label; it depends
  on these objective factors.
- 2025 amendments to the Rule took effect June 23, 2025; the amended
  provisions carry a **compliance deadline of April 22, 2026**, after which
  FTC enforcement actions can be brought under the new requirements
  (expanded definition of personal information, new parental-consent
  methods, stricter data security/retention obligations).
- Requires verifiable parental consent before collecting, using, or
  disclosing personal information from a child under 13 once COPPA is
  triggered; requires reasonable data-security procedures for children's
  data.
- Feb. 2026: FTC issued a policy statement saying it will not bring COPPA
  enforcement against operators that collect/use/disclose personal
  information **solely to determine a user's age** via age-verification
  technology — relevant if an app later adds age-gating.
- **Practical read for a small consumer app with no child-directed content
  and no age/birthdate collection at signup:** a "not directed to children
  under 13, no actual knowledge of under-13 users" claim in a privacy policy
  has a reasonable, verifiable basis on those facts — but re-verify if the
  app's content, marketing, or signup flow changes (e.g., adds a birthdate
  field, kid-oriented mascot/theming, or evidence of a child audience).

**Sources:**
- FTC, "Children's Online Privacy Protection Rule ('COPPA')": https://www.ftc.gov/legal-library/browse/rules/childrens-online-privacy-protection-rule-coppa
- Federal Register, COPPA Rule final amendments (2025-04-22): https://www.federalregister.gov/documents/2025/04/22/2025-05904/childrens-online-privacy-protection-rule
- eCFR, 16 CFR Part 312: https://www.ecfr.gov/current/title-16/chapter-I/subchapter-C/part-312
- FTC press release, COPPA age-verification policy statement (2026-02-25): https://www.ftc.gov/news-events/news/press-releases/2026/02/ftc-issues-coppa-policy-statement-incentivize-use-age-verification-technologies-protect-children

**Date researched:** 2026-08-05.
**Volatility:** Moderate-high — 2025 amendments have a live compliance
deadline (2026-04-22) that has likely already passed by the time this entry
is reused; re-verify current enforcement posture and whether further
amendments have issued. The age-verification safe-harbor policy statement is
new (Feb. 2026) and could be revised.
**Related tasks:** Brew Me Up (Coffee Shop Tracker) Disclaimer/Privacy Policy
update, 2026-08-05 — see `proposals/nell-disclaimer-privacy-update-2026-08.md`
in that project.

---

### CalOPPA — California Online Privacy Protection Act (baseline privacy-policy content law)

**Jurisdictions:** California (Cal. Bus. & Prof. Code §§22575–22579).
Distinct from and predating CCPA/CPRA — **no revenue or user-count
threshold**, unlike CCPA, so it can apply to small/solo-developer operators
that CCPA's size thresholds would exempt.

**Key findings:**
- Requires operators of commercial websites/online services that collect PII
  from California residents to **conspicuously post a privacy policy**. A
  2012 California AG announcement explicitly extended CalOPPA's application
  to **mobile applications** for smartphones/tablets, not just websites.
- A CalOPPA-compliant policy must disclose:
  1. Categories of PII collected;
  2. Categories of third parties the operator may share that PII with;
  3. The process (if any) for a consumer to review and request changes to
     their PII;
  4. How the operator notifies users of material changes to the policy;
  5. The policy's effective date.
- A 2014 amendment added a requirement to disclose how the operator responds
  to browser "Do Not Track" (DNT) signals, and whether third parties may
  collect PII through the site/app.
- Enforcement: supports a claim under California's Unfair Competition Law;
  operator gets a 30-day cure period after notice of noncompliance, then
  faces penalties up to $2,500 per violation.
- **Verification note:** statute number and general content confirmed via
  multiple independent secondary legal sources (IAPP, FindLaw, Pillsbury
  Law); a direct fetch of the primary statutory text at
  leginfo.legislature.ca.gov timed out twice during the 2026-08-05 research
  session. Re-fetch primary text before relying on exact statutory wording
  in a dispute.

**Sources:**
- Cal. Bus. & Prof. Code §§22575–22579: https://leginfo.legislature.ca.gov/faces/codes_displaySection.xhtml?lawCode=BPC&sectionNum=22575.
- FindLaw, Cal. Bus. & Prof. Code §22575: https://codes.findlaw.com/ca/business-and-professions-code/bpc-sect-22575/
- IAPP, "What Do the New Disclosure Requirements Under CalOPPA Mean for Your Business?": https://iapp.org/news/a/what-do-the-new-disclosure-requirements-under-caloppa-mean-for-your-busines
- Pillsbury Law, "California AG Issues New Privacy Policy and 'Do Not Track' Recommendations": https://www.pillsburylaw.com/en/news-and-insights/california-ag-issues-new-privacy-policy-and-do-not-track.html

**Date researched:** 2026-08-05.
**Volatility:** Low-moderate — statute itself is stable; re-check if a new
CA AG guidance document or amendment surfaces. Primary text unread in this
pass (see verification note) — treat as a gap to close before high-stakes
reliance.
**Related tasks:** Brew Me Up (Coffee Shop Tracker) Disclaimer/Privacy Policy
update, 2026-08-05 — see `proposals/nell-disclaimer-privacy-update-2026-08.md`
in that project.

---

### FTC Act Section 5 — Deceptive Privacy/Data-Handling Claims (USA, Federal)

**Jurisdictions:** USA, federal (15 U.S.C. §45).

**Key findings:**
- FTC Act §5 prohibits "unfair or deceptive acts or practices in or
  affecting commerce." The FTC's established enforcement position: **failing
  to adhere to the specific steps, standards, and promises made in a privacy
  notice is itself a deceptive practice**, independent of whether the
  underlying data handling was otherwise reasonable (e.g., an "appropriate
  safeguards" claim that didn't match actual practice was treated as
  deceptive in an FTC action against Blackbaud).
- The FTC has also brought standalone §5 **unfairness** claims (not just
  deception) over unreasonable data-retention practices and inaccurate
  breach notifications — a newer theory as of the sources reviewed.
- **Practical read:** an absolute, unqualified claim in a privacy policy
  (e.g., "deleted data cannot be recovered") that doesn't match a known,
  real (even if narrow) technical exception creates avoidable deception
  exposure. Advising a client to caveat such claims accurately, rather than
  overstate completeness, is a defensible, low-cost risk-reduction
  recommendation grounded in this enforcement pattern — not a requirement I
  can assert with "you must," since no specific violation has occurred
  absent a complaint/investigation.
- I verified this general principle via law-firm secondary sources
  summarizing FTC consent orders/actions, not by reading full consent-order
  text myself in this pass — treat specific case citations in those
  summaries as unread by me and re-verify before citing a specific matter by
  name.

**Sources:**
- 15 U.S.C. §45 (FTC Act, Section 5): https://www.ftc.gov/legal-library/browse/statutes/federal-trade-commission-act
- Perkins Coie, "FTC Brings First Standalone Section 5 Unfairness Claims for Unreasonable Data Retention and Inaccurate Breach Notice": https://perkinscoie.com/insights/update/ftc-brings-first-standalone-section-5-unfairness-claims-unreasonable-data-retention

**Date researched:** 2026-08-05.
**Volatility:** Low (statutory authority itself is stable) but enforcement
theory/posture shifts with FTC leadership and priorities — re-check current
enforcement focus before relying on this for a novel fact pattern.
**Related tasks:** Brew Me Up (Coffee Shop Tracker) Disclaimer/Privacy Policy
update, 2026-08-05 — see `proposals/nell-disclaimer-privacy-update-2026-08.md`
in that project.

---

### CCPA/CPRA — California Privacy (USA)

**Jurisdictions:** California; applies to any business (including out-of-state
iPhone app publishers) meeting the threshold and collecting CA residents' data.

**Key findings:**
- CCPA (effective 2020): California residents have rights to access, delete,
  opt-out of sale.
- CPRA (effective 2023): expanded rights, higher fines, new categories
  (sensitive personal information).
- Applies if business collects CA resident data and meets threshold (annual
  revenue >$25M, or collects data of 100,000+ residents/households, or derives
  revenue from selling data).
- Right to opt-out of "sale" (broad definition: includes marketing partners).
- Fines: up to $2,500 per violation, $7,500 per intentional violation.
- **Mobile-app-specific (2026 amendments to CCPA regulations):**
  - The app's privacy policy must be directly accessible inside the app
    itself (e.g., a settings-menu link), not only on a website.
  - The opt-out mechanism ("Do Not Sell or Share My Personal Information")
    must be reachable at or near the point personal information is collected,
    and from the homepage/app settings.
  - **Global Privacy Control (GPC):** businesses must honor GPC as a valid
    opt-out signal. As of 2026, silent processing is no longer sufficient —
    the business must display an explicit confirmation to the user that the
    opt-out was honored (e.g., a toggle or "Opt-Out Request Honored" message).
    For an iPhone app this typically means honoring GPC signals from any
    embedded/in-app browser and mirroring an equivalent in-app control.
  - As of January 1, 2026: any business that sells or shares personal
    information must conduct and document a **risk assessment** before that
    processing begins (benefits vs. risks to the consumer), producible to the
    CPPA on request.
  - Automated decision-making technology (ADMT) rules are also newly in force
    for 2026 — relevant if the app uses profiling/algorithmic decisions with
    legal or similarly significant effects; **re-verify current ADMT scope and
    effective dates before advising**, as CPPA rulemaking in this area has been
    contested and amended.

**Sources:**
- California Consumer Privacy Act: https://oag.ca.gov/privacy/ccpa
- CPRA Updates: https://oag.ca.gov/privacy/cpra
- CA DOJ, Global Privacy Control: https://oag.ca.gov/privacy/ccpa/gpc
- Butler Snow, "CCPA Regulations Amendments Effective January 1, 2026": https://www.butlersnow.com/news-and-events/ccpa-regulations-amendments-effective-january-1-2026-a-practical-roadmap-for-in-house-counsel

**Date researched:** 2026-07-17 (refreshed; original entry undated — treat
prior "will update" placeholder as superseded). **In-app-accessibility point
re-verified 2026-08-05**: confirmed via independent, more recent sources
(Osano, Greenberg Traurig, Butler Snow) that the CPPA finalized this
regulation package in September 2025, it took effect January 1, 2026, and
the requirement changed from "may" to "must" link the privacy policy from
the app's settings menu (in addition to the download page). No contrary
development found as of 2026-08-05.
**Volatility:** High (CPRA regs, GPC enforcement posture, and ADMT rules are
actively evolving; re-check before any CA-facing app release, especially
around January regulatory effective dates).
**Related tasks:** TASK-Nell-1 (deep-dive: iPhone apps in CA/FL, 2026-07-17);
Brew Me Up (Coffee Shop Tracker) Disclaimer/Privacy Policy update, 2026-08-05.

---

### California Invasion of Privacy Act (CIPA) — App/Website Tracking Wiretap Litigation

**Jurisdictions:** California (Cal. Penal Code §630 et seq.).

**Key findings:**
- CIPA is a criminal wiretap statute (with a civil private right of action,
  Penal Code §637.2) originally aimed at phone-call eavesdropping, now the
  basis of a fast-growing wave of civil litigation against companies whose
  websites and mobile apps use analytics/tracking pixels, session-replay
  tools, chatbots, and similar technologies.
- Core theory: these tools "intercept" electronic communications between the
  user and the site/app and route them to a third party (analytics vendor,
  ad-tech company) **before** the user has given consent via a cookie/consent
  banner — plaintiffs argue consent must precede any interception, not follow
  it.
- Litigation is active and evolving rapidly: a $3.85M class settlement against
  the Los Angeles Times was approved June 26, 2026, targeting three specific
  trackers (TripleLift, GumGum, Audiencerate) used on its website **and mobile
  apps** — confirms CIPA theories are being applied to native apps, not just
  websites.
- Legislative reform is in motion: as of July 1, 2026, the CA Assembly's
  Privacy and Consumer Protection Committee was hearing amended language for
  **SB 690**, aimed at narrowing/clarifying CIPA's application to ordinary
  analytics — status unresolved as of this research date; re-check before
  advising on litigation risk exposure.
- Practical implication for an iPhone app: any third-party SDK that captures
  in-app user interaction data (analytics, crash/session replay, chat widgets,
  ad SDKs) before the user has affirmatively consented is a plausible CIPA
  target under current case theories, independent of CCPA/CPRA compliance.

**Sources:**
- Loeb & Loeb, "The Millisecond Problem: How Pre-Consent Tracking Is Driving
  CIPA Lawsuits in 2026" (2026-04): https://www.loeb.com/en/insights/publications/2026/04/the-millisecond-problem-how-pre-consent-tracking-is-driving-cipa-lawsuits-in-2026
- Spencer Fane, "CIPA Website Tracking Lawsuits: Where the Law Stands, Where
  It's Going": https://www.spencerfane.com/insight/cipa-website-tracking-lawsuits-where-the-law-stands-where-its-going-and-what-your-business-should-do-now/
- ConsentPixel, "CIPA Lawsuit Tracker 2026": https://consentpixel.com/blogs/cipa-lawsuit-tracker-2026-every-website-wiretapping-case/
- Termly, "Understanding California's Wiretapping Claims Against Website
  Tracking": https://termly.io/resources/articles/california-wiretapping-claims-against-website-tracking/

**Date researched:** 2026-07-17.
**Volatility:** Very high — active litigation wave, contested legal theory,
and pending legislative amendment (SB 690) that could narrow the statute's
reach. Re-verify immediately before advising on any specific SDK/tracking
implementation; do not treat this entry as settled law.
**Related tasks:** TASK-Nell-1 (deep-dive: iPhone apps in CA/FL, 2026-07-17)

---

### California Automatic Renewal Law (CARL) — Subscription Apps

**Jurisdictions:** California (Bus. & Prof. Code §17600 et seq.).

**Key findings:**
- Original SB 313 (2018, effective July 1, 2018): automatic-renewal or
  continuous-service offers (including free trials/gifts) must clearly and
  conspicuously disclose the post-trial price or pricing-change mechanics;
  card/account authorization for a free/reduced offer must go through a
  separate stand-alone acknowledgment; business must give notice 3–7 days
  before the first auto-renewal charge (for offers of a year or longer, per
  the statute's notice provisions); cancellation must be **at least as easy**
  as sign-up.
- **2024 amendment, AB 2863 (Schiavo)**, signed 2024-09-24: expands CARL to
  cover free-to-pay conversions explicitly, and imposes requirements similar
  to — but on the whole more burdensome than — the FTC's "click-to-cancel"
  final rule. Applies to contracts entered into, amended, or extended on or
  after **July 1, 2025**.
- Under the 2025 amendments, businesses must obtain the consumer's **"express
  affirmative consent"** to the auto-renewal/continuous-service terms
  specifically (not bundled into general terms acceptance).
- Directly relevant to any iPhone app selling subscriptions: even though
  Apple's own In-App Purchase system handles the billing/cancellation
  mechanics for IAP-based subscriptions, the **offer presentation and
  disclosure** (trial terms, pricing-change notices, consent flow) inside the
  app's own UI is squarely within CARL's scope and is a distinct legal
  question from Apple's App Store Guidelines.

**Sources:**
- CA Legislative Info, SB-313 bill text: https://leginfo.legislature.ca.gov/faces/billNavClient.xhtml?bill_id=201720180SB313
- CA Legislative Info, AB-2863 bill text: https://leginfo.legislature.ca.gov/faces/billTextClient.xhtml?bill_id=202320240AB2863
- Davis Wright Tremaine, "Click To Cancel: California Updates Automatic
  Renewal Law, Echoing FTC's Proposed Negative Option Rule": https://www.dwt.com/insights/2024/10/ab-2863-updates-california-automatic-renewal-law
- CA Attorney General Bonta, Consumer Alert on CARL: https://oag.ca.gov/news/press-releases/attorney-general-bonta-issues-consumer-alert-california%E2%80%99s-automatic-renewal-law

**Date researched:** 2026-07-17.
**Volatility:** Moderate-high — AB 2863's expanded requirements only took
effect 2025-07-01; enforcement posture and interpretation are still fresh.
Re-verify before advising on any new subscription flow.
**Related tasks:** TASK-Nell-1 (deep-dive: iPhone apps in CA/FL, 2026-07-17)

---

### California Age-Appropriate Design Code Act (CAADCA / AB 2273)

**Jurisdictions:** California.

**Key findings:**
- CAADCA imposes design and data-use obligations on online services "likely
  to be accessed by children," including age estimation/verification,
  restrictions on data use, and a ban on "dark patterns."
- **Currently subject to a partial injunction** in ongoing First Amendment
  litigation, *NetChoice, LLC v. Bonta* (N.D. Cal.; 9th Cir. No. 25-2366).
- On 2026-03-12, the Ninth Circuit ruled on appeal: of six substantive
  provisions NetChoice challenged, the court **affirmed the injunction** as to
  the act's **data-use restrictions** and its **dark-patterns prohibition**
  (both found likely unconstitutionally vague), but **vacated the injunction**
  as to the act's **coverage definition** and its **age-estimation
  requirement** — finding NetChoice unlikely to succeed on a facial challenge
  to age estimation, since a business can comply by defaulting to
  child-protective settings for all users rather than a content-based
  restriction.
- Case remanded to the N.D. Cal. district court for further proceedings on
  age estimation and severability — **the injunction's exact scope is
  actively moving; do not rely on this summary for a compliance deadline
  without re-checking current docket status.**
- Practical read for an iPhone app likely to be accessed by minors in
  California: age-estimation/default-protective-settings obligations may
  currently be enforceable, while specific data-use and dark-pattern
  provisions remain blocked — but this is genuinely unsettled and outcome-
  determinative facts (what the app is, who accesses it) matter.

**Sources:**
- Ninth Circuit opinion, *NetChoice, LLC v. Bonta*, No. 25-2366 (2026-03-12):
  https://cdn.ca9.uscourts.gov/datastore/opinions/2026/03/12/25-2366.pdf
- Justia case page: https://law.justia.com/cases/federal/appellate-courts/ca9/25-2366/25-2366-2026-03-12.html
- Holland & Knight, "Ninth Circuit Issues Mixed Ruling on California
  Age-Appropriate Design Code Act": https://www.hklaw.com/en/insights/publications/2026/03/ninth-circuit-issues-mixed-ruling-on-california-age-appropriate-design
- Cooley, "NetChoice v. Bonta: Ninth Circuit Narrows Injunction": https://www.cooley.com/news/insight/2026/2026-03-30-netchoice-v-bonta-ninth-circuit-narrows-injunction-against-californias-ageappropriate-design-code-act
- NetChoice case tracker: https://netchoice.org/netchoice-v-bonta/

**Date researched:** 2026-07-17.
**Volatility:** Very high — actively litigated, partially enjoined, remanded;
this is a moving target and must be re-verified immediately before any advice
that depends on CAADCA's current enforceable scope.
**Related tasks:** TASK-Nell-1 (deep-dive: iPhone apps in CA/FL, 2026-07-17)

---

### Florida Digital Bill of Rights (FDBR / SB 262)

**Jurisdictions:** Florida.

**Key findings:**
- Effective **July 1, 2024**.
- Applies only to entities meeting the statutory "controller" definition: a
  for-profit entity conducting business in Florida or targeting Florida
  residents, that determines the purposes/means of processing personal data,
  **and** has **global annual revenue over $1 billion**, **and** meets at
  least one of: (a) derives 50%+ of global gross revenue from online
  advertising (including targeted advertising), (b) operates a
  smart-speaker/voice-assistant service with hands-free activation, or (c)
  operates an app store or digital distribution platform with at least
  250,000 different apps available for download.
- **Practical scope note:** because of the $1B+ global revenue threshold
  combined with the additional criteria, the FDBR applies to a small number of
  very large platform/advertising companies — most individual iPhone app
  publishers will **not** be a "controller" under FDBR, though a publisher
  could still be indirectly affected if it operates within a covered app
  store's ecosystem or as a processor for a covered controller. Verify actual
  revenue/business-model facts before concluding FDBR does or doesn't apply —
  do not default-assume exemption without checking the client's numbers.
- Exemptions include state government, nonprofits, HIPAA-covered entities,
  higher-education institutions, GLBA-regulated entities, and certain data
  types (health records, FERPA-covered data, employment data, payment-
  processing data, etc.).
- Controllers must respond to consumer rights requests within 45 days
  (extendable by 15 days for complex/numerous requests).

**Sources:**
- Florida Senate, SB 262 enrolled bill text: https://www.flsenate.gov/Session/Bill/2023/262/BillText/er/HTML
- Burr & Forman, "Florida Digital Bill of Rights (FDBR): Key Requirements and
  Compliance Steps": https://www.burr.com/newsroom/articles/floridas-digital-bill-of-rights-a-summary-of-key-points-for-large-online-platforms
- White & Case, "Florida Enacts the Digital Bill of Rights": https://www.whitecase.com/insight-alert/florida-enacts-digital-bill-rights-joining-growing-privacy-landscape
- Greenberg Traurig, "A Detailed Overview of Florida SB 262": https://www.gtlaw.com/en/insights/2023/6/detailed-overview-florida-sb-262-new-data-privacy-protections-for-florida-residents

**Date researched:** 2026-07-17.
**Volatility:** Moderate — law is relatively new (effective mid-2024);
thresholds and exemptions are statutory rather than regulatory, so more
stable than CCPA-style agency rulemaking, but confirm current revenue
thresholds haven't been amended before relying on an exemption analysis.
**Related tasks:** TASK-Nell-1 (deep-dive: iPhone apps in CA/FL, 2026-07-17)

---

### Florida Telephone Solicitation Act (FTSA)

**Jurisdictions:** Florida (Fla. Stat. §501.059).

**Key findings:**
- Enacted 1987, predating the federal TCPA (1991); requires consent for
  autodialed calls/texts and provides a **private right of action** for
  Florida residents who receive unwanted telephone solicitations/texts.
- 2021 amendments allowed successful plaintiffs to obtain injunctive relief,
  statutory damages per violation, and **treble damages** for willful/knowing
  violations — this triggered a wave of individual and class-action lawsuits
  against companies using SMS/text marketing.
- **2023 amendment (H.B. 761, signed 2023-05-25)** added guardrails: before
  filing an FTSA damages lawsuit, a would-be plaintiff must first reply
  "STOP" to the specific number and affirmatively notify the sender they don't
  want further texts; the sender then has a **15-day grace period** to comply
  before liability attaches.
- Relevant to an iPhone app if it sends **SMS/text messages** (not push
  notifications through Apple's APNs, which are a different technical channel
  not confirmed as within FTSA's scope in the sources reviewed) for marketing,
  reminders, or 2FA-adjacent messaging without proper consent capture — verify
  the app's actual messaging channel (SMS vs. in-app push) before concluding
  FTSA applies, since this research pass did not find authoritative confirmation
  that push notifications are treated as "telephone solicitation" under the Act.

**Sources:**
- Florida Bar Journal, "Putting Pandora Back in the Box: The Florida
  Telephone Solicitation Act": https://www.floridabar.org/the-florida-bar-journal/putting-pandora-back-in-the-box-the-florida-telephone-solicitation-act/
- Morrison Foerster, "Uptick in Florida Telephone Solicitation Act
  Litigation": https://www.mofo.com/resources/insights/241111-uptick-in-florida-telephone-solicitation-act-litigation
- Steptoe, "Do You Believe in Miracles? Yes! Florida Legislature Amends the
  FTSA": https://www.steptoe.com/en/news-publications/do-you-believe-in-miracles-yes-florida-legislature-amends-the-florida-telephone-solicitation-act.html
- Bradley, "Navigating Claims Under the FTSA and Florida Telemarketing Act": https://www.bradley.com/insights/publications/2024/11/navigating-claims-under-the-florida-telephone-solicitation-act-and-florida-telemarketing-act

**Date researched:** 2026-07-17.
**Volatility:** Moderate — statute itself is stable post-2023 amendment, but
litigation volume/theories continue to shift; the push-notification question
above is an open gap, not a settled finding — flag as unverified if asked.
**Related tasks:** TASK-Nell-1 (deep-dive: iPhone apps in CA/FL, 2026-07-17)

---

### Florida Security of Communications Act (FSCA) — App/Website Wiretap Litigation

**Jurisdictions:** Florida (Fla. Stat. §934.01 et seq.) — Florida's analog to
California's CIPA.

**Key findings:**
- Unlike the federal Wiretap Act (one-party consent), the FSCA requires
  **all-party consent** before a wire, oral, or electronic communication is
  intercepted — a stricter standard that plaintiffs are using against tracking
  pixels, session-replay tools, and analytics on websites and in patient/
  customer-facing apps.
- Since 2021, over two dozen lawsuits have been filed in Florida courts
  against companies using tools that track clicks, scrolls, and keystrokes
  without explicit consent.
- **Key 2025 ruling:** *W.W. v. Orlando Health, Inc.* — plaintiff alleged
  Orlando Health installed Meta and Google tracking pixels on its patient
  portal without consent; the court (March 2025) **denied Orlando Health's
  motion to dismiss** the FSCA claim, holding the plaintiff adequately alleged
  the tracked data was "contents" of a communication under the statute. This
  reversed the earlier trend of courts dismissing FSCA claims against
  session-replay/cookie tools for not capturing statutory "contents."
    - Verify current docket status/final disposition before citing as
      settled — this was a motion-to-dismiss ruling, not a final merits
      judgment, as of the sources reviewed.
- Statutory damages start at **$1,000 per violation**; the statute also has a
  criminal dimension (felony exposure) which raises the stakes of a finding of
  liability beyond typical civil privacy statutes.

**Sources:**
- Sidley, "Florida Federal Court Puts Florida's Security of Communications
  Act in Play" (2025-03-19): https://datamatters.sidley.com/2025/03/19/florida-federal-court-puts-floridas-security-of-communications-act-in-play-in-the-ongoing-wave-of-website-privacy-class-actions/
- Fisher Phillips, "Is Florida the New Hotbed for Digital Wiretapping
  Lawsuits?": https://www.fisherphillips.com/en/insights/insights/is-florida-the-new-hotbed-for-digital-wiretapping-lawsuits
- Captain Compliance, "Florida's Wiretapping Law Under Fire: The FSCA and
  Data Privacy Litigation": https://captaincompliance.com/education/floridas-wiretapping-law-under-fire-the-fsca-and-data-privacy-litigation/
- Online and On Point, "From Convenience to Courtroom: Florida's Expanding
  Website 'Wiretapping' Litigation Risk" (2026-02): https://www.onlineandonpoint.com/2026/02/from-convenience-to-courtroom-floridas-expanding-website-wiretapping-litigation-risk/

**Date researched:** 2026-07-17.
**Volatility:** Very high — active, fast-moving litigation trend with a
pivotal 2025 ruling; treat as unsettled and re-verify before advising on SDK/
tracking risk for any FL-facing app, especially in regulated/sensitive
contexts (health, finance).
**Related tasks:** TASK-Nell-1 (deep-dive: iPhone apps in CA/FL, 2026-07-17)

---

### Florida HB 3 — Online Protections for Minors

**Jurisdictions:** Florida.

**Key findings:**
- Signed into law 2024-03-25; took effect **January 1, 2025**.
- Bars minors under 14 from opening accounts on covered social media
  platforms (defined by "addictive features"); 14- and 15-year-olds may have
  accounts only with **verified parental/guardian consent**.
- Requires anonymous or standard age verification for access to material
  "harmful to minors" (e.g., pornographic/sexually explicit content).
- **Enforcement has been contested and is currently in flux:**
  - 2025-06-03: Chief U.S. District Judge Mark Walker issued a **preliminary
    injunction** blocking enforcement, on First Amendment grounds.
  - Late November 2025: the **Eleventh Circuit lifted the injunction**,
    allowing Florida to enforce HB 3 while the appeal continues.
  - Following that ruling, Florida AG James Uthmeier gave platforms 30 days
    to implement age restrictions and 60 days to stand up parental-consent
    systems, warning of enforcement action against noncompliant companies.
  - As of early 2026, the merits appeal was heading to oral argument before
    the Eleventh Circuit; further Supreme Court review is plausible.
- Directly relevant to any iPhone app with social/UGC features that could be
  "accessed by" Florida minors — but **current enforceability is a live,
  moving legal question, not settled law**; confirm the litigation's current
  posture before advising on compliance deadlines.

**Sources:**
- Privo, "What is Florida's HB 3 Act? Requirements & Compliance Overview": https://www.privo.com/blog/what-is-floridas-hb-3-act-online-protection-for-minors
- Wilson Sonsini, "State Social Media Law Patchwork Emerging: Florida Passes
  Law to Restrict Minors' Use of Online Services": https://www.wsgr.com/en/insights/state-social-media-law-patchwork-emerging-florida-passes-law-to-restrict-minors-use-of-online-services.html
- CCIA, "CCIA Files Brief to Court of Appeals on Florida's Social Media Age
  Verification Law" (2025-09): https://ccianet.org/news/2025/09/ccia-files-brief-to-court-of-appeals-on-floridas-social-media-age-verification-law/
- Harvard Law Review, recent legislation note on Florida HB 3 (First
  Amendment analysis): https://harvardlawreview.org/wp-content/uploads/2025/01/138-Harv.-L.-Rev.-1161.pdf

**Date researched:** 2026-07-17.
**Volatility:** Very high — actively litigated, injunction status has
flipped once already (enjoined, then unenjoined on appeal); re-verify
immediately before advising on any specific compliance deadline or
enforceability assumption.
**Related tasks:** TASK-Nell-1 (deep-dive: iPhone apps in CA/FL, 2026-07-17)

---

### Florida Deceptive and Unfair Trade Practices Act (FDUTPA)

**Jurisdictions:** Florida (Fla. Stat. §§501.201–501.213).

**Key findings:**
- Broad consumer-protection statute prohibiting "unfair methods of
  competition" and "unfair or deceptive acts or practices" in trade or
  commerce; covers virtually all commercial transactions involving goods,
  services, or property — mobile apps as a commercial service offering fall
  within this scope.
- Protects both individual consumers and businesses; provides a private right
  of action as well as state AG enforcement.
- **Relevant recent federal backdrop:** the FTC's "click-to-cancel" rule
  (finalized late 2024, enforcement beginning 2025) requires that canceling a
  subscription be at least as easy as signing up, bars burying cancellation
  behind phone calls/chatbots when sign-up was online, and requires specific
  advance disclosures for free trials that auto-convert to paid plans.
  - Note: the FTC's click-to-cancel rule's own procedural history has been
    contested at the federal level in 2025; confirm current federal
    enforcement status separately from the state-law FDUTPA analysis before
    advising, since the two operate on independent legal tracks.
- Practical read: a Florida-facing app that enrolls users in recurring
  billing without clear disclosure, makes cancellation unreasonably difficult,
  or uses confusing/dark-pattern UI to obtain consent risks both FTC
  enforcement (federal) and a FDUTPA claim (state) — hidden fees and
  non-disclosed auto-renewal are the most commonly cited fact patterns.

**Sources:**
- Florida Statutes §501.204: https://www.leg.state.fl.us/statutes/index.cfm?App_mode=Display_Statute&URL=0500-0599%2F0501%2FSections%2F0501.204.html
- Jimerson Birr, "Florida Deceptive and Unfair Trade Practices Act (FDUTPA)": https://www.jimersonfirm.com/services/bet-company-litigation/florida-deceptive-unfair-trade-practices-act-fdutpa/
- LegalClarity, "Florida Unfair Trade Practices Act: What FDUTPA Covers": https://legalclarity.org/which-unfair-trade-practices-act-applies-in-florida/

**Date researched:** 2026-07-17.
**Volatility:** Moderate — the statute itself is stable, but the federal
click-to-cancel-rule backdrop it's often analyzed alongside is contested;
re-verify the FTC rule's status separately before combining the two in advice.
**Related tasks:** TASK-Nell-1 (deep-dive: iPhone apps in CA/FL, 2026-07-17)

---

(Additional topics will be added as Nell researches: Trademark, Patent Prior Art,
App Store Rejection Appeals, Gambling Regulation, Health Claims Regulation,
Export Controls, Tax/VAT, NDA Best Practices, EU Digital Markets Act as it
affects iOS payment/distribution rules, etc. COPPA, CalOPPA, and FTC Act
§5 deceptive-practices theory were added 2026-08-05.)

---

## Notes

- This repository is maintained by Nell and updated after each research task.
- Entries are **never** exhaustive — they are leads for quick reference.
- **Always** verify current law before advising a project; do not rely on
  outdated entries.
- Sources are cited with URLs and dates; if a source link breaks, consider the
  entry stale and re-research.
