# Robotics Engineering Lab — Three-Article Delivery Report

**Publication date:** August 25, 2026
**Target market:** English-language readers in the USA and Canada
**Repository state:** 56 existing articles before publication; 59 after publication

## 1. Candidate topics evaluated

No first-party keyword-tool data was available in this session, so all volumes below are **directional monthly estimates for the combined US/Canada English market**, triangulated on August 25, 2026 from public search-result inspection (which publishers compete on each term), related-query and "people also ask" presence, and the public ranges that keyword tools historically report for adjacent robotics terms. They are not Google Search Console data and should be replaced with the site's own data when available.

| # | Candidate (proposed title) | Primary keyword | Secondary keywords | Est. volume (US+CA, directional) | Difficulty / why | Intent | Likely reader | Decision |
|---|---|---|---|---|---|---|---|---|
| 1 | Machine Tending Robots: CNC Cell Design & Cost Guide | `machine tending robots` | cnc machine tending, robot lathe tending, machine tending cobot, lights-out machining, robot machine cell | 1,300–2,600 | Medium-High — SERP dominated by FANUC, UR and integrator application pages, but few independent engineering comparisons | Commercial investigation | Manufacturing/automation engineer, integrator, plant manager | **Selected** |
| 2 | Robot Arm Linear Rail: 7th Axis Selection & Sizing | `robot arm linear rail` | 7th axis robot, seventh axis, robot transfer unit, robot track, robot rail foundation | 400–1,000 | Low-Medium — vendor pages (Güdel, Rollon, IPR) rank, but independent sizing/engineering explainers are thin | Commercial investigation (component selection) | Integrator, mechanical engineer, maintenance lead | **Selected** |
| 3 | micro-ROS on ESP32: Robot Arm Node Tutorial | `micro-ROS` | micro-ROS ESP32, ROS 2 microcontroller, XRCE-DDS agent, ESP32 ROS 2 node, rclc tutorial | 500–1,200 (global higher) | Medium — official docs plus community tutorials rank; no dominant commercial player | Informational (tutorial) | ROS 2 developer, advanced maker, student | **Selected** |
| 4 | Stepper vs Servo Motors for Robot Arm Joints | `stepper vs servo robot arm` | closed-loop stepper, servo torque sizing, nema 17 robot arm, stepper driver robot | 1,000–2,500 | High | Informational | Maker, student | Rejected: overlaps `smart-servo-robot-arm` (servo categories, torque sizing math) |
| 5 | Robot Deburring and Finishing with Force Control | `robot deburring` | force control finishing, constant force tool, compliant deburring spindle | 200–600 | Medium | Commercial investigation | Manufacturing engineer | Rejected this session: overlaps force-torque sensor application coverage on `force-torque-sensors-robot` |
| 6 | Robot Tool Changer Selection Guide | `robot tool changer` | quick change coupler, ISO 9409-1 tool changer, pneumatic tool changer | 300–700 | Medium | Commercial investigation | Integrator, EOAT designer | Rejected: quick-change couplers already covered in `robot-end-effector-selection` |
| 7 | Safety PLC Programming for Robot Cells | `safety plc programming` | safety PLC robot cell, PLd safety logic, muting light curtain PLC | 150–400 | Medium | Informational | Controls engineer | Rejected: overlaps the e-stop, light-curtain, risk-assessment and PLC-integration safety sections |
| 8 | Robot Controller Backup and Recovery | `robot controller backup` | robot program backup, robot controller recovery, image backup FANUC | 50–150 | Low | Informational | Maintenance technician | Rejected: demand too small for a 2,500-word resource; thin official source base |
| 9 | Predictive Maintenance for Robot Arms | `robot predictive maintenance` | condition monitoring robot, vibration analysis robot joint, IIoT robot health | 300–800 | Medium-High | Informational/commercial | Maintenance lead, plant manager | Rejected: overlaps `robot-arm-maintenance`; revisit later with a condition-monitoring angle |

US/Canada split: for all nine candidates the Canadian share is a small fraction (typically 8–12% of combined English volume), which does not change any decision here; both countries are served by the same pages, with US/Canadian standards context included where applicable.

## 2. Selected articles and why they won

Scoring criteria: demand × realistic ranking opportunity, audience fit, editorial/commercial relevance, sourceability, distinctness from the existing 56 articles, and the ability to sustain a genuinely useful 2,500-word resource.

