# Debra Research Knowledge Repository

This is Debra's durable, cross-project research memory. Read this file before
starting research and update it after completing research. Keep entries
concise, sourced, searchable, and deduplicated. This repository stores reusable
findings, not complete proposals.

## Usage rules

- Organize entries by market or topic, then by product or competitor.
- Merge updates into existing entries instead of creating duplicates.
- Attach a source URL and verification date to factual claims.
- Mark outdated or contradicted claims as superseded; preserve context only
  when it helps explain a meaningful change.
- Re-check volatile claims such as pricing, plan limits, availability, product
  features, policies, and market position before relying on them.
- Link related proposals and Debra task logs when they contain useful detail.

## Entry template

### <Market or topic> — <Product or competitor>

- **Aliases/keywords:** <search terms and related names>
- **Last verified:** <YYYY-MM-DD>
- **Freshness:** <stable|moderately volatile|volatile>; <re-check trigger>
- **Related work:** <proposal or TASK-Debra path, if any>

#### Findings

- <Concise reusable finding> ([Source title](https://example.com), verified
  YYYY-MM-DD)

#### Changes and superseded claims

- <Optional dated note describing what changed and which older claim it
  replaces>

---

## Knowledge entries

<!-- Add and maintain research entries below this line. -->

### Consumer iOS App User Guide & Documentation — Best Practices & Baseline

- **Aliases/keywords:** user guide, help center, documentation, in-app help, FAQ, troubleshooting, accessibility documentation, mobile app support
- **Last verified:** 2026-07-17
- **Freshness:** stable; re-check when major iOS versions (iOS 27+) introduce new accessibility requirements or help delivery patterns
- **Related work:** `ai-factory/proposals/user-guide-feedback-v1-rev2-to-v1-rev3-debra.md`, TASK-Debra-5; `ai-factory/proposals/user-guide-feedback-v1-rev3-to-v1-rev4-debra.md`, TASK-Debra-6

#### Findings

- **Figma Mobile App Guide** exemplifies task-based user guide structure: prerequisites → foundational features → intermediate features → advanced capabilities. Includes extensive annotated screenshots showing actual app UI states, step-by-step instructions with specific UI references ("Tap the icon in the top right corner"), dedicated troubleshooting section for device-specific issues, and hierarchical organization. Model for visual documentation and task orientation. ([Figma Mobile App Guide](https://help.figma.com/hc/en-us/articles/1500007537281-Guide-to-the-Figma-mobile-app), verified 2026-07-17)

- **Apple Support Guides** (Reminders, Stocks) use hierarchical organization nested within platform guides with cross-linking to related features. Support multiple iOS versions simultaneously. Task-based grouping (e.g., "Add reminders" vs. "View reminders") rather than feature-first organization. ([Apple Support](https://support.apple.com/guide/iphone/get-started-with-reminders-iphc7880ecd6/ios), verified 2026-07-17)

- **Beanhunter Help Center** organizes by category (About, Business Owners, Mobile App, Beanhunter Coffee Club). Uses FAQ format with Q&A structure. Searchable help portal. Simple but effective for café discovery app. ([Beanhunter Help](https://help.beanhunter.com/), verified 2026-07-17)

- **Waze Help Center** (2026) is organized into 8 main sections using verb-first audience-focused structure: "Plan your drive", "Drive with Waze", "Edit the Waze map", "Manage your account", "Manage your driving experience", "Waze on in-car displays", "Help & feedback", "Learn about Waze". Exceeds standard documentation by dedicating sections to community participation (map editing) and partnership scenarios (in-car displays). ([Waze Help](https://support.google.com/waze/?hl=en), verified 2026-07-17)

- **Industry best practices for iOS app documentation** (per Apple HIG, NN/G, Userpilot, industry sources): Use visual hierarchy and chunked content for scannability; step-by-step instructions with UI callouts; search and filtering for discoverability; FAQ and troubleshooting sections for completeness; annotated screenshots (images processed 60,000× faster than text); accessibility compliance (WCAG AA/AAA contrast, keyboard navigation, dynamic text sizing); multiple support channels (email, web, in-app); progressive disclosure (collapsible sections); and mobile-first responsive design. ([Apple HIG](https://developer.apple.com/design/human-interface-guidelines/offering-help), [NN/G Heuristic #10](https://www.nngroup.com/articles/help-and-documentation/), [Userpilot In-App Resource Center](https://userpilot.com/blog/in-app-resource-center/), verified 2026-07-17)

- **Brew Me Up User Guide (v1-rev4)** [UPDATED 2026-07-17]: Restructured to 8 main sections (Overview → Getting Started [A. Quick Start] → Navigation [A–E subsections] → Data Sync → Glossary → Troubleshooting → FAQ → Getting Help). Verified improvements over v1-rev3: (1) TOC reorganized into task-based hierarchy matching Figma/Waze patterns; (2) "What's new" is plain-language user-focused bullets (zero internal filename references); (3) screenshots render at uniform aspect-ratio 202/440 and fixed width 230px, with onboarding screenshots correctly placed under Getting Started > First Launch; (4) "Common icons at a glance" section removed entirely. Strengths retained from v1-rev3: built-in TOC keyword filter (exceeds baseline search), WCAG AAA contrast ratios with documented specifications, responsive two-column desktop / single-column mobile layout, collapsible progressive disclosure, skip link and focus states. Overall structure aligns with or exceeds Figma and Waze baselines. ([user-guide-feedback-v1-rev3-to-v1-rev4-debra.md](ai-factory/proposals/user-guide-feedback-v1-rev3-to-v1-rev4-debra.md), verified 2026-07-17)

#### Changes and superseded claims

- 2026-07-17: Updated Brew Me Up entry from v1-rev3 to v1-rev4. Rev4 addresses all four required fixes from prior revision: section hierarchy, "What's new" content, screenshot consistency, and removal of "Common icons" section. Added Waze baseline (8-section structure verified as market standard).

---

### Coffee Tracking & Specialty Coffee Apps Market — Competitive Landscape

- **Aliases/keywords:** coffee tracker, coffee logger, specialty coffee app, café discovery, coffee journaling, bean tracking, brew logging
- **Last verified:** 2026-07-16
- **Freshness:** moderately volatile; re-check when new entrants launch or major features are announced
- **Related work:** `proposals/debra-competitive-review.md`, TASK-Debra-1

#### Findings

- **Coffi** is the leading AI-powered coffee scanner app with SCA (Specialty Coffee Association) tasting framework integration. Users photograph coffee bags for instant identification of roaster, origin, flavor profile, and roast level. Includes community ratings, roaster profiles, and global leaderboards. ([Coffi App Store](https://apps.apple.com/us/app/coffi-coffee-tracker/id6743347762), [coffi.com](https://www.coffi.com/), verified 2026-07-16)

- **CoffeeJourney** emphasizes visual coffee journey mapping on a world map. Each logged cup appears as a pin showing geographic exploration history. Supports brew method selection (roast levels: Extra Light, Light-Medium, Medium-Dark, Extra Dark) and includes keyword search for past records. ([CoffeeJourney App Store](https://apps.apple.com/us/app/coffeejourney-coffee-tracker/id6758566084), verified 2026-07-16)

- **CoffeeLover** focuses on visual journaling with AI-powered sticker generation (Subject Lifting for instant photo cutouts). Includes caffeine tracking with real-time progress bar and color-coded health status. Features weekly/monthly reports with Taste DNA charts and mood-based categorization (MBTI tags). ([CoffeeLover App Store](https://apps.apple.com/us/app/coffeelover-coffee-tracker/id6760238275), verified 2026-07-16)

- **iBrewCoffee** targets specialty coffee enthusiasts with detailed brew logging: tracks 20+ parameters (grinder settings, water amount, temperature, extraction time, aroma, aftertaste, acidity). Provides access to 3000+ roasteries, 2000 coffee regions, 300 varietals. Supports 60+ brewing methods with custom method creation. ([iBrewCoffee](https://ibrew.coffee/), verified 2026-07-16)

- **Beanstats** specializes in home barista precision brewing with Bluetooth scale integration. Connects to Acaia and Bookoo scales for live weight/flow rate display during brewing. Includes espresso auto-capture (stops when flow drops below 0.2 g/s) and bean inventory management. ([Beanstats App Store](https://apps.apple.com/us/app/beanstats-coffee-tracker/id6756850760), [beanstats.com](https://www.beanstats.com/), verified 2026-07-16)

- **Cafeor** emphasizes minimalist daily coffee tracking with focus on caffeine monitoring. Converts photos to cute stickers, displays weekly/monthly/yearly statistics. ([Cafeor App Store](https://apps.apple.com/us/app/cafeor-coffee-tracker/id6757520656), verified 2026-07-16)

- **Coffee Book: Brew Timer** designed for brew repeatability. Tracks 20+ variables per brew and displays previous brew weight curves as reference overlay during new brew attempts. Supports comparison of repeat brews. ([Coffee Book App Store](https://apps.apple.com/us/app/coffee-book-brew-timer/id1512681263), verified 2026-07-16)

- **Beanconqueror** open-source specialty coffee app with 30+ customizable brewing parameters per method. Supports V60, AeroPress, Espresso, and others. ([BEANCONQUEROR](https://beanconqueror.com/), verified 2026-07-16)

- **Beanhunter** is community-driven café discovery platform (originated in Australia, now 180+ cities globally). Focus on user reviews and ratings of coffee shops by location. Features map-based café discovery. ([Beanhunter](https://www.beanhunter.com/mobile), verified 2026-07-16)

- **Coffeegram** allows social sharing of coffee statistics and achievements. Includes weekly/monthly stats visualization for Instagram and other social platforms. ([Coffeegram App Store](https://apps.apple.com/us/app/coffeegram-coffee-tracker/id6751598251), verified 2026-07-16)

- **World's 100 Best Coffee Shops** is curated café directory (2026 edition) with rankings, photos, editorial notes, precise map locations, and direct links to shop websites/Instagram. Includes favorites list and visit tracking. ([World's 100 Best Coffee Shops App Store](https://apps.apple.com/us/app/worlds-100-best-coffee-shops/id6759538654), verified 2026-07-16)

#### Market Segmentation

- **Personal tracking + café discovery** (minimal/casual): Cafeor, CoffeeLover, CoffeeJourney
- **Specialty coffee bean tracking + curation**: Coffi, iBrewCoffee
- **Home barista precision brewing**: Beanstats, Beanconqueror, Coffee Book
- **Community café discovery/reviews**: Beanhunter, Coffeegram
- **Ranked café directories**: World's 100 Best Coffee Shops

#### Key Feature Gaps in BrewMeUp vs. Competitors

- No coffee bean/roaster tracking (vs. Coffi, iBrewCoffee, Beanstats)
- No detailed brewing parameters beyond drink type (vs. iBrewCoffee, Beanstats, Beanconqueror, Coffee Book tracking 20-30+ variables)
- No caffeine tracking or daily limit warnings (vs. CoffeeLover, Cafeor, CoffeeWatch)
- No visual world map of coffee journey (vs. CoffeeJourney)
- No AI sticker/card generation for social sharing (vs. CoffeeLover, Cafeor)
- No community ratings or leaderboards (vs. Coffi, Beanhunter, Coffeegram)
- No Bluetooth scale integration (vs. Beanstats)
- No spending analytics/trends (vs. CoffeeLover, Cafeor)
- No structured tasting framework (vs. Coffi with SCA standards)
- No bean inventory management (vs. Beanstats, iBrewCoffee)
- No brew comparison/replay (vs. Coffee Book, Beanstats)

#### Changes and superseded claims

None yet—initial research entry.

---

### Route Discovery & Trip Planning Apps Market — Coffee Crawl Feature Competitors

- **Aliases/keywords:** route planner, trip planner, points of interest along route, search along route, multi-stop routing, coffee stops discovery, roadside attractions
- **Last verified:** 2026-07-16
- **Freshness:** moderately volatile; re-check pricing, plan limits, and feature releases annually
- **Related work:** `ai-factory/proposals/coffee-crawl-review-v1-debra.md`, TASK-Debra-2

#### Findings

- **Google Maps "Search Along Route"** allows users to find restaurants, gas stations, and attractions along a calculated route. Powered by Google Routes API which supports waypoint order optimization (automatic reordering for efficiency). Users enter destination, tap "Add stops", explore pins organized by category, add to trip. ([Google Maps documentation](https://developers.google.com/maps/documentation/routes/opt-way), verified 2026-07-16)

- **Google Maps Routes API** natively optimizes waypoint order for multi-stop trips, minimizing total distance/time. EZRoutePlanner and Upper use similar algorithms; Google Maps itself limits to 10 stops and doesn't auto-optimize in UI, but Routes API supports it. ([11 Best Multi-Stop Route Planner Apps for 2026](https://www.upperinc.com/blog/best-multi-stop-route-planner-app/), verified 2026-07-16)

- **Roadtrippers** is a premium road trip planner ($49.99/year Premium; free version allows up to 7 waypoints). Pulls from a curated database of road-trip-specific stops beyond Google Maps (roadside attractions, quirky diners, lesser-known state parks, viewpoints). Suggests stops by category (national parks, restaurants, coffee, campsites, hotels). ([Roadtrippers App Store](https://apps.apple.com/us/app/roadtrippers-trip-planner/id944060491), [How to Use Roadtrippers](https://thestokefam.com/how-to-use-roadtrippers/), verified 2026-07-16)

- **Wanderlog** is the leading collaborative trip planner in 2026. Supports collaborative itinerary creation, route sharing via link, expense splitting, in-app comments, and map optimization. "Map-first interface helps you visualize your route, optimize stop order, and estimate drive times." ([Wanderlog](https://wanderlog.com/), [Best Group Travel Planning Apps in 2026](https://www.avosquado.app/blog/best-group-travel-planning-apps-2026-complete-comparison/), verified 2026-07-16)

- **Yelp Collections** allows users to save groups of businesses and organize by category. Supports browsing on a map and filtering by distance. Collections can be shared but lack native route planning. ([Yelp Collections](https://www.yelp-support.com/article/What-is-a-Collection?l=en_US), verified 2026-07-16)

- **Apple Maps Trip Planner** (native iOS feature) supports creating routes with up to 15 waypoints, saving routes to Places Library, and sharing via link. Supports driving, walking, and transit modes natively. Routes use Apple Maps POI database. ([Apple Maps Features](https://www.apple.com/maps/), verified 2026-07-16)

- **CafeRadar** is a specialty café discovery map (60,000+ curated cafés, including every World's 100 Best Coffee Shops 2026 winner). Offers rich filtering: award badges, brunch hours, vibe tags (cozy/lively/quiet), amenities (wifi, seating, etc.), and live open hours. Walking directions included. ([CafeRadar](https://caferadar.app/), verified 2026-07-16)

- **Cappuccin** is a curated specialty coffee map with real shop profiles (photos, hours, vibe tags). Supports filtering by roastery, pour-over capability, work-friendly, and "open now" status. ([Cappuccin](https://apps.apple.com/us/app/cappuccin-coffee-shop-finder/id6755759425), verified 2026-07-16)

- **Roasters** maps 23,000+ cafés and roasters across 126 countries, crowd-curated. Supports filtering by "open now", nearest, newest, and community ratings/photos. ([Roasters App Store](https://apps.apple.com/us/app/roasters-great-coffee-nearby/id1466079049), verified 2026-07-16)

- **Waze Navigation** provides real-time rerouting based on live traffic, incidents, and road closures. Crowd-sourced alerts from drivers (accidents, construction, police, potholes). Auto-rerouting is automatic. ([Waze](https://www.waze.com/live-map), verified 2026-07-16)

- **HERE WeGo** supports full offline map regions with public transit infrastructure, enabling offline routing across transit, walking, and driving in 1,900+ cities. Widely used for international travel and offline navigation. ([Beyond Google Maps: Best Apps for Offline Public Transport Navigation](https://medium.com/@tamirmelinek/beyond-google-maps-the-best-apps-for-offline-public-transport-navigation-in-2026-dbbcdf10b9bc), verified 2026-07-16)

- **Moovit** specializes in public transit navigation with offline "Favorites" and schedule caching; particularly strong in cities outside North America. ([Beyond Google Maps article](https://medium.com/@tamirmelynek/beyond-google-maps-the-best-apps-for-offline-public-transport-navigation-in-2026-dbbcdf10b9bc), verified 2026-07-16)

- **AllTrails** focuses on multi-day hiking route planning with waypoint management (water sources, campsites, bail-out points), elevation data, and terrain analysis. AllTrails Peak offers custom route creation, multi-day splits, and map layers for slopes and public lands. ([AllTrails Help – Custom Routes](https://support.alltrails.com/hc/en-us/articles/37270479773204-How-to-create-custom-routes), verified 2026-07-16)

- **Upper** / **Upper Crew** are specialist multi-stop route optimization apps. Handle 25+ stops with automatic reordering for efficiency, bulk import, proof of delivery, real-time driver tracking. Among the most reliable multi-stop optimizers in 2026. ([11 Best Multi-Stop Route Planner Apps for 2026](https://www.upperinc.com/blog/best-multi-stop-route-planner-app/), verified 2026-07-16)

#### Feature Comparison: Coffee Crawl vs. Market Leaders

| Feature | Coffee Crawl | Google Maps | Roadtrippers | Wanderlog | CafeRadar | Roasters |
|---------|--------------|-------------|---------------|-----------|-----------|----------|
| Route calculation | Yes (Apple Maps) | Yes | Yes | Yes | Walk/POI only | Walk/POI only |
| Multi-stop optimization | No (fixed route order) | Optional (API) | Yes | Yes | N/A | N/A |
| Walking routes | No | Yes | Yes | Yes | Yes | Yes |
| Transit routes | No | Yes | Yes | Yes | No | No |
| Offline maps | No | Yes (regions) | No | No | No | No |
| Save/share routes | No | Yes (Places) | Yes | Yes (link share) | N/A | N/A |
| Collaborative editing | No | No | No | Yes | No | No |
| Open Now filtering | No | Yes | Yes | Yes | Yes | Yes |
| Rating/vibe filtering | No | Yes | Yes | Yes | Yes | Yes |
| Amenity filters | No | Yes | Partial | Partial | Yes | Yes |
| Live rerouting | No | Yes | Partial | No | N/A | N/A |
| Specialty coffee data | No (Apple Maps POI) | No | Partial | No | Yes (curated 60k+) | Yes (crowd 23k+) |

#### Key Gaps in Coffee Crawl vs. Competitors

1. **Multi-stop optimization**: Coffee Crawl cannot reorder stops for efficient visiting (competitors: Upper, Google Routes API, Wanderlog).
2. **Walking/transit modes**: Coffee Crawl supports driving only (competitors: Google Maps, Apple Maps, Wanderlog, CafeRadar).
3. **Save/share crawls**: No persistent storage or social sharing of crawl plans (competitors: Wanderlog, Roadtrippers, Apple Maps Places).
4. **Live availability**: No "open now" or hours filtering (competitors: CafeRadar, Cappuccin, Roasters, Google Maps).
5. **Rich filtering**: Only venue type (cafe/truck/bakery); no ratings, vibes, or amenities (competitors: CafeRadar, Cappuccin, Roasters).
6. **Collaborative planning**: Solo-only crawl planning (competitors: Wanderlog, Jourma, Let's Jetty).
7. **Live rerouting**: Static crawl; no response to shop closures or traffic (competitors: Waze, Google Maps).
8. **Specialty data**: Limited to Apple Maps POI (competitors: CafeRadar 60k+, Roasters 23k+, Beanhunter 180+ cities).
9. **Offline capability**: Requires internet (competitors: HERE WeGo, Apple Maps, Google Maps).
10. **Route history**: No saved crawls or favorites (competitors: Wanderlog, Roadtrippers, Apple Maps).

#### Changes and superseded claims

None yet—initial research entry (2026-07-16).

---

### iOS App Sync/Account/Onboarding/Search UX Baselines — Coffee & Consumer Apps

- **Aliases/keywords:** iCloud sync, account deletion, App Store Guideline 5.1.1, onboarding carousel, value proposition screens, recent searches, search history, autocomplete UX
- **Last verified:** 2026-07-17
- **Freshness:** moderately volatile (App Store guideline text and competitor feature sets can change); re-check before compliance-sensitive decisions
- **Related work:** `proposals/debra-usability-test-2026-07-17.md`, TASK-Debra-7; `proposals/debra-signup-field-requirements-2026-07-17.md`, TASK-Debra-8

#### Findings

- **Apple App Store Review Guideline 5.1.1(v)** requires any app that supports account creation to also offer in-app account deletion that actually removes the account's personal data (not just deactivation); a support-email-only flow is explicitly insufficient outside regulated industries. ([Apple Developer – Offering account deletion in your app](https://developer.apple.com/support/offering-account-deletion-in-your-app/), verified 2026-07-17)

- **Zero-setup iCloud sync is the baseline pattern for small coffee-tracker apps.** Beanstats, CoffeeLog, HiCoffee, and Caffeine App all sync automatically via the device's existing Apple ID/iCloud — no separate account signup, email entry, or manual "enable sync" toggle. ([Beanstats](https://apps.apple.com/us/app/beanstats-coffee-tracker/id6756850760), [CoffeeLog](https://apps.apple.com/gh/app/coffeelog-coffee-tracker/id6760129538), [HiCoffee](https://apps.apple.com/us/app/hicoffee-caffeine-tracker/id1507361706), [Caffeine App](https://apps.apple.com/us/app/caffeine-app-track-caffeine/id1045959983), verified 2026-07-17)

- **Recent-searches / search history in the empty ("zero state") search screen is treated as baseline search UX, not an advanced feature** — expected alongside autocomplete and matching-term highlighting. ([Baymard – Autocomplete Design Patterns](https://baymard.com/blog/autocomplete-design), [Smart Interface Design Patterns – Autocomplete UX](https://smart-interface-design-patterns.com/articles/autocomplete-ux/), verified 2026-07-17)

- **Multi-slide onboarding carousels (3–5 slides) that show rather than tell the app's value proposition** are a standard pattern for apps with real feature depth to preview (gamification, unique tools) before or alongside account/profile setup. ([UXCam – 12 Apps with Great User Onboarding](https://uxcam.com/blog/10-apps-with-great-user-onboarding/), [Userpilot – Mobile App Onboarding Flow](https://userpilot.com/blog/mobile-app-onboarding/), verified 2026-07-17)

- **Brew Me Up (as of 2026-07-17)**: sync requires manual email entry + a Settings toggle (no iCloud auto-sync); silently creates an anonymous server-side account via `AuthService.bootstrapAnonymous` the first time sync is enabled, with **no in-app account/data deletion found anywhere in source** (`grep` for delete-account patterns returns zero matches) — flagged as a possible App Store Guideline 5.1.1(v) exposure pending independent compliance review. Search (`SearchView.swift`) has no recent-searches/history and wipes query+scope on every tab exit. Onboarding is a single data-entry screen with no feature preview. Spending Analytics (previously a gap per the 2026-07-16 competitive review) is now implemented in Profile → Insights. ([debra-usability-test-2026-07-17.md](proposals/debra-usability-test-2026-07-17.md), verified 2026-07-17)

- **Brew Me Up onboarding field requirements — CORRECTED 2026-07-17 (supersedes the "verify this yourself" uncertainty in the entry above)**: Direct read of `OnboardingView.canSave` (`Coffee_Shop_TrackerApp.swift` lines 344–453) confirms the "Get Started" button is gated **only** on Name being non-empty; Email has no presence requirement, only an optional format check if the user types something. Both fields have real downstream use (Name displays in the Profile header via `savedName`; Email pre-fills Settings → Personal Info for the still-opt-in Sync feature), so this is not vestigial collection — but the UI gives no visual signal that Email is optional (identical styling to Name, no "(optional)" label), which is the likely source of user confusion/complaints that "the app requires both." Fix proposed: add an "(optional)" label or skip affordance to Email, no logic change needed.

- **App Store privacy-label verification (direct fetch, 2026-07-17): Beanstats and HiCoffee collect zero contact info.** Both apps' live "App Privacy" nutrition labels list only "Data Not Linked to You" (Device ID/Usage Data for Beanstats; Usage Data/Diagnostics for HiCoffee) — no Contact Info category at all, confirming via Apple-mediated disclosure (not just marketing copy) that these apps require neither name nor email at any point. This is a stronger evidentiary basis than the marketing-copy-only claim previously in this entry for these two apps specifically. ([Beanstats](https://apps.apple.com/us/app/beanstats-coffee-tracker/id6756850760), [HiCoffee](https://apps.apple.com/us/app/hicoffee-caffeine-tracker/id1507361706), verified 2026-07-17)

- **"Every app asks for email anyway" is category-dependent, not a universal iOS norm.** Personal-utility/habit-tracker apps trend toward zero or minimal signup (Streaks: "no account needed," no onboarding screens, iCloud-only, per [streaksapp.com](https://streaksapp.com/); Bear: core note-taking works with no signup, account only required to unlock cross-device Pro features, per [bear.app](https://bear.app/)). Social/networked apps (Instagram, BeReal) do gate hard on verified phone/email before any use, because their core function requires a verified identity in a shared graph ([BeReal Help Center](https://help.bereal.com/hc/en-us/sections/7350307994429005-Login-Signup), [Instagram Help](https://help.instagram.com/574047304429005/)). Conclusion: don't generalize "every app requires X" across categories without checking — the norm differs by whether the app's core function is networked/social vs. personal/on-device. (All verified 2026-07-17)

- **Apple Guideline 5.1.1(v) forced-registration standard, and 5.1.1(iii) data minimization**: Apple's accepted remediation for forced-registration rejections is a guest/anonymous mode letting users access non-account-based features before any registration/login; account creation should be deferred until a genuinely account-tied action. Optional fields at signup that aren't used by a shipping feature (example cited: birthdate, city, full name) are a common 5.1.1(iii) trigger; accepted fixes are removing the field or making it clearly optional. ([Apple Developer Forums – 5.1.1(v) clarification](https://developer.apple.com/forums/thread/724336), verified 2026-07-17; secondary summary via [PTKD](https://ptkd.com/journal/guideline-5-1-1-data-collection-and-storage-fix), published May 2026, verified 2026-07-17). **Caveat:** Apple's canonical guidelines page (`developer.apple.com/app-store/review/guidelines/`) is JavaScript-rendered and could not be fetched directly in this environment — the above is sourced from a developer-forum thread plus a third-party explainer, not Apple's own page text. Re-check against the canonical page (e.g., via a signed-in browser) before relying on this for an actual compliance decision.

- **Apple Guideline 4.8 (Sign in with Apple)** only applies to apps offering a third-party/social login (Facebook, Google, etc.) to set up/authenticate the primary account; when triggered, an equivalent Sign-in-with-Apple-style option must limit data to name/email, allow private relay email, and not collect ad-targeting interactions without consent. Not currently triggered for Brew Me Up (only Sign in with Apple itself is offered, as an optional link, no other third-party login) — would only become relevant if Google/Facebook login is added later. ([Apple Developer Forums – Guideline 4.8](https://developer.apple.com/forums/thread/750911), verified 2026-07-17)

- **Signup-friction UX research (NN/G, Baymard)**: NN/G's "Eliminate, Automate, Simplify" (EAS) framework and Baymard's sign-up friction research both frame minimal/deferred field collection ("ask only what's needed now, expand as investment grows") as current best practice — directionally well-supported across multiple sources, though specific completion-rate percentages seen in this pass came from search-result summaries rather than first-hand full-report reads and should be treated as lower-confidence than the directional conclusion. NN/G's "Get Started Stops Users" (fetched first-hand) reinforces that forcing data entry before demonstrating value causes trust loss/abandonment. ([NN/G – Get Started Stops Users](https://www.nngroup.com/articles/get-started/), verified 2026-07-17; [NN/G – EAS Framework](https://www.nngroup.com/articles/eas-framework-simplify-forms/), [Baymard – Reducing Sign Up Friction](https://baymard.com/blog/fast-and-easy-user-sign-up), both verified 2026-07-17 via search summary)

#### Changes and superseded claims

- 2026-07-17: Updated "Key Feature Gaps in BrewMeUp vs. Competitors" (Coffee Tracking & Specialty Coffee Apps Market entry above) — "No spending analytics/trends" is now superseded; Profile → Insights has a live total-spend figure and per-period bar chart as of 2026-07-17. The other listed gaps (bean/roaster tracking, brew parameters, caffeine tracking, world map, AI stickers, community ratings, Bluetooth scale, structured tasting, bean inventory, brew comparison) were not re-verified in this pass and should be treated as still-current pending a fresh check.
- 2026-07-17 (second pass, same day): Corrected the onboarding-field-requirement uncertainty flagged in the "Brew Me Up's actual current onboarding" note above — direct source read confirms Email is already optional in code (only Name is required); the "both fields appear required" language in that note is superseded. See new sub-finding above. Related: `proposals/debra-signup-field-requirements-2026-07-17.md`, TASK-Debra-8.
- 2026-07-18: Added Untappd comparable finding to iOS App Sync/Account/Onboarding entry (see new finding below about Untappd's zero-required-fields onboarding model). Reinforces the "every app asks for email" claim is category-dependent and not a universal norm.

---

### Beverage Tracking Apps Market — Untappd (Beer/Wine/Spirits Focus)

- **Aliases/keywords:** Untappd, drink tracker, beverage check-in, beer app, wine tracker, spirits log, social drinking app
- **Last verified:** 2026-07-18
- **Freshness:** moderately volatile (app feature updates, social/social-graph changes); re-check onboarding pattern or iOS privacy label if refactoring signup flow
- **Related work:** `proposals/debra-signup-field-requirements-2026-07-17.md`, TASK-Debra-8 (Finding 7)

#### Findings

- **Untappd is a direct beverage-tracking category peer to Brew Me Up** with a social-networking component (check-ins, badges, toasts/reactions, ratings, friend feeds). Unlike Brew Me Up's coffee-only focus, Untappd covers beer, wine, spirits, and other alcoholic beverages. Most significant finding: **Untappd allows complete app usage without account creation at all**, via a "New Registration Free Experience" feature (deployed ~2024, still live as of 2026-07-18). Users of legal drinking age (age/country verification only) can access core features (browse menus, search venues, find establishments, view ratings) without creating an account, logging in, or providing name/email. Account creation with email/username/password is fully optional and only required to unlock social features (check-ins, earning badges, connecting with friends, ratings, messaging, RSVP). Sign in with Apple and Google are also available as authentication alternatives. ([Untappd Help Center – New Registration Free Experience](https://help.untappd.com/hc/en-us/articles/14811149192596-New-Registration-Free-Experience-on-Untappd), verified 2026-07-18; [Untappd Help Center – Sign In With Apple](https://help.untappd.com/hc/en-us/articles/10310390430996-Sign-In-With-Apple-On-Web), verified 2026-07-18)

- **Onboarding pattern is more permissive than Brew Me Up's current model:** Brew Me Up requires a Name field to proceed ("Get Started" button gates on Name non-empty); Untappd requires nothing — users can press "Skip" and start browsing immediately. This contradicts the "every major app requires email at signup" claim often cited in informal feedback; Untappd proves that even in a social/networked beverage category (where identity collection would be architecturally justified), a market leader chose to remove friction entirely at first use and defer all identity/account info until the user voluntarily engages with social features.

- **Compliance implication for Brew Me Up:** If Untappd's zero-required-fields-for-browsing approach has cleared App Review (confirmed live in public app store listing as of 2026-07-18), then Brew Me Up's current "Name required, Email optional" is conservative and carries no incremental App Store Guideline 5.1.1 risk. The research supporting Brew Me Up's recommended fix (mark Email as optional in UI) remains valid, and DJ could technically go further (deferring Name entirely or making it optional after age/region verification) without new compliance exposure — though that's a larger product decision.

#### Changes and superseded claims

None yet—initial research entry.

---

### Food/Restaurant Tracker & Discovery Apps Market — Beli, Yelp, Photo Loggers

- **Aliases/keywords:** food tracker, restaurant discovery, check-in app, food photography, social dining, restaurant collections, food sharing
- **Last verified:** 2026-07-28
- **Freshness:** moderately volatile; re-check feature lists, pricing, social graph changes annually
- **Related work:** `proposals/debra-competitive-review.md`, TASK-Debra-10

#### Findings

- **Beli** is a food/restaurant-focused social discovery app (2.5M+ downloads, 4.9/5 rating as of 2026). Core features: users track restaurants they've visited, rate dining experiences, receive personalized recommendations via "Match Score" (taste compatibility with friends). Includes **ranked lists and maps** for organization and "Want to Go" distinction (restaurants user wants to visit vs. has visited). Users can **add tags to help organize and filter lists**, add notes and favorite dishes, and view a **Taste Profile** to learn preferences. The app emphasizes **friend-based discovery** with a newsfeed showing "the latest spots your friends have tried" and comparison of taste compatibility. **No explicit spending tracking or temporal analytics mentioned** in app store listing. ([Beli App Store](https://apps.apple.com/us/app/beli/id1478375386), verified 2026-07-28; [Beli – Wikipedia](https://en.wikipedia.org/wiki/Beli_(app)), verified 2026-07-28)

- **Untappd** (beverage focus, already documented above) features **check-in and community ratings**, with **badges earned for exploring new styles/breweries**, and **live beer menus** at nearby venues. Notably implements **friend messaging** and **direct toasts/reactions** to check-ins. Allows browsing/searching **without account**, but account (email/username or Sign in with Apple/Google) is required for social participation (check-ins, badges, ratings, RSVP). ([Untappd App Store](https://apps.apple.com/us/app/untappd-find-drinks-you-love/id449141888), verified 2026-07-28; [Untappd Blog – New Badges: World Pint 2026](https://untappd.com/blog/new-badges-world-pint-2026/1925), verified 2026-07-28)

- **Yelp Collections** (2026 update) allow users to **create, follow, and share Collections** (groups of saved business pages). Collections are **shareable via link**, can be followed by other users, and users can browse auto-generated or manually curated lists. The 2026 home feed refresh includes "AI-powered personalization" and "Want to Go" bookmarking. Search and filtering include **live "open now" status**, ratings, and review-based sorting. ([Yelp – Collections Support](https://www.yelp-support.com/article/What-is-a-Collection?l=en_US), verified 2026-07-28; [Yelp Blog – Collections Sharing](https://blog.yelp.com/news/bookmark-sharing/), verified 2026-07-28; [Yelp Blog – Spring 2026 Release](https://blog.yelp.com/news/spring-product-release-2026/), verified 2026-07-28)

- **Food Photo Log** app (photo-based logging) supports **exporting data in a ZIP bundle** containing an **Excel-compatible CSV plus all uploaded photos with metadata**. Users can "choose the date range to export," offering granular control over data portability. ([Food Photo Log App Store](https://apps.apple.com/us/app/food-photo-log/id6596760732), verified 2026-07-28)

- **Coffeegram** (coffee-specific, already researched) emphasizes **temporal analytics**: "monthly breakdowns, expense reports, and consumption trends." Shows **spending patterns over weeks/months** and **peak coffee times** via visual charts. ([Coffeegram App Store](https://apps.apple.com/us/app/coffeegram-coffee-tracker/id6751598251), verified 2026-07-28)

- **Coffee Budget Tracker** includes **monthly budget setting, expense monitoring**, and **spending history/trends analysis**. Tracks "bought vs. home-made coffee" distinction and provides **work-mode tracking** and **daily challenges/streaks** for engagement. ([Coffee Budget Tracker App Store](https://apps.apple.com/us/app/coffee-budget-tracker/id6749211840), verified 2026-07-28)

- **Cafeor** (minimalist coffee tracker) features **daily coffee logging by type**, **caffeine intake monitoring**, and **total spending tracking** with aggregated stats. Emphasizes simplicity and visual presentation (photos converted to stickers). ([Cafeor App Store](https://apps.apple.com/us/app/cafeor-coffee-tracker/id6757520656), verified 2026-07-28)

- **NutriBalance** gamified nutrition tracker (non-food-specific but relevant for gamification patterns) includes **40+ achievement badges**, daily streaks, XP points, **weekly league leaderboards**, daily missions, and social accountability features. Demonstrates **notification-driven badge unlocking** and **social competition** as retention mechanics. ([NutriBalance Official](https://officialnutribalance.app/blog/best-gamified-calorie-tracker/), verified 2026-07-28)

#### Key competitive patterns identified

- **To-visit vs. visited distinction**: Beli ("Want to Go"), Yelp ("Want to Go" bookmark), Google Maps (favorites + saved list) all distinguish intention-to-visit from actual visits. Single-category trackers (coffee, donuts, etc.) often collapse this.
- **Collections/curated lists**: Yelp Collections, Beli ranked lists, Google Maps Places, Wanderlog trips — persistent, shareable, modifiable groupings are standard for trip planning.
- **Temporal analytics**: Coffeegram, Coffee Budget Tracker, Cafeor all show spending/consumption over time (weekly, monthly, yearly). Rare in single-transaction loggers.
- **Search history / recent searches**: Expected in search-forward apps (Yelp, Google Maps, Untappd). Baseline UX.
- **Export options**: Food Photo Log (ZIP + CSV + photos), CSV-only trackers, and no-export apps. Photo export is emerging as table stakes for photo-logging.
- **Badge notifications**: NutriBalance, Untappd, Streaks drive engagement via push notifications on badge earn/progress. Silent badges are discoverable but non-motivating.
- **Open now / live status**: Yelp, Google Maps, CafeRadar, Roasters, Cappuccin all filter by current operating status. Requires backend API for live hours.

#### Changes and superseded claims

None yet—initial research entry (2026-07-28).

---
