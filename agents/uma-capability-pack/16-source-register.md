# 16 — Source Register
Verified via web research on 2026-07-12 unless marked [training-knowledge —
verify before load-bearing use]. Record format: ID · source · date · why cited.

- **S1** W3C, *Web Content Accessibility Guidelines (WCAG) 2.2* —
  https://www.w3.org/TR/WCAG22/ — W3C Recommendation 2023-10-05, editorial
  update 2024-12-12. Normative basis for all web accessibility findings.
- **S2** W3C WAI, *What's New in WCAG 2.2* —
  https://www.w3.org/WAI/standards-guidelines/wcag/new-in-22/ — the nine new
  SCs; 4.1.1 removal. Also *WCAG 2 Overview*
  (https://www.w3.org/WAI/standards-guidelines/wcag/): 2.2 as recommended
  target; ISO/IEC 40500:2025 adoption (2025-10-21).
- **S3** W3C, *WCAG2ICT* — https://www.w3.org/TR/wcag2ict-22/ — applying WCAG
  to non-web software (used for the native app) [training-knowledge — verify
  current draft status].
- **S4** W3C WAI, *ARIA Authoring Practices Guide (APG)* —
  https://www.w3.org/WAI/ARIA/apg/ — canonical custom-widget patterns
  [training-knowledge, stable].
- **S5** Nielsen Norman Group, *10 Usability Heuristics for User Interface
  Design* — https://www.nngroup.com/articles/ten-usability-heuristics/ —
  1994, last major update 2020s [training-knowledge, stable].
- **S6** Nielsen Norman Group, *Severity Ratings for Usability Problems* —
  https://www.nngroup.com/articles/how-to-rate-the-severity-of-usability-problems/
  [training-knowledge, stable].
- **S7** ISO, *ISO 9241-210:2019 Human-centred design for interactive systems*
  — https://www.iso.org/standard/77520.html — 2019 [training-knowledge, stable].
- **S8** Apple, *Human Interface Guidelines* —
  https://developer.apple.com/design/human-interface-guidelines/ — living
  document; verify page revision at use time. 44×44 pt target guidance.
- **S9** Apple Developer, *What's New in SwiftUI (WWDC26 session 269)* —
  https://developer.apple.com/videos/play/wwdc2026/269/ — and *SwiftUI
  What's New* (https://developer.apple.com/swiftui/whats-new/) — 2026-06 —
  2027-line APIs: toolbar visibilityPriority/overflow/pinned/minimize, new
  Document protocol, reorderable containers, AsyncImage caching, @State macro.
- **S10** TechTimes (secondary), *Apple Liquid Glass iOS 27: WWDC 2026
  refinements* — 2026-06-08 — iOS 26 Liquid Glass contrast criticism (NN/g),
  transparency slider, UIGlassEffect/glassEffect() sync caveat. Secondary
  source; prefer Apple docs for load-bearing API claims.
- **S11** Use Your Loaf, *WWDC 2026 Viewing Guide* — 2026-06 — session-level
  summary incl. UIKit modernization (UIScene required, no UIScreen.main).
  Secondary; corroborates S9.
- **S12** Apple, *XCTest performAccessibilityAudit* (Xcode 15+, WWDC23
  "Perform accessibility audits for your app") —
  https://developer.apple.com/documentation/xctest — [training-knowledge,
  stable API; verify current options].
- **S13** OWASP, *OWASP Top 10:2025* — https://owasp.org/Top10/2025/en/ —
  announced 2025-11 (Global AppSec DC), final released 2026-01. New: A03
  Software Supply Chain Failures, A10 Mishandling of Exceptional Conditions;
  SSRF folded into A01.
- **S14** GitHub Docs, *About protected branches* / *About pull request
  reviews* / *About code owners* — https://docs.github.com/ —
  living documents [training-knowledge, stable concepts].

**Disagreements noted:** secondary sources differ on how fully iOS 27's slider
resolves Liquid Glass contrast complaints (S10 vs S11 tone) — treat as
unresolved until GA testing. **Fast-decay knowledge:** everything in S9–S11
(beta APIs may change before ~Sept 2026 GA); review_by 2026-10-12.