- **Machine tending (1)** — the highest-demand term with a defensible angle: manufacturer and integrator pages describe *their* products; none provide an independent cobot-vs-fenced-arm decision matrix, a two-machine timing calculation, a handshake signal table, and quotation structure in one place. Strong commercial relevance (application buying decision) and fully sourceable from FANUC America, Universal Robots, published integrator pages, and public standards.
- **Linear rail (2)** — best ranking opportunity of the session: the SERP is vendor catalogues with little independent engineering content, and the existing library covers fixed base mounting but nothing on travel axes. It serves an integrator/mechanical audience already present on the site, and every claim is anchored to published manufacturer data (Güdel TMF tables, Rollon RTU pages, IPR catalog PDF).
- **micro-ROS (3)** — the fastest-growing informational gap in the site's ROS 2 cluster: the micro-ROS project documentation itself (now at micro.vulcanexus.org) is authoritative but dense, and the site's existing ESP32 and ros2_control articles stop exactly at this boundary. Tutorial format with checkpoints is reproducible from official docs.

The three selected topics have distinct primary intents and user problems: application cell design (plant team deciding *how* to automate machining), component selection (integrator sizing a travel axis for an existing cell), and an informational build/commissioning tutorial (developer putting an MCU into a ROS 2 graph).

## 3. Anti-cannibalization audit

Audit basis: every HTML file in `articles/`, `articles/index.html`, `index.html`, `sitemap.xml`, plus the title, H1, visible H2s, FAQ questions and related links of each existing article (extracted programmatically on August 25, 2026).

### A. Machine Tending Robots — `robot-machine-tending`

Closest existing pages:

- `/articles/palletizing-robot-arm` — application guide, but for palletizing queries (sizing, patterns, EOAT, palletizing safety); different application and keyword set.
- `/articles/robot-arm-plc-integration` — PLC/fieldbus handshake architecture, not application sizing or part presentation.
- `/articles/collaborative-assembly-arm` — assembly-cell safety/design/ROI, not machine-tool tending.
- `/articles/robot-arm-safety-usa-canada` — standards explainer, cited here rather than competed with.

**Decision: Pass with a distinct angle.** The angle: the first application-design page in the library targeting machine-tending queries, organized around a cobot-vs-fenced-industrial-arm decision matrix plus a two-machine timing example. No existing H2 overlaps (verified). The new article links to, rather than repeats, the PLC, safety, and palletizing pages.

### B. Robot Arm Linear Rail — `robot-arm-linear-rail`

Closest existing pages:

- `/articles/robot-arm-base-mounting` — fixed-base installation (foundation, anchors, flatness); the rail article covers travel, drive, moment, environment, and controls constraints that mounting does not, and links to it for the load-path detail.
- `/articles/cable-management-robot` — dress packs; linked, not duplicated (only the energy-chain line item overlaps).
- `/articles/palletizing-robot-arm` and `/articles/types-of-robotic-arms` — no rail-selection content.

**Decision: Pass.** No existing page targets rail/seventh-axis keywords or contains rail sizing content. Slug `robot-arm-linear-rail` was absent from `articles/`, `sitemap.xml`, and all internal links before insertion (verified).

### C. micro-ROS on ESP32 — `microros-esp32-robot-arm`

Closest existing pages:

- `/articles/esp32-robot-controller` — ESP32 as a standalone PWM/Wi-Fi controller, no ROS; the new article is the ROS 2-node architecture and links to it for wiring.
- `/articles/ros2-robot-arm-control` — Linux-side ros2_control (hardware interfaces, controllers); the new article explicitly states micro-ROS does not put ros2_control on the MCU and cross-references it.
- `/articles/moveit-2-setup-assistant-robot-arm` — planning configuration; different query and reader stage.

**Decision: Pass with a distinct angle.** The angle: the MCU-side ROS 2 boundary (client–agent–DDS-XRCE) with commissioning checkpoints, which none of the existing ROS 2 pages cover. Cross-checked the three new topics against each other: no shared H2 sequences, intents, or primary keywords.

## 4. Delivered articles

| | A. Machine tending | B. Linear rail | C. micro-ROS |
|---|---|---|---|
| Slug | `robot-machine-tending` | `robot-arm-linear-rail` | `microros-esp32-robot-arm` |
| Title (chars) | Machine Tending Robots: CNC Cell Design & Cost Guide (53) | Robot Arm Linear Rail: 7th Axis Selection & Sizing (51) | micro-ROS on ESP32: Robot Arm Node Tutorial (43) |
| Meta description (chars) | 136 | 149 | 140 |
| Primary keyword | machine tending robots | robot arm linear rail | micro-ROS |
| Intent / audience | Commercial investigation; manufacturing engineer, integrator, plant manager | Commercial investigation (component); integrator, mechanical engineer, maintenance lead | Informational tutorial; ROS 2 developer, advanced maker, student |
| Structure (all three differ) | Comparison with decision matrix | Selection guide organized by constraints | Build/commissioning tutorial with checkpoints |
| Visible main-content words | 3,806 | 3,530 | 3,178 |
| Contextual internal links | 5 | 5 | 5 |
| FAQs (visible = schema, 1:1) | 6 | 6 | 6 |

