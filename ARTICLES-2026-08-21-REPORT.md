# Robotics Engineering Lab — Three-Article Delivery Report

**Publication date:** August 21, 2026
**Target market:** English-language readers in the USA and Canada
**Repository state:** 53 existing articles before publication; 56 after publication

## 1. Candidate topics evaluated

Search-volume figures below are directional monthly estimates for the combined US/Canada English market. The niche is B2B and technically specialised, so a lower-volume query can still be valuable when it has strong engineering or commercial intent. Estimates were triangulated from public SERP demand, related-query presence, specialist robotics keyword lists, and the typical ranges returned by public keyword tools. They are not first-party Google Search Console data and should be replaced with the site's own Search Console data when available.

| Candidate | Primary keyword | Estimated monthly volume | Difficulty | Intent | Decision |
|---|---|---:|---|---|---|
| Robot arm | `robot arm` | 5,000–12,000 | High | Informational/commercial | Rejected: broad overlap with types, guide, reviews, and buying pages |
| Robot arm programming | `robot arm programming` | 1,000–2,500 | High | Informational | Rejected: overlaps programming languages and PLC tutorials |
| Robot arm gripper | `robot arm gripper` | 1,000–2,000 | High | Commercial investigation | Rejected: end-effector, gripper-design, vacuum, and magnetic-gripper pages already cover the intent |
| Robot arm payload calculator | `robot arm payload calculator` | 700–1,500 | High | Transactional/informational | Rejected: exact calculator already exists |
| ROS 2 robot arm control | `ROS 2 robot arm control` | 500–1,200 | High | Informational | Rejected for this session: substantial overlap with `ros2-robot-arm-control` |
| MoveIt 2 Setup Assistant | `MoveIt 2 Setup Assistant` | 300–800 | Medium | Informational | Selected: distinct configuration-package workflow |
| Robot arm singularity | `robot arm singularity` | 150–400 | Medium | Informational/troubleshooting | Selected: distinct diagnosis and path-recovery intent |
| Robot arm base mounting | `robot arm base mounting` | 100–250 | Low–Medium | Commercial investigation/transactional | Selected: no existing foundation, anchor, or base-installation guide |
| Robot arm price | `robot arm price` | 1,000–3,000 | High | Commercial investigation | Rejected: leasing, ROI, market, and multiple product-cost pages already target this decision |

The selected topics were not simply the three highest-volume terms. They offer a better combination of ranking opportunity, technical sourceability, audience value, and topical separation from the existing library.

## 2. Selected articles

### A. Robot Arm Singularity: Detection & Avoidance Guide

- **Slug:** `robot-arm-singularity-guide`
- **URL:** `https://roboticsengineeringlab.com/articles/robot-arm-singularity-guide`
- **Primary keyword:** `robot arm singularity`
- **Secondary keywords:** singularity avoidance, robot singularity detection, wrist singularity, Jacobian singularity, MoveIt 2 singularity
- **Estimated volume:** 150–400 monthly searches, combined US/Canada directional estimate
- **Difficulty:** Medium
- **Search intent:** Informational and troubleshooting
- **Reader:** Controls engineer, ROS 2 developer, robotics student, and advanced maker
- **Format:** Troubleshooting guide with diagnosis and recovery workflow
- **Visible main-content word count:** 2,619
- **Value added:** A symptom-versus-diagnosis workflow that separates singularity, joint-limit, collision, TCP, and frame faults; it also explains Jacobian condition number, manipulability, path-type changes, and MoveIt 2 Servo thresholds without presenting them as a safety function.

#### Anti-cannibalization result

**PASS with a distinct angle.** The closest existing pages are:

- `robot-arm-inverse-kinematics`: explains forward/inverse kinematics and solver implementation, but does not target singularity diagnosis and recovery as its primary intent.
- `robot-arm-calibration`: covers accuracy, repeatability, mastering, and metrology; it does not explain path conditioning or singularity families.
- `robot-arm-simulation-software`: compares simulation products; it does not provide a singularity troubleshooting workflow.

