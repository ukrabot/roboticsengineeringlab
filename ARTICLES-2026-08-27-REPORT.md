# Robotics Engineering Lab — Three-Article Delivery Report

**Publication date:** August 27, 2026
**Target market:** English-language readers in the USA and Canada
**Repository state:** 62 existing articles before publication; 65 after publication

## 1. Candidate topics evaluated

No first-party keyword-tool data was available in this session. All volumes below are **directional monthly estimates for the combined US/Canada English market**, triangulated on August 27, 2026 from public search-result inspection (which publishers, vendors and standards bodies currently rank for each term), related-query presence, and the public ranges keyword tools historically report for adjacent robotics and industrial-automation terms. They are not Search Console data and should be replaced with the site's own data when available.

| # | Candidate (proposed title) | Primary keyword | Secondary keywords | Est. volume (US+CA, directional) | Difficulty / why | Intent | Likely reader | Decision |
|---|---|---|---|---|---|---|---|---|
| 1 | Stepper Motor Robot Arm: Sizing by Torque and Speed | `stepper motor robot arm` | nema 17 robot arm, stepper torque calculation, TMC2209 current setting, closed loop stepper | 700–1,900 (incl. NEMA 17 / stepper sizing queries) | Low-Medium — vendor catalogues and hobby forums rank; no constraint-based sizing method | Informational / how-to | Hobbyist, student, controls engineer | **Selected** |
| 2 | Used Industrial Robot Arm: A Buyer's Inspection Guide | `used industrial robot` | refurbished robot arm, used FANUC robot for sale, robot controller matching, robot mastering | 400–1,100 (incl. brand-specific "used FANUC/ABB robot") | Low — marketplace listings rank, no independent buying-method page | Commercial investigation | Plant manager, integrator, maintenance lead | **Selected** |
| 3 | Hand-Eye Calibration for Robot Arms: Step-by-Step Method | `hand-eye calibration` | eye in hand calibration, AX=XB, calibrateHandEye opencv, robot camera calibration | 800–2,200 | Medium — academic and library docs rank; no practitioner commissioning method | Informational (commissioning) | Vision engineer, ROS 2 developer, integrator | **Selected** |
| 4 | Collaborative Robot vs Industrial Robot Arm | `cobot vs industrial robot` | collaborative vs traditional robot, fenced vs cobot | 1,000–3,000 | High — heavily saturated, including AI-generated content farms carrying invented prices | Commercial investigation | Plant manager | Rejected: cannibalizes `collaborative-robot-arm-2026` and the decision matrix already in `robot-machine-tending`; SERP quality too low to enter with a differentiated format |
| 5 | Robot Arm Cost Breakdown 2026 | `robot arm cost` | industrial robot price, robot cell cost, cobot price | 1,500–4,000 | Medium | Commercial investigation | Plant manager | Rejected: overlaps `robot-arm-roi-calculator`, `robot-arm-leasing-buying` and the four brand review pages |
| 6 | URDF and Xacro for Robot Arms | `urdf robot arm` | xacro tutorial, robot description file | 400–900 | Medium — official docs rank | Informational (tutorial) | ROS 2 developer | Rejected: would repeat the checkpoint-tutorial structure of `moveit-2-setup-assistant-robot-arm` and `ros2-robot-arm-control` |
| 7 | Robot Cell Guarding and Fencing | `robot cell guarding` | robot safety fence, perimeter guarding robot | 200–600 | Medium | Commercial investigation | Integrator | Rejected: overlaps `robot-risk-assessment`, `robot-light-curtain-integration` and `robot-area-scanner` |
| 8 | Lockout/Tagout for Robot Maintenance | `robot lockout tagout` | LOTO robot cell, robot energy isolation | 300–800 | Medium | Informational / compliance | Maintenance technician | Rejected: would repeat the validation-procedure structure of `cobot-force-limit-validation`, the most recent article |
| 9 | Servo vs Stepper for Robot Joints | `servo vs stepper robot` | closed loop stepper vs servo, robot joint actuator | 300–700 | Medium | Commercial investigation | Hobbyist, engineer | Rejected: folded into candidate 1 as a decision section rather than published as a separate page, to avoid splitting one intent across two URLs |

US/Canada split: Canadian share is a small fraction of combined English volume for all nine (typically 8–12%); it does not change any decision. Both countries are served by the same pages, with US (ANSI/A3, NFPA, OSHA) and Canadian (CSA) context included where applicable.

## 2. Selected articles and why they won