H2 sequences were verified distinct across the three articles and against the nearest existing articles (`palletizing-robot-arm`, `robot-arm-base-mounting`, `esp32-robot-controller`, `moveit-2-setup-assistant-robot-arm`).

## 5. Unique value added

- **Machine tending:** an 8-factor cobot-vs-fenced-arm decision matrix; a minimum handshake signal table with failure handling; a fully stated two-machine timing/spindle-utilization calculation (31 s tending, 66 s robot work in a 95 s cut window, 77.9% spindle utilization); a quotation line-item structure; and coolant-exposure maintenance practice from UR's official CNC tending guidance.
- **Linear rail:** a constraint-ordered selection method with two worked calculations (carriage tilting moment ≈ 1,272 N·m static for a stated 250 kg robot + 60 kg riser + 30 kg wrist load; trapezoidal move time 3.7 s over 6 m at 2 m/s, 3 m/s²); a drive-type comparison; and a manufacturer data table compiled only from official Güdel, Rollon, and IPR publications with access date.
- **micro-ROS:** a client–agent–DDS-XRCE architecture walkthrough grounded in the current official docs (including the micro.ros.org → micro.vulcanexus.org move); four verifiable commissioning checkpoints with pass criteria and deliberate failure tests; an agent build/run procedure from eProsima documentation; and a message-budget calculation (115200 baud ≈ 11,520 B/s → ~128 msg/s ceiling for a ~90-byte JointState).

Competing English-language results inspected for positioning (not an exhaustive audit): FANUC America's and Universal Robots' machine-tending pages and two integrator cost pages (machine tending); Güdel, Rollon, and IPR product pages plus a dealer listing (rails); the official micro-ROS documentation, eProsima Micro XRCE-DDS docs, and community ESP32/ROS 2 tutorials (micro-ROS). These are the same sources cited in the articles. None of the inspected competitor pages provides the above calculations, matrices, or checkpoint flows.

## 6. E-E-A-T / value layers included

| Layer | Machine tending | Linear rail | micro-ROS |
|---|---|---|---|
| Illustrative scenario / example calculation | Two-machine timing and spindle-utilization example, labelled illustrative | Carriage-moment and move-time calculations, labelled illustrative | Serial-bandwidth message budget, labelled planning arithmetic |
| Price transparency | Published 2026 integrator/cobot reference ranges, labelled, with sources and dates; no CAD conversion invented | Quote-required framing with mandatory quotation line items; no invented street price | Indicative 2026 price: Adafruit ESP32-S3-DevKitC-1 $15.95/$19.95 USD, dated and sourced |
| Typical reader question | Manual lathe door automation | Cobot on a belt track without a foundation | Why not plain serial strings instead of micro-ROS |
| Official sources | FANUC America, Universal Robots (application + CNC maintenance), ANSI/RIA R15.06, CSA Z434, ISO 10218-2, OSHA | Güdel, Rollon, IPR, ANSI/RIA R15.06, CSA Z434, ISO 10218-2 | micro-ROS docs (micro.vulcanexus.org), eProsima Micro XRCE-DDS, docs.ros.org, Espressif/Adafruit |

All three pages carry an editorial disclosure stating that Robotics Engineering Lab did not buy, install, or test the equipment, and that industrial figures come from documentation. Safety sections are educational, point to qualified integrators/controls engineers and the current standard editions, and are not presented as risk assessments or legal advice.

## 7. Source and price caveats

- Volume estimates are directional (method and date stated in section 1).
- Machine-tending cost ranges are published third-party figures (US integrator and cobot-supplier pages, 2026), labelled as reference ranges, not quotations and not Robotics Engineering Lab inventory; Canadian pricing left as quote-dependent.
- Rail pricing is deliberately quote-required with a mandatory line-item list; the ±0.02 mm repeatability figure is attributed to a dealer listing of a small Güdel TMF unit, official figures (±0.04 mm Rollon, ±0.1 mm IPR) are from manufacturer pages.
- Firmware in the micro-ROS article is presented as a reference skeleton adapted from official examples — explicitly not claimed as compiled or run by the site.
- Standards editions move: the articles tell readers to consult current editions (noting the 2025 revision cycle of ISO 10218 rolling into national adoptions).

## 8. Quality-control checklist

