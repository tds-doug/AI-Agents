# 05 — Role Knowledge Guide
Applied knowledge for Uma's daily work. Each section: concepts → how to apply →
failure modes → validation → escalation triggers → references (full citations
in §16). Knowledge is tagged:
**[STABLE]** foundational · **[VERSIONED]** tied to a platform release ·
**[CURRENT]** best practice as of 2026-07 · **[CONTESTED]** context-dependent ·
**[DEPRECATED]** do not recommend.

---
## 05.1 The review mindset [STABLE]
A UI review is an **argument from evidence**, not a taste exercise. Every
finding must answer: *What is wrong, for whom, how do we know, how bad is it,
what fixes it, and what does the fix cost?* If any answer is missing, the
finding is not done. ISO 9241-210 frames this: design decisions should be
driven by user needs and evaluated against them, iteratively [S7].

**Failure mode:** vibes-based critique ("feels cluttered"). **Fix:** anchor to a
heuristic, standard, or measurable property (tap-target px, contrast ratio,
step count, time-to-first-action).

## 05.2 Evidence tiers and severity [STABLE]
Label every finding with the strongest tier that actually applies:
- **T1 Standard violation** — testable breach of WCAG 2.2 or an explicit HIG
  requirement (e.g., contrast 2.9:1 < 4.5:1). Objective; cite the criterion.
- **T2 Heuristic violation** — breach of an established heuristic (NN/g 10
  [S5], platform conventions) with a described user impact.
- **T3 Informed inference** — pattern known to cause problems, but impact here
  is inferred. Must be labeled "inference"; candidate for user validation.
- **T4 Opinion/preference** — allowed, but labeled and never rated Critical.

Severity (adapted from NN/g severity ratings [S6]):
**S0 Blocker** — prevents task completion or is a T1 violation on a core flow.
**S1 Major** — significant friction/exclusion; workaround exists but costly.
**S2 Minor** — irritant; cosmetic-plus. **S3 Polish** — nice-to-have.
Rule: severity may not exceed what the evidence tier supports; a T4 caps at S2.
Impact scope multiplies: (all users / subset / edge case) × (core / secondary
flow). Record both.

**Failure modes:** inflating T3→T1; rating on annoyance-to-Uma rather than
user impact. **Validation:** a second agent (or the human) should be able to
reproduce the finding from the evidence alone.

## 05.3 Apple platform: SwiftUI + HIG
### 05.3.1 Baseline [VERSIONED — verify against current docs before citing]
As of July 2026: shipping OS generation is the 2026 line (iOS/iPadOS/macOS 26,
"Liquid Glass" design language, WWDC 2025). WWDC 2026 (June 8–12, 2026)
announced the 2027 releases (iOS 27 etc., betas since June 8; public release
expected ~Sept 2026) with a refined Liquid Glass, a user-facing transparency
slider, new toolbar APIs (`visibilityPriority`, `toolbarOverflowMenu`,
`topBarPinnedTrailing`, `toolbarMinimizeBehavior`), a new SwiftUI Document API,
reorderable containers, AsyncImage HTTP caching, `@State` as a macro (lazy
init of @Observable classes), and resizable iPhone apps [S9][S10][S11].
**Operating rule:** before asserting any API/HIG detail, check whether it is
26-line (shipping) or 27-line (beta) and say which. Recommendations for
production apps target the shipping line unless the task says otherwise.

### 05.3.2 HIG essentials Uma applies constantly [STABLE core, details versioned]
- **Clarity of hierarchy:** one primary action per screen; system typography
  (Dynamic Type styles, not fixed point sizes).
- **Touch targets:** ≥ 44×44 pt per HIG [S8]; note WCAG 2.2's separate 24×24
  CSS-px minimum for web (SC 2.5.8) [S1].
- **Navigation:** prefer standard `NavigationStack`/`TabView` patterns;
  nonstandard navigation is a finding unless justified.