The new H2 sequence — symptom diagnosis, Jacobian interpretation, singularity families, diagnostic workflow, path changes, MoveIt 2 monitoring, and production checklist — is distinct from all three pages.

### B. Robot Arm Base Mounting: Anchors, Leveling & Safety

- **Slug:** `robot-arm-base-mounting`
- **URL:** `https://roboticsengineeringlab.com/articles/robot-arm-base-mounting`
- **Primary keyword:** `robot arm base mounting`
- **Secondary keywords:** robot foundation design, robot arm anchors, robot pedestal, robot base plate, robot arm installation
- **Estimated volume:** 100–250 monthly searches, combined US/Canada directional estimate
- **Difficulty:** Low–Medium
- **Search intent:** Commercial investigation and transactional installation research
- **Reader:** Automation integrator, mechanical engineer, maintenance technician, and plant project manager
- **Format:** Installation guide organized as a load-path and commissioning workflow
- **Visible main-content word count:** 2,647
- **Value added:** A model-specific installation workflow covering reaction loads, foundation stiffness, flatness versus level, support architecture, anchor selection, locating pins, torque records, and controlled dry-run commissioning. It explicitly avoids giving generic anchor sizes as if they were engineering approval.
- **Reference prices:** Hilti and Simpson anchor listings plus a ROBOTIS accessory listing, all labelled indicative retail references rather than Robotics Engineering Lab inventory.

#### Anti-cannibalization result

**PASS.** The closest existing pages are:

- `aluminum-robot-frame`: focuses on link-material selection and CNC design, not foundation or base anchoring.
- `types-of-robotic-arms`: explains robot configurations and workspace, not installation engineering.
- `robot-arm-safety-usa-canada`: covers North American safety standards, not mechanical support design or anchor installation.
- `robot-arm-calibration`: addresses calibration and accuracy after installation, not the base load path.

The new H2 sequence — manual and anchor catalogue, base reactions, support architecture, flatness/stiffness, anchor types, installation workflow, commissioning checks, and mistakes — is not duplicated in the library.

### C. MoveIt 2 Setup Assistant: Configure a Robot Arm

- **Slug:** `moveit-2-setup-assistant-robot-arm`
- **URL:** `https://roboticsengineeringlab.com/articles/moveit-2-setup-assistant-robot-arm`
- **Primary keyword:** `MoveIt 2 Setup Assistant`
- **Secondary keywords:** MoveIt 2 robot arm setup, ROS 2 robot arm configuration, SRDF, MoveIt planning group, ros2_control MoveIt
- **Estimated volume:** 300–800 monthly searches, combined US/Canada directional estimate
- **Difficulty:** Medium
- **Search intent:** Informational/tutorial
- **Reader:** ROS 2 developer, robotics student, controls engineer, and advanced maker
- **Format:** Step-by-step software commissioning tutorial with verification checkpoints
- **Visible main-content word count:** 2,657
- **Value added:** A configuration-first explanation of URDF/Xacro, SRDF, self-collision matrices, virtual joints, planning groups, named poses, end effectors, controller mappings, and the boundary between MoveIt planning and `ros2_control` execution.

#### Anti-cannibalization result

**PASS with a distinct angle.** The closest existing pages are:

- `ros2-robot-arm-control`: explains hardware interfaces, controller managers, YAML, and the control architecture; it is not a Setup Assistant tutorial.
- `robot-arm-simulation-software`: compares RobotStudio, ROS 2/Gazebo, Webots, and Isaac Sim; it is not a package-generation workflow.
- `robot-arm-inverse-kinematics`: covers IK mathematics and code; the new article only explains solver selection as one Setup Assistant step.
- `robot-arm-controller-comparison`: compares boards; it does not configure a MoveIt package.

