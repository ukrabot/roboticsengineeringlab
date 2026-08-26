# Robotics Engineering Lab — Three-Article Delivery Report

**Publication date:** August 26, 2026
**Target market:** English-language readers in the USA and Canada
**Repository state:** 59 existing articles before publication; 62 after publication

## 1. Candidate topics evaluated

No first-party keyword-tool data was available in this session. All volumes below are **directional monthly estimates for the combined US/Canada English market**, triangulated on August 26, 2026 from public search-result inspection (which publishers and standards bodies currently rank for each term), related-query presence, and the public ranges keyword tools historically report for adjacent robotics and industrial-automation terms. They are not Search Console data and should be replaced with the site's own data when available.

| # | Candidate (proposed title) | Primary keyword | Secondary keywords | Est. volume (US+CA, directional) | Difficulty / why | Intent | Likely reader | Decision |
|---|---|---|---|---|---|---|---|---|
| 1 | Robot Arm Troubleshooting: Symptom-to-Cause Diagnosis | `robot arm troubleshooting` | robot arm fault diagnosis, robot lost mastering, robot arm vibration, robot following error, cobot troubleshooting | 400–1,000 | Medium — OEM support pages and integrator blogs rank; no independent diagnostic-method page exists | Informational (diagnostic) | Maintenance technician, controls engineer, integrator | **Selected** |
| 2 | Robot Cell Electrical Design: NFPA 79 & IEC 60204-1 | `robot cell electrical design` | NFPA 79 robot, IEC 60204-1 robot cell, robot cell wiring, SCCR robot control panel, robot cell 24 VDC | 200–600 for the head term; `NFPA 79` alone 1,000–2,500 US | Low-Medium — standards bodies and panel shops rank; no robot-cell-specific walkthrough | Commercial investigation / informational | Controls engineer, integrator, maintenance electrician | **Selected** |
| 3 | Cobot Force Limit Validation: ISO 10218-2 Test Plan | `cobot force limit validation` | power and force limiting, ISO 10218-2 collaborative, ISO/TS 15066 force limits, PFL validation, cobot force testing | 300–900 (incl. ISO 15066 / PFL queries) | Low — vendor pages and standards summaries rank; no validation-procedure page | Informational / commercial investigation | Integrator, safety engineer, controls engineer | **Selected** |
| 4 | RV Reducer vs Harmonic Drive for Robot Joints | `rv reducer vs harmonic drive` | cycloidal drive robot, robot joint gearbox comparison | 300–800 | Medium | Commercial investigation | Mechanical engineer | Rejected: overlaps `harmonic-drive-review` and `belt-drive-vs-gear-drive` |
| 5 | Gazebo + ros2_control: Simulate a Robot Arm | `gazebo ros2 control` | gz_ros2_control, robot arm simulation tutorial, Gazebo URDF robot | 500–1,500 | Medium-High — official docs and community tutorials dominate | Informational (tutorial) | ROS 2 developer, student | Rejected: overlaps `robot-arm-simulation-software` (comparison) and `ros2-robot-arm-control` |
| 6 | Teach Pendant Programming Basics | `robot teach pendant` | teach pendant programming, robot jogging coordinates, KRL RAPID basics | 200–600 | Medium | Informational | Operator, student | Rejected: overlaps `robot-arm-programming-languages` and `robot-arm-training-program` |
| 7 | Conveyor Tracking for Robot Pick and Place | `robot conveyor tracking` | encoder-based tracking, line tracking robot, pick on the fly | 150–400 | Medium | Commercial investigation | Integrator | Rejected: demand too small for a 2,500-word resource this session |
| 8 | TCP Calibration: 4-Point Tool Frame Setup | `robot TCP calibration` | tool center point calibration, 4-point TCP method, tool frame robot | 300–700 | Medium | Informational | Technician, integrator | Rejected: would cannibalize `robot-arm-calibration` (mastering, ISO 9283) |
| 9 | Robot Cycle Time: Motion Profiles & Takt Math | `robot cycle time reduction` | S-curve motion profile, robot takt time, cycle time optimization | 200–500 | Medium | Informational | Controls engineer | Rejected: partial overlap with `robot-arm-payload-calculator` dynamics and `robot-machine-tending` timing example |