- **State communication:** loading, empty, error, and success states must all
  exist; missing empty/error states are among the most common findings.
- **Dynamic Type & truncation:** review at largest accessibility sizes;
  clipped labels at AX5 = S1 accessibility finding.
- **Dark Mode & Increased Contrast:** review in all appearance modes.

### 05.3.3 SwiftUI accessibility review protocol [CURRENT]
1. Automated: run XCUITest `performAccessibilityAudit()` (Xcode 15+) on key
   screens [S12]; attach the test output.
2. Inspect: Accessibility Inspector pass per screen (labels, traits, hints,
   contrast warnings).
3. Manual: VoiceOver walk of each core flow — reading order, rotor
   navigation, custom-control actions; Dynamic Type at AX sizes; Reduce
   Motion/Transparency behavior.
4. Code spot-check: `accessibilityLabel/Value/Hint`, `accessibilityElement
   (children: .combine)` for composite views, `accessibilityAddTraits`.
Automated audits catch a minority of issues; never report "accessible" from
automation alone — say what each method covered.

### 05.3.4 Running the iOS Simulator for review work [STABLE]
When reviewing SwiftUI apps, build and run them in the iOS Simulator to
observe actual UI behavior. This is part of your evidence capture; screenshots
from the Simulator are primary evidence (more reliable than code review alone).

### Setup
1. Ensure Xcode is installed and the project builds locally.
2. Confirm the Simulator runtime matches or exceeds the project's minimum iOS
   (e.g., iOS 18 for your projects).
3. Open the `.xcodeproj` or `.xcworkspace`; select a Simulator as the build
   target (e.g., "iPhone 15 Pro Simulator").

### Build & run procedure
```bash
# Command-line build (optional, if you prefer)
xcodebuild -scheme <SchemeName> -configuration Debug -sdk iphonesimulator
# Then launch the app in Simulator (or use Xcode's Run button)
```

**What you may do:**
- Build the project as-is (no code changes)
- Run it in the Simulator
- Capture screenshots, screen recordings, and accessibility audit outputs
- Interact with the app to observe UI states and behaviors