| Check | Machine tending | Linear rail | micro-ROS |
|---|---|---|---|
| ≥ 2,500 visible main-content words | PASS — 3,806 | PASS — 3,530 | PASS — 3,178 |
| Title unique, ≤ 60 chars | PASS — 53 | PASS — 51 | PASS — 43 |
| Meta description unique, ≤ 160 chars | PASS — 136 | PASS — 149 | PASS — 140 |
| Primary keyword in title, H1, intro, and a relevant H2 | PASS | PASS (first H2 edited to include it) | PASS |
| Slug unique and absent before insertion | PASS | PASS | PASS |
| No substantial paragraph/H2 duplication with existing or other new articles | PASS (only boilerplate template strings shared) | PASS | PASS |
| Intent and reader explicit | PASS | PASS | PASS |
| Anti-cannibalization audit documented | PASS with distinct angle | PASS | PASS with distinct angle |
| Technical data sourced, assumed, or labelled estimate | PASS | PASS | PASS |
| Prices labelled indicative/reference/quote-required; not REL inventory | PASS | PASS | PASS |
| Structure differs from other two and nearest existing article | PASS — decision matrix | PASS — constraint-ordered selection | PASS — checkpoint tutorial |
| Standards/safety relevant, current enough, not certification or legal advice | PASS | PASS | PASS (no industrial standards forced; scope limits stated) |
| Exactly six visible FAQs | PASS | PASS | PASS |
| Visible FAQs match FAQPage JSON-LD 1:1 | PASS — programmatically compared | PASS | PASS |
| JSON-LD valid with required types | PASS — BlogPosting, FAQPage, BreadcrumbList | PASS | PASS |
| Canonical, OG, Twitter, robots, author, publisher, dates, images coherent | PASS | PASS | PASS |
| ≤ 5 contextual internal article links | PASS — 5 | PASS — 5 | PASS — 5 |
| All internal links and local image paths resolve | PASS | PASS | PASS |
| HTML parses without structural errors; page loads on local server | PASS — HTTP 200 | PASS — HTTP 200 | PASS — HTTP 200 |

Site-wide:

- sitemap.xml: three new no-trailing-slash URLs with `<lastmod>2026-08-25</lastmod>`, existing style preserved — PASS (68 URLs, no duplicates).
- Homepage: 3 new cards with correct slugs/images/dates; ItemList extended to 59 sequential positions; `numberOfItems` 59; visible stat 59; category grid counts reconciled to 59 items (pre-existing staleness from the August 21 session — moveit/singularity/base-mounting entries — also corrected) — PASS.
- articles/index.html: three visible entries in the correct categories (Industrial automation & safety; Mechanical design & materials; ROS 2, kinematics & software); CollectionPage ItemList extended to 59 sequential positions; `numberOfItems` 59; archive canonical/navigation unchanged — PASS.
- No existing article, metadata block, or legal/consent code removed (git diff reviewed; deletions limited to the three swapped homepage cards and count labels) — PASS.

## 9. Files created or updated

Created:

- `articles/robot-machine-tending.html`
- `articles/robot-arm-linear-rail.html`
- `articles/microros-esp32-robot-arm.html`
- `articles/diagram-machine-tending.jpg` (original AI-generated editorial illustration)
- `articles/diagram-linear-rail.jpg` (original AI-generated editorial illustration)
- `articles/diagram-microros-esp32.jpg` (original AI-generated editorial illustration)
- `ARTICLES-2026-08-25-REPORT.md`

Updated:

- `sitemap.xml` — three URLs with `<lastmod>2026-08-25</lastmod>`
- `index.html` — three cards, ItemList 59, homepage stat 59, category grid reconciliation
- `articles/index.html` — three visible entries, ItemList 59, `numberOfItems: 59`

## 10. Validation performed before delivery

- All JSON-LD blocks in the three new articles, `index.html`, and `articles/index.html` parsed with Python's JSON parser (all valid; ItemList positions 1–59 sequential on both index pages).
- The six visible FAQ pairs in each article were compared character-for-character against the FAQPage schema (exact match, including punctuation and apostrophes).
- Title and meta-description lengths measured programmatically.
- Word counts measured from visible text inside `<main>` (navigation, hero, metadata, schema, and boilerplate excluded).
- Every contextual internal link and local image path resolved to an existing file (clean-URL mapping checked against `.html` files); H2 text and 8-word content shingles compared across all 59 articles for duplication.
- All three pages, the homepage, the archive, and the three new diagrams returned HTTP 200 from a local static server (`python3 -m http.server`), and the three HTML documents were parsed with an HTML parser with no structural errors.