US/Canada split: Canadian share is a small fraction of combined English volume for all nine (typically 8–12%); it does not change any decision. Both countries are served by the same pages, with US (ANSI/A3, NFPA, OSHA) and Canadian (CSA) context included where applicable.

## 2. Selected articles and why they won

- **Robot arm troubleshooting (1)** — the library had no diagnostic page: every existing fault content is a sub-section (transmission troubleshooting, cable troubleshooting, singularity diagnosis). Highest-confidence ranking opportunity in a maintenance intent the site's audience already has, fully sourceable from ABB/FANUC/UR public manuals plus ISO 9283 and ISO 10218-2:2025.
- **Robot cell electrical design (2)** — a genuine gap: the site covers PLC handshakes and safety devices but never the electrical system itself. The 2024 NFPA 79 edition and the 2025 ISO 10218/CSA Z434:26 adoptions make the topic current and sourceable; design-walkthrough-with-calculations format with verified component reference prices.
- **Cobot force limit validation (3)** — the 2025–2026 standards transition (ISO 10218-2:2025 absorbing ISO/TS 15066; ANSI/A3 R15.06-2025; CSA Z434:26) left every existing safety page on this site written against the old framework. A validation-procedure article is the most current, highest-authority addition available, with a distinct intent (safety validation) from all existing pages.

The three have different primary intents (diagnostic, design/commercial investigation, safety validation) and different user problems; none targets "robot arm" broadly.

## 3. Anti-cannibalization audit

Audit basis: every HTML file in `articles/` (titles, meta descriptions, H1s, visible H2s, FAQ questions), `articles/index.html`, `index.html`, `sitemap.xml`, extracted programmatically on August 26, 2026.

### A. Robot Arm Troubleshooting — `robot-arm-troubleshooting`
Closest existing pages: `robot-arm-singularity-guide` (kinematic fault only), `robot-arm-maintenance` (scheduled care, not diagnosis), `joint-encoders-robot-arm` (component explainer). Overlap: none of their H2 sequences or intents is a symptom-to-cause triage across electrical/software/mechanical/safety domains.
**Decision: Pass.** Angle: a fault-domain method with a symptom-to-cause table, worked ISO 9283 separation calculation, and escalation boundary. Links to (rather than repeats) calibration, maintenance, encoders, cooling and e-stop pages.

### B. Robot Cell Electrical Design — `robot-cell-electrical-design`
Closest existing pages: `robot-arm-plc-integration` and `industrial-plc-robotics` (controls handshake, not electrical supply/panel design), `robot-arm-emergency-stop` (device-side safety circuit), `robot-light-curtain-integration` (device sizing). No existing page covers NFPA 79/IEC 60204-1 supply path, SCCR, control-power budgeting or conductor practice.
**Decision: Pass.** Angle: the electrical system as a design walkthrough with two worked calculations and a verified-price budget; links to the device-side pages.

### C. Cobot Force Limit Validation — `cobot-force-limit-validation`
Closest existing pages: `robot-arm-safety-usa-canada` (standards overview, pre-2025 framework), `robot-risk-assessment` (ISO 12100 method), `collaborative-assembly-arm` (cell design/ROI). None contains a PFL measurement/validation procedure, and none reflects the 2025–2026 standards stack.
**Decision: Pass with a distinct angle.** Angle: the instrumented validation procedure under ISO 10218-2:2025/ANSI-A3 R15.06-2025/CSA Z434:26, including the SSM separation-distance calculation; the article cross-links the overview and risk-assessment pages instead of restating them.

Slug check: all three slugs were absent from `articles/`, `sitemap.xml`, and the internal-link graph before insertion (verified programmatically).

## 4. Delivered articles