**What you may NOT do:**
- Modify source code, SwiftUI components, or build settings
- Change provisioning profiles, certificates, or signing configuration
- Deploy to real devices or Simulators on other machines
- Commit any changes (you're read-only on the codebase)

### Evidence capture best practices
Every screenshot/recording:
- **Name:** `<screen>-<state>-<device>-<date>.png`
  - Example: `login-success-iphone15pro-2026-07-16.png`
- **Metadata:** Include in your report or filename:
  - iOS version (e.g., iOS 18)
  - Device/Simulator (e.g., "iPhone 15 Pro")
  - Build date/commit SHA
  - App version (if versioned)
- **Storage:** Save all evidence to `evidence/<task-id>/` with clear organization

### Common issues & troubleshooting
| Problem | Action |
|---|---|
| Xcode won't build | Stop; report the build error to DJ. Never continue without a successful build. |
| Simulator won't launch the app | Check that you selected a Simulator (not "My Mac"), and that the build succeeded. |
| Screenshots are blurry or unreadable | Use native Simulator screenshot (Cmd+S) or Video recording; avoid third-party tools. |
| Can't run Accessibility Inspector | Make sure Accessibility Inspector is installed (Xcode → Open Developer Tool → Accessibility Inspector). |
| Build takes > 5 min | That's normal for first build. Subsequent builds are faster. If stuck, ask DJ. |

### Workflow: building for evidence
1. Receive task with a screen to review.
2. Ensure project is up-to-date: `git pull origin <branch>` (DJ tells you which).
3. Open Xcode; select a Simulator target (e.g., iPhone 15 Pro, iOS 18).
4. Build: Cmd+B; then Run: Cmd+R (or use Xcode Run button).
5. Wait for app to launch in Simulator.
6. Interact with app to reach the screen in scope (navigate, enter data, etc.).
7. Capture screenshot (Cmd+S in Simulator, or use Accessibility Inspector).
8. Name and save to `evidence/<task-id>/<screen>-<state>-device-date.png`.
9. Continue to next screen or state (loading, error, empty, etc.).
10. Log every finding immediately with evidence path.

### Version awareness
iOS 18 is your current min. If a future iOS releases a breaking UI change, you
may need to test on multiple Simulator versions. Ask DJ if it's worth the build
time; if so, you can select different Simulators for different OS versions
(one at a time; Simulator can't run multiple OS versions simultaneously for
your purposes).

### 05.3.5 Liquid Glass–specific pitfalls [VERSIONED][CONTESTED]
Documented criticism (incl. NN/g) of first-gen Liquid Glass: translucent
elements over busy content can drop text contrast below readable thresholds;
Reduce Transparency only partially compensates on iOS 26 [S10]. iOS 27 adds a
user transparency slider and refinements [S9][S10]. Review implications:
- Test glass surfaces over worst-case backgrounds (photos, video, dense lists).
- Contrast findings on glass are T1 if measurable below 4.5:1 for body text.
- Do not recommend heavy custom workarounds that iOS 27's slider may obsolete;
  flag as version-dependent and present both paths [CONTESTED].
- Mixed UIKit/SwiftUI apps: `UIGlassEffect` and `.glassEffect()` don't auto-
  synchronize visual identity; check `GlassEffectContainer` boundaries [S10].

### 05.3.6 Deprecated / do-not-recommend [DEPRECATED]
Fixed point sizes instead of Dynamic Type; `NavigationView` for new code
(superseded by `NavigationStack`, iOS 16+); hardcoded colors instead of
semantic/asset-catalog colors; `UIScreen.main` and orientation-based layout
decisions (called out again at WWDC26 as unsupported patterns in resizable
environments [S11]); disabling system accessibility behaviors.

## 05.4 WCAG 2.2 applied [STABLE spec, CURRENT status]
Status: W3C Recommendation 2023-10-05, editorial update 2024-12-12; also
ISO/IEC 40500:2025. W3C recommends 2.2 as the conformance target; 4.1.1
Parsing is removed [S1][S2]. Target: **Level AA**.
Organize reviews by POUR; the nine 2.2-new criteria deserve explicit checks
because tooling coverage is weak [S2]:
| SC | Level | Uma's concrete test |
|---|---|---|
| 2.4.11 Focus Not Obscured (Min) | AA | Tab through page with banners/stickies open; focused element ≥ partially visible |
| 2.4.12 Focus Not Obscured (Enh) | AAA | fully visible (report as advisory) |
| 2.4.13 Focus Appearance | AAA | advisory: focus indicator size/contrast |
| 2.5.7 Dragging Movements | AA | every drag interaction has a single-pointer alternative |
| 2.5.8 Target Size (Minimum) | AA | interactive targets ≥ 24×24 CSS px or adequately spaced |
| 3.2.6 Consistent Help | A | help mechanism in same relative place across pages |
| 3.3.7 Redundant Entry | A | previously entered info auto-filled or selectable within a process |
| 3.3.8 Accessible Authentication (Min) | AA | no cognitive test to log in without alternative; never block paste/password managers |
| 3.3.9 Accessible Authentication (Enh) | AAA | advisory |
Plus the perennials: 1.4.3 contrast 4.5:1 (3:1 large text), 1.4.11 non-text
contrast 3:1, 2.1.1 keyboard, 4.1.2 name/role/value, 1.3.1 info-and-
relationships (semantic HTML/headings/labels).
**Method:** automated scan (axe-core/Lighthouse) ➜ manual keyboard-only pass ➜
screen-reader pass ➜ zoom/reflow at 400%. Report which SCs were tested by
which method; automation typically covers well under half of SCs — never claim
conformance from a scan [CURRENT].
For the native app, apply WCAG2ICT mappings pragmatically; HIG accessibility
guidance governs where WCAG doesn't translate [S3].

## 05.5 Web UI specifics [STABLE]
Semantic HTML first; ARIA only when semantics can't do it ("no ARIA is better
than bad ARIA" — WAI-ARIA APG [S4]). Custom widgets must match an APG pattern
(roles, states, keyboard interaction) or be flagged. Check responsive behavior
at 320 px width (SC 1.4.10 reflow), visible focus styles (never
`outline: none` without replacement), form labels programmatically associated,
and error messages announced (aria-live or focus management).

## 05.6 Security-relevant UX [CURRENT]
Uma's remit intersects OWASP Top 10:2025 (final released Jan 2026 [S13]) at:
- **Authentication UX:** login/reset flows must not enable user enumeration
  ("email not found" vs. uniform messaging); never recommend blocking paste,
  password managers, or autofill (also a WCAG 3.3.8 issue); MFA prompts must
  be phishing-resistant in wording (no "enter this code anywhere" ambiguity).
- **Error handling & messaging (A10:2025 Mishandling of Exceptional
  Conditions):** UI must fail closed with honest, non-leaking errors — no stack
  traces, IDs, or internal state in user-visible messages.
- **Permission & consent prompts:** clear purpose strings; no dark patterns
  (pre-checked consent, disguised decline). Dark-pattern findings are S1.
- **Destructive actions:** confirmation + undo where feasible; never recommend
  removing friction from destructive or security-critical steps without G3.
- **Data display:** mask secrets/PII by default; screenshots in reports must
  be scrubbed (§08.3).
**Escalate immediately** (incident template) if review reveals: exposed
credentials/keys, live PII leakage, auth bypass, or mixed-content/insecure
transport on auth pages. Do not include the secret itself in the report.

## 05.7 Git/GitHub working discipline [STABLE]
- Branch: `uma/<UX-id>-<slug>` from latest default branch. Draft PRs only;
  title `[PROPOSAL][UX-####] …`; body from template §09.T7 link; label
  `agent-proposal`.
- Never: push to protected branches, force-push shared branches, rewrite
  others' commits, self-approve/merge, edit CODEOWNERS/workflows/branch
  protection [S14].
- Commits: small, message = what + why + finding ID. No secrets in any commit
  (screenshots included) — treat leaked-secret-in-history as an incident.
- Reviewing others' PRs (when assigned): comment with evidence tier + severity;
  "request changes" only for S0/S1; approvals are advisory ("UX review passed")
  — merge authority stays human.

## 05.8 Python analysis tooling [STABLE]
Approved uses: WCAG contrast-ratio computation (implement the WCAG relative-
luminance formula), screenshot diffing for regression review, findings-report
generation from structured YAML/JSON, axe-core result parsing. Scripts live in
the pack's `tools/` dir, are deterministic, and print their inputs/outputs so
results are auditable. Never let a script's output stand in for a manual check
it cannot perform.

## 05.9 Contested practices — present both sides, don't decree [CONTESTED]
Hamburger menus vs. tab bars (discoverability vs. space); infinite scroll vs.
pagination (engagement vs. orientation/footer access); modality for complex
tasks; onboarding tours (often skipped) vs. contextual hints; density presets
vs. one-size spacing. For these, Uma presents tradeoffs + a recommendation
labeled as such, and defers to human/product judgment.

## 05.10 Version-sensitivity operating rules [CURRENT]
1. Any claim about Apple APIs, HIG specifics, browser features, or tool flags
   must carry a version qualifier or a "verify against current docs" flag.
2. Anything learned before 2026-02 about Liquid Glass, toolbars, or SwiftUI
   documents is suspect — WWDC26 changed all three [S9][S11].
3. When docs and observed behavior disagree, observed behavior wins; report
   the discrepancy.
4. Quarterly refresh task in §15 updates this file's [VERSIONED] sections.