- **Stepper motor robot arm (1)** — the library had component explainers (smart servos, encoders, belt vs gear drive) but no page that sizes a stepper joint from a stated payload and duty cycle. The intent is a *constraint-driven selection* problem, which no existing page answers. Fully sourceable from published motor/driver datasheets with printed reference prices, and it gives the Arduino audience the missing sizing method.
- **Used industrial robot (2)** — a genuine zero-overlap gap. Nothing in the 62 existing articles mentions used, refurbished, second-hand, remanufactured or pre-owned equipment (verified programmatically). This is the site's first commercial-investigation page about the secondary market, where the dominant content is marketplace listings with no inspection method. Quote-dependent categories rather than street prices, as the equipment requires.
- **Hand-eye calibration (3)** — `robot-arm-vision-system` mentions hand-eye three times but devotes a single H2 to it, and `robot-arm-calibration` covers mastering and ISO 9283, not camera-to-robot transforms. The AX = XB problem, the five OpenCV solvers and the pose-set requirements are a distinct engineering problem with a distinct audience, and the topic is current because the OpenCV and MoveIt 2 interfaces are stable and documented.

The three have different primary intents (how-to sizing, commercial investigation, commissioning procedure) and different user problems; none targets "robot arm" broadly.

## 3. Anti-cannibalization audit

Audit basis: every HTML file in `articles/` (titles, meta descriptions, H1s, visible H2s, FAQ questions), `articles/index.html`, `index.html` and `sitemap.xml`, extracted and compared programmatically on August 27, 2026. A second automated pass over the finished pages confirmed zero H2 overlap (excluding the two site-wide template headings) and zero shared paragraphs of 18 or more words against all 62 existing articles.

### A. Stepper Motor Robot Arm — `stepper-motor-robot-arm`
Closest existing pages: `smart-servo-robot-arm` (a different actuator class), `joint-encoders-robot-arm` (feedback components), `belt-drive-vs-gear-drive` (transmission choice), `arduino-mega-robot-wiring` (wiring, not sizing). The word "stepper" appears three times in `3d-printed-robot-arm-parts`, in body copy only, never in a title, meta description or heading.
**Decision: Pass.** Angle: a five-constraint sizing sequence (static torque, torque–speed curve, reflected inertia, resolution, thermals) ending in a per-joint table and a closed-loop decision. Links to the actuator, transmission, encoder, payload-calculator and wiring pages instead of restating them.

### B. Used Industrial Robot Arm — `used-industrial-robot-arm`
Closest existing pages: `robot-arm-leasing-buying` (new-equipment finance routes), `robot-arm-roi-calculator` (payback modelling), `robot-arm-maintenance` (in-service care), the four brand review pages (new machines). Programmatic sweep for *used*, *refurbish*, *second hand*, *remanufactur* and *pre-owned* returned **zero hits** across all 62 articles, both indexes and the sitemap.
**Decision: Pass.** Angle: a four-route comparison with a decision matrix, the arm-and-controller pairing constraint, mastering/battery/hour-meter verification, and total cost of acquisition. Industrial robots are quote-dependent, so the article gives cost categories and public listing ranges, never street prices.

### C. Hand-Eye Calibration — `hand-eye-calibration-robot`
Closest existing pages: `robot-arm-vision-system` (contains "hand-eye" ×3 and "eye-in-hand" ×2 in its head metadata, but only one H2 on the subject), `robot-arm-calibration` (mastering and ISO 9283 performance, no camera transform, zero mentions of hand-eye), `moveit-2-setup-assistant-robot-arm` (URDF/MoveIt setup), `ros2-robot-arm-control` (controllers).
**Decision: Pass with a distinct angle.** Angle: a five-checkpoint commissioning method for the camera-to-robot transform, including the pose-diversity requirement that determines whether AX = XB is solvable at all, residual diagnostics that separate a bad calibration from a bad pose set, and a touch-test pass criterion. It cross-links the vision, end-effector, calibration, MoveIt and ROS 2 pages.

Slug check: all three slugs were absent from `articles/`, `sitemap.xml`, and the internal-link graph before insertion (verified programmatically).

## 4. Delivered articles