| | A. Troubleshooting | B. Electrical design | C. PFL validation |
|---|---|---|---|
| Slug | `robot-arm-troubleshooting` | `robot-cell-electrical-design` | `cobot-force-limit-validation` |
| Title (chars) | Robot Arm Troubleshooting: Symptom-to-Cause Diagnosis (53) | Robot Cell Electrical Design: NFPA 79 & IEC 60204-1 (51) | Cobot Force Limit Validation: ISO 10218-2 Test Plan (51) |
| Meta description (chars) | 153 | 150 | 157 |
| Primary keyword | robot arm troubleshooting | robot cell electrical design | cobot force limit validation |
| Intent / audience | Informational diagnostic; maintenance technician, controls engineer | Commercial investigation/design; controls engineer, integrator, electrician | Informational/safety validation; integrator, safety engineer |
| Structure (all three differ) | Troubleshooting with symptom-to-cause diagnosis | Design walkthrough with calculations | Maintenance/validation procedure |
| Visible main-content words | 2,885 | 2,631 | 2,615 |
| Contextual internal links | 5 | 4 | 4 |
| FAQs (visible = schema, 1:1) | 6 | 6 | 6 |

H2 sequences verified distinct across the three articles and against the nearest existing articles (`robot-arm-singularity-guide`, `robot-arm-maintenance`, `robot-arm-plc-integration`, `industrial-plc-robotics`, `robot-arm-safety-usa-canada`, `robot-risk-assessment`).

## 5. Unique value added

- **Troubleshooting:** a fault-domain triage method with a six-row symptom-to-cause table with pass criteria; a worked ISO 9283-based calculation separating backlash wear from datum/software error (0.0002 rad at a 0.6 m lever arm ≈ 0.12 mm TCP scatter); documented battery-failure behaviour cited from ABB product manuals (38213 event; 36/18-month SMB battery lifetime) and FANUC's BZAL → SRVO-075 sequence; a fault-log practice and a hard escalation boundary.
- **Electrical design:** the NFPA 79 (machine) vs NEC (building) jurisdictional split; a connected-load/SCCR sizing flow with a worked 8 kVA → 9.6 A example; an illustrative 24 VDC budget table with 80%-loading rule; NFPA 79 vs IEC 60204-1 conductor-color differences including the 2024 orange-with-blue-stripe rule; a worked voltage-drop calculation (√3·I·R, 12 AWG ≈ 1.93 Ω/kft, ≈1.4% at 100 ft); verified indicative prices (Mean Well HDR-60-24 $20.10; Phoenix Contact QUINT4-PS ≈ $193.91; NFPA 79-2024 print $139.00) with source and date.
- **PFL validation:** the first page on this site (and among the first independent English pages) explaining the 2025–2026 stack — ISO 10218-2:2025 absorbing ISO/TS 15066, ANSI/A3 R15.06-2025 Parts 1–3, CSA Z434:26 and Z434.1:26, RIA TR R15.806; the quasi-static vs transient distinction; a four-stage validation procedure; an illustrative SSM separation-distance calculation; and a validation-report content checklist. Threshold values are deliberately not reproduced — the article tells readers to read them from the current standard.

Competing English results inspected for positioning (not an exhaustive audit): OEM support/alarm pages and integrator maintenance blogs (troubleshooting); NFPA/IEC/UL pages and panel-shop blogs (electrical); ISO/A3/CSA pages and cobot-vendor safety pages (PFL). None provides the above method, calculations, or 2026 standards mapping in one place.

## 6. E-E-A-T / value layers included

| Layer | Troubleshooting | Electrical design | PFL validation |
|---|---|---|---|
| Illustrative scenario / example calculation | Weekend-power-off mastering-loss scenario + ISO 9283 backlash calculation, both labelled | 8 kVA load calc, 24 VDC budget, voltage-drop calc, all labelled | Illustrative hand-off scenario + SSM separation-distance calc, labelled |
| Indicative 2026 price / quote breakdown | Quote-breakdown framing (what a service visit should contain) | Three verified indicative prices + UL 508A panel quote categories | Quote-required measurement systems + third-party validation quote categories |
| Typical reader question | Escalation and bypass questions answered in FAQs and body | "Can I keep my 120 V AC control circuit?" pullquote | "What voids a validation?" and standards-status FAQs |
| Official sources | ABB/FANUC manuals, ISO 9283, ISO 10218-2:2025, OSHA 1910.147 | NFPA 79-2024, IEC 60204-1:2016+A1:2021, UL 508A, ISO 13849-1:2023, CSA Z434:26, OSHA | ISO 10218-1/-2:2025, ISO/TS 15066:2016, ANSI/A3 R15.06-2025, CSA Z434:26, RIA TR R15.806 |