The new H2 sequence follows the Setup Assistant workflow and separates model, semantic configuration, planning, controller, and execution faults. It does not target the broader “ROS 2 robot arm control” query already covered by the site.

## 3. E-E-A-T/value layers included

| Article | Illustrative scenario/calculation | Reference price or cost boundary | Typical reader question | Official sources/institutions |
|---|---|---|---|---|
| Singularity guide | TCP speed and Jacobian amplification example, explicitly hypothetical | Software and hardware costs are not forced into the article because they are not needed to answer the query | Six article-specific FAQs | MoveIt 2, Universal Robots, Doosan Robotics |
| Base mounting | Hypothetical base reaction/load-path example, explicitly not a test | Hilti, Simpson, and ROBOTIS prices labelled indicative and dated | Six installation-specific FAQs | Universal Robots, ABB, Kawasaki, Home Depot/ROBOTIS listings |
| MoveIt 2 Setup Assistant | TCP frame offset example, explicitly not a test | No fabricated software price; open-source licensing is discussed as a boundary | Six setup and execution-specific FAQs | MoveIt 2, ROS 2 Control, Universal Robots |

## 4. Quality-control checklist

| Check | Singularity | Base mounting | MoveIt 2 Setup Assistant |
|---|---|---|---|
| At least 2,500 visible main-content words | PASS — 2,619 | PASS — 2,647 | PASS — 2,657 |
| Title at most 60 characters | PASS — 50 | PASS — 51 | PASS — 47 |
| Meta description at most 160 characters | PASS — 142 | PASS — 144 | PASS — 144 |
| Unique slug absent before publication | PASS | PASS | PASS |
| Search intent and reader profile stated | PASS | PASS | PASS |
| Anti-cannibalization audit completed | PASS with distinct angle | PASS | PASS with distinct angle |
| H2 structure distinct from closest existing article and the other two | PASS | PASS | PASS |
| Technical facts sourced or labelled as estimates/examples | PASS | PASS | PASS |
| Prices labelled as indicative/reference where used | PASS — no forced price | PASS | PASS — no fabricated price |
| Exactly six visible FAQs | PASS | PASS | PASS |
| Visible FAQs and FAQPage JSON-LD identical 1:1 | PASS — parsed and matched | PASS — parsed and matched | PASS — parsed and matched |
| JSON-LD types present and valid | PASS — BlogPosting, FAQPage, BreadcrumbList | PASS — BlogPosting, FAQPage, BreadcrumbList | PASS — BlogPosting, FAQPage, BreadcrumbList |
| Canonical, robots, Open Graph, Twitter metadata | PASS | PASS | PASS |
| Contextual internal links within limit | PASS — 3 article links | PASS — 3 article links | PASS — 4 article links |
| Local image paths resolve | PASS | PASS | PASS |
| Safety/professional boundaries included where relevant | PASS | PASS | PASS |

## 5. Files created or updated

Created:

- `articles/robot-arm-singularity-guide.html`
- `articles/robot-arm-base-mounting.html`
- `articles/moveit-2-setup-assistant-robot-arm.html`
- `ARTICLES-2026-08-21-REPORT.md`

Updated:

- `index.html` — three cards, homepage ItemList with 56 items, homepage count, date, and latest-section copy.
- `articles/index.html` — three visible library entries, archive ItemList, and `numberOfItems: 56`.
- `sitemap.xml` — three URLs with `<lastmod>2026-08-21</lastmod>`.

## 6. Validation performed

- Parsed all new JSON-LD blocks with Python’s JSON parser.
- Confirmed six visible FAQ pairs match six FAQPage schema pairs character-for-character.
- Confirmed title and description length limits.
- Confirmed new sitemap URLs and current last-modified date.
- Confirmed homepage and archive ItemLists contain 56 sequential positions.
- Confirmed every new local image path resolves.
- Compared the new H2 sequences and article text against the existing article inventory for exact and substantial duplication.
- Confirmed the three new HTML documents are static-server compatible and ready for local HTTP loading.