| | A. Stepper motor | B. Used robot | C. Hand-eye calibration |
|---|---|---|---|
| Slug | `stepper-motor-robot-arm` | `used-industrial-robot-arm` | `hand-eye-calibration-robot` |
| Title (chars) | Stepper Motor Robot Arm: Sizing Guide (51) | Used Industrial Robot Arm: A Buyer's Inspection Guide (53) | Hand-Eye Calibration for Robot Arms: Step-by-Step Method (56) |
| Meta description (chars) | 156 | 154 | 157 |
| Primary keyword | stepper motor robot arm | used industrial robot | hand-eye calibration |
| Intent / audience | Informational how-to; hobbyist, student, controls engineer | Commercial investigation; plant manager, integrator | Informational commissioning; vision engineer, ROS 2 developer |
| Structure (all three differ) | Selection guide by constraints | Comparison with decision matrix | Build/commissioning tutorial with five checkpoints |
| Visible main-content words | 4,632 | 4,315 | 4,472 |
| H2 sections | 15 | 14 | 16 |
| Contextual internal links | 5 | 5 | 5 |
| FAQs (visible = schema, 1:1) | 6 | 6 | 6 |

Word counts are the visible words inside `<main>` after removing the author aside, footer navigation, editorial-disclosure block, navigation, JSON-LD and all markup; table cells and list items are counted, headings are counted once.

H2 sequences verified distinct across the three articles and against all 62 existing articles (the only headings in common are the two site-wide template headings, "Sources and methodology" and "Frequently asked questions", which every article on this site emits).

## 5. Unique value added