All three carry an editorial disclosure that Robotics Engineering Lab did not buy, install, measure or test the equipment, that scenarios are illustrative, and that the work requires qualified professionals and the current standard editions. Safety content is educational and approves nothing.

## 7. Source and price caveats

- Volume estimates are directional (method and date in section 1).
- ABB/FANUC alarm behaviour is cited from public product-manual wording and widely documented alarm references; readers are told to confirm exact wording in their controller edition.
- Component prices are public distributor listings accessed August 26, 2026 (DigiKey; a US standards retailer for NFPA 79), labelled as reference ranges, not quotations and not Robotics Engineering Lab inventory.
- ISO/TS 15066 biomechanical threshold values are intentionally not reproduced; the article points to the current standard text.
- Standards move: every standards section tells readers to verify the edition enforced in their jurisdiction (noting NFPA 79 AHJ adoption lag and ISO/AWI 15066-1 in development).

## 8. Quality-control checklist

| Check | Troubleshooting | Electrical design | PFL validation |
|---|---|---|---|
| ≥ 2,500 visible main-content words | PASS — 2,885 | PASS — 2,631 | PASS — 2,615 |
| Title unique, ≤ 60 chars | PASS — 53 | PASS — 51 | PASS — 51 |
| Meta description unique, ≤ 160 chars | PASS — 153 | PASS — 150 | PASS — 157 |
| Primary keyword in title, H1, intro, relevant H2 | PASS | PASS (wiring H2 carries it) | PASS (test-equipment H2 carries it) |
| Slug unique, absent pre-insertion | PASS | PASS | PASS |
| No paragraph/H2 duplication vs site or siblings | PASS | PASS | PASS |
| Intent and reader explicit | PASS | PASS | PASS |
| Anti-cannibalization audit documented | PASS | PASS | PASS |
| Every number sourced, assumed, or labelled | PASS | PASS | PASS |
| Prices labelled indicative/reference/quote-required | PASS | PASS | PASS |
| Structure distinct, H2 order distinct | PASS | PASS | PASS |
| Standards relevant, current, not certification | PASS | PASS | PASS |
| Exactly six visible FAQs, 1:1 with FAQPage | PASS | PASS | PASS |
| JSON-LD parses (BlogPosting, FAQPage, BreadcrumbList) | PASS | PASS | PASS |
| Canonical/OG/Twitter/robots/author/dates coherent | PASS | PASS | PASS |
| ≤ 5 contextual internal links, all resolve | PASS — 5 | PASS — 4 | PASS — 4 |
| Local static server returns 200 for all three | PASS | PASS | PASS |

Site-wide checks: three sitemap entries with `lastmod` 2026-08-26 (PASS); homepage cards link to the correct slugs with unique alt text (PASS); homepage and archive ItemLists both contain positions 1–62 sequential with the three new URLs at 60–62 and `numberOfItems` 62 (PASS); visible homepage stat updated to 62 (PASS); category counts on the homepage now sum to 62 and each block's declared count matches its list (PASS); archive sections updated (PASS); no existing article, metadata block, or consent/analytics code removed — `git status` shows only the three new files plus `index.html`, `articles/index.html`, `sitemap.xml` modified (PASS).

**Follow-up recommendation (not done this session):** the existing `robot-arm-safety-usa-canada` page (lastmod 2025-06-07) predates ANSI/A3 R15.06-2025 and CSA Z434:26; schedule a refresh so the site's standards overview matches the 2026 stack described in the new PFL article.

## 9. Files created or updated

Created: `articles/robot-arm-troubleshooting.html`, `articles/robot-cell-electrical-design.html`, `articles/cobot-force-limit-validation.html`, `ARTICLES-2026-08-26-REPORT.md`.
Updated: `sitemap.xml`, `index.html`, `articles/index.html`.

## 10. Load and parse confirmation

All three article pages were served from a local static server and returned HTTP 200 with full content (44.5 KB, 42.4 KB, 42.4 KB). All JSON-LD blocks on the three pages and the updated ItemList blocks in `index.html` / `articles/index.html` were parsed as valid JSON during QC, and the sitemap parsed as valid XML with the three new URLs dated 2026-08-26.