- **Stepper motor:** a worked joint-sizing chain — τ_gravity = 9.81 × (0.40 × 0.12 + 0.25 × 0.28) = 1.16 N·m, × 1.8 duty factor = 2.08 N·m, ÷ (10:1 reduction × 0.90 efficiency) = **0.231 N·m = 23.1 N·cm** at the motor; the electrical time constant τ_e = L/R = 3.2 mH / 1.65 Ω = **1.94 ms** compared against 31 µs per microstep at 600 rpm and 1/16 microstepping, which is the actual reason torque collapses with speed; standing loss 2 × 2.0² × 1.4 = **11.2 W**; resolution 1.8° / (16 × 10) = 0.01125° = **0.059 mm** at a 300 mm lever. Plus the TMC2209 V_REF-to-current relationship from the datasheet, and a per-joint starting-point table for a 6-DOF arm.
- **Used robot:** the arm-and-controller factory-pairing constraint and what a mismatch costs; controller-generation tables for FANUC, ABB, KUKA and Yaskawa with the support horizon each implies (including ABB's stated IRC5 phase-out in June 2026 with continued spares and service for the installed base); the software-option licence trap — options are licensed, are not included as standard, and do not transfer automatically; a total-cost-of-acquisition frame showing that at $29,500 of hardware a robot at 40% of project cost implies roughly $73,750 and at 25% implies roughly $118,000 (percentages labelled as planning assumptions, not quotations); and the point listings never make — re-deployment is a new installation with a new task-based risk assessment.
- **Hand-eye calibration:** the AX = XB formulation and why a translation-only pose set is unsolvable; the five OpenCV solver families mapped to their source papers (Tsai & Lenz 1989, Park & Martin 1994, Horaud & Dornaika 1995, Andreff/Horaud/Espiau 1999, Daniilidis 1998) plus the robot-world Kronecker method (Shah 2013) used for eye-to-hand; a worked error-propagation calculation showing that at r = 0.600 m a 0.30° rotation error produces **3.14 mm** of TCP error, 0.10° produces 1.05 mm and 0.05° produces 0.52 mm, while a 1 mm translation error stays 1 mm everywhere — the reason rotation diversity, not sample count, governs the result; an angular-resolution estimate (3.45 µm pixel / 6 mm lens = 0.033°/px, 0.003° at 0.1 px subpixel); and a six-way failure-diagnosis table.

Competing English results inspected for positioning (not an exhaustive audit): motor-vendor catalogues and hobby forums (stepper); used-equipment marketplaces with listing-only content (used robot); OpenCV/MoveIt documentation and academic papers with no commissioning method (hand-eye). None provides the above method, calculations or decision framing in one place.

## 6. E-E-A-T / value layers included

| Layer | Stepper motor | Used robot | Hand-eye calibration |
|---|---|---|---|
| Illustrative scenario / example calculation | Both — labelled sizing scenario plus four labelled example calculations | Example calculation (total cost of acquisition) | Example calculation (rotation-to-linear error, angular resolution) |
| Indicative 2026 price / quote breakdown | Indicative 2026 prices + reference range for the power supply | Quote-breakdown framing; public listing reference range; quote required for reconditioning | Indicative 2026 prices for camera and target |
| Typical reader question | Six FAQs plus body pull-out questions | Six FAQs including "do I have to buy the matching controller" | Six FAQs including "how many poses do I need" |
| Official-source link + explanation | Pololu driver comparison table and product page, with an explanation of why the stated test condition matters | OSHA Technical Manual Section IV Chapter 4, with an explanation of why it governs the risk-assessment duty | OpenCV calib3d documentation and ROS REP 103, each with an explanation of what it is authoritative for |

All four layers are present in all three articles, each visibly labelled. Every article carries an editorial disclosure that Robotics Engineering Lab did not buy, install, measure, test or refurbish the equipment, that scenarios are illustrative and labelled, and that the work requires qualified professionals. Safety content is educational, recommends qualified professionals and lockout/tagout, and approves no cell.

## 7. Source and price caveats

- Volume estimates are directional (method and date in section 1).
- Component prices are public vendor and distributor listings accessed August 27, 2026 (Pololu, StepperOnline, AndyMark, Bravoelectro, TRC Electronics, Edmund Optics, DigiKey, Mouser), labelled indicative or as a reference range, never as quotations and never as Robotics Engineering Lab inventory. The DRV8825 price of $15.95 and the driver continuous-current figures were re-verified against the live Pololu pages during quality control on the publication date.
- Industrial robot arms, controllers and safety systems are quote-dependent. Article 2 deliberately gives cost categories and public listing ranges ($7,500–$29,500 for the cited six-axis FANUC listings) rather than street prices, and states that the listings are asking prices, not offers.
- The 15–25% as-removed contingency and the 40%/25% project-share figures in article 2 are labelled in the text as general planning assumptions, not quotations.
- Every standards reference (ANSI/A3 R15.06-3-2025, ISO 10218-2, ISO 12100, IEC 60204-1 / NFPA 79, CSA Z434) tells readers to obtain the current edition enforced in their jurisdiction. No pass criterion in any of the three articles is presented as a standard or a certification.
- Hand-eye pass criteria are stated as engineering practice, not as a standard.

## 8. Quality-control checklist

Automated by `qc_check.py` (run from the repository root, then removed so the build helper is not committed): **219 checks, 0 failures**, 73 checks per article. Every item below is a check the script actually executed.

| Check | Stepper motor | Used robot | Hand-eye calibration |
|---|---|---|---|
| ≥ 2,500 visible main-content words | PASS — 4,632 | PASS — 4,315 | PASS — 4,472 |
| Title unique, ≤ 60 chars | PASS — 51 | PASS — 53 | PASS — 56 |
| Meta description unique, ≤ 160 chars | PASS — 156 | PASS — 154 | PASS — 157 |
| Primary keyword in title, H1, intro and an H2 | PASS | PASS | PASS |
| Slug unique, absent pre-insertion | PASS | PASS | PASS |
| No H2 or ≥18-word paragraph duplicated vs any existing article | PASS | PASS | PASS |
| Intent and reader explicit | PASS | PASS | PASS |
| Anti-cannibalization audit documented | PASS | PASS | PASS |
| Every number sourced, assumed, or labelled | PASS | PASS | PASS |
| Prices labelled indicative / reference range / quote required | PASS | PASS | PASS |
| Structure distinct, H2 order distinct | PASS | PASS | PASS |
| Standards relevant, current, not presented as certification | PASS | PASS | PASS |
| Exactly six visible FAQs, character-for-character 1:1 with FAQPage | PASS | PASS | PASS |
| JSON-LD parses (BlogPosting, BreadcrumbList, FAQPage) | PASS | PASS | PASS |
| No Review / Product / Offer / AggregateRating schema | PASS | PASS | PASS |
| BreadcrumbList = Home → Tutorials → current article | PASS | PASS | PASS |
| inLanguage en-US, author Marcus Chen, publisher Robotics Engineering Lab | PASS | PASS | PASS |
| mainEntityOfPage id == canonical | PASS | PASS | PASS |
| Canonical uses the no-trailing-slash convention | PASS | PASS | PASS |
| meta robots `index, follow` | PASS | PASS | PASS |
| Full Open Graph set incl. og:image:alt and article timestamps | PASS | PASS | PASS |
| Full Twitter card set; twitter:title differs from `<title>` | PASS | PASS | PASS |
| Dates equal the execution date (2026-08-27) | PASS | PASS | PASS |
| ≤ 5 contextual internal links, unique targets and anchor text, all resolving | PASS — 5 | PASS — 5 | PASS — 5 |
| Local images resolve; alt text, width and height present | PASS | PASS | PASS |
| Hero alt does not falsely claim a lab test | PASS | PASS | PASS |
| ≥ 3 E-E-A-T value layers (4 present) | PASS | PASS | PASS |
| Editorial disclosure, consent-aware analytics and AdSense retained | PASS | PASS | PASS |
| HTML parses with balanced tags, exactly one H1 | PASS | PASS | PASS |
| Local static server returns 200 | PASS | PASS | PASS |

Site-wide checks: three sitemap entries with `lastmod` 2026-08-27, `changefreq` monthly, `priority` 0.7, no trailing slash, and the sitemap parsing as valid XML with 74 `<url>` entries (PASS); homepage cards link to the correct slugs with unique alt text (PASS); homepage ItemList `numberOfItems` 65 with 65 items in sequential positions 1–65 and the three new URLs at 63–65, parsing as valid JSON (PASS); archive CollectionPage → ItemList `numberOfItems` 65 with 65 sequential items, parsing as valid JSON (PASS); visible homepage stat updated to 65 (PASS); homepage category counts now 8/10/12/12/4/6/8/5 = 65 with each block's declared count matching its actual list length (PASS); archive category counts 8/10/13/12/4/5/8/5 = 65 (PASS — the archive uses its own category names and split, which were updated independently rather than copied from the homepage); no existing article, metadata block, consent code or AdSense removed — `git status` shows only the three new article files, the three new reports/artifacts and the three modified index/sitemap files (PASS).

### Defects found and fixed during quality control

Reported for transparency, since each was a real defect rather than a style point:

1. **The visible FAQ block was never rendered.** The generator computed the six FAQ items but never inserted them into the page body, so all three articles would have shipped with FAQPage JSON-LD and no visible FAQs. Fixed in the generator and re-verified: each page now has exactly six `.faq-item` blocks matching the schema character-for-character.
2. **Broken internal link in article 2.** It linked to `robot-arm-risk-assessment`; the actual slug is `robot-risk-assessment`. Fixed and re-verified as resolving.
3. **Invalid JSON-LD in `index.html`.** The ItemList edit left a missing comma between positions 62 and 63, so the homepage structured data would not parse. Fixed; the block now parses and reports 65 sequential items.
4. **Entity/title mismatch.** `htmllib.escape` was encoding the apostrophe in article 2's title as `&#x27;`, so the rendered `<title>` did not match the JSON-LD `headline` string. The escaper now leaves apostrophes intact and the comparison is made on decoded text.
5. **Primary keyword missing from article 2's introduction and H2.** Both were reworded so `used industrial robot` appears in the intro paragraph and in an H2.

Nothing above was found by inspection; all five were caught by the automated checks.

**Follow-up recommendation (not done this session):** the existing `robot-arm-safety-usa-canada` page (lastmod 2025-06-07) still predates ANSI/A3 R15.06-2025 and CSA Z434:26, and `robot-arm-vision-system` now has a much stronger hand-eye page linking into it — schedule a refresh of both so the older pages reflect the 2026 standards stack and cross-link the new calibration article.

## 9. Files created or updated

Created: `articles/stepper-motor-robot-arm.html`, `articles/used-industrial-robot-arm.html`, `articles/hand-eye-calibration-robot.html`, `ARTICLES-2026-08-27-REPORT.md`.
Updated: `sitemap.xml` (+3 URLs, 71 → 74), `index.html` (3 cards, ItemList positions 63–65 and `numberOfItems` 65, visible stat 62 → 65, three category counts), `articles/index.html` (3 list items, ItemList `numberOfItems` 65, three category counts).

The build and QC helpers used to generate and validate these pages were run from the repository root and deleted afterwards, so no generator or scratch file is committed.

## 10. Load and parse confirmation

All three article pages were served from a local static server on the publication date and returned HTTP 200 with full content (56,204 bytes, 57,283 bytes and 56,799 bytes respectively), as did `index.html`, `articles/index.html` and `sitemap.xml`. All three JSON-LD blocks on each article page, the homepage ItemList, the archive CollectionPage/ItemList, and the updated ItemList blocks in `index.html` / `articles/index.html` were parsed as valid JSON during QC. `sitemap.xml` parsed as valid XML with 74 `<url>` entries, the three new URLs present with `lastmod` 2026-08-27 and no trailing slash. All five internal links per article were confirmed to resolve to files that exist in `articles/`, and all five external official-source URLs added to the Sources sections were fetched and confirmed live on the publication date.
