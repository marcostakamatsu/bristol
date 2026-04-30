# Bristol Machine Company — Website Redesign
## Full Project Plan

---

## Project Overview

The goal is to completely recreate the Bristol Machine Company website inside WordPress using Elementor. Before building the sitemap or designing anything, the project follows a structured discovery and planning process to ensure every decision is grounded in the brand, the audience, and the current site's real strengths and weaknesses.

---

## Materials Reviewed

- Brand Guide: `Brand Guide/BRISTOL_brand-guide_250904_V2.pdf`
- Website Audit 1: `Audits/Bristol Machine Company - Website Audit.docx`
- Website Audit 2: `Audits/BRISTOL - Website Audit.docx`
- SEO Audit: `Audits/Bristol Machine Company - SEO Audit.pdf`
- Current website: https://bristolmachinecompany.com/
- Logo files: `Assets/Logos/`
- Icon library: `Assets/Icons/`

---

## Phase 1 — Brand Analysis

**Goal:** Build a complete picture of Bristol's brand before touching the sitemap.

**Deliverable:** `01_Brand-Analysis.md`

Covers:
- Brand positioning and business model (distributor + fabricator)
- Target audience definition (industries served, buyer type, decision-maker profile)
- Tone of voice (what the current website says vs. what the brand guide prescribes)
- Visual identity: colors, typography, logo usage rules, iconography
- What the website must communicate based on the brand

**Key findings:**
- Design philosophy: **Modern Industrial Authority** — industrial, technical, trustworthy, direct, professional, established, conversion-focused
- Brand attributes: Hardworking · Trusted · Relational · Serving · Innovative
- Brand values: excellent customer service, unparalleled work ethic, customer-centered decision-making, innovative customized solutions, industry-leading reliability
- Primary brand color: Navy Blue `#1f3b70` + Black `#000000`
- Supporting blues: `#4c628d`, `#7989a9`, `#a5b1c6`
- Grays: `#616160`, `#a5a5a4`, `#e9e9e9`
- Typography: Helvetica Neue LT — Heavy for headings, Roman for body, Light for captions and supporting display copy. Single family, three weights, no exceptions.
- Font files: `Assets/Fonts/`
- No tagline or mission statement defined
- Core differentiator: Bristol both distributes AND fabricates — undersold on the current site
- Target audience: professional B2B buyers (engineers, procurement managers, specialty contractors)
- Tone: Expert, accessible, accountable, and authoritative — defensible superlatives allowed when tied to brand attributes

---

## Phase 2 — Website Audit

**Goal:** A structured audit that clearly separates confirmed findings from existing audits vs. new findings from live review.

**Deliverable:** `02_Website-Audit.md`

**Section A — Confirmed findings (from audit documents):**
- Boxed layout, not full-width (High)
- Header misaligned, icons inconsistent (High)
- Hero oversized, typography too small (High)
- Content boxes outdated (Medium)
- Content sections unbalanced, font too large (Medium)
- Footer completely empty (Critical)
- No inner page banners (Medium)
- Contact page unstructured (Medium)
- Section spacing inconsistent (Medium)
- Submenu hover too subtle (Low)
- Multiple font families in headings (High)
- Banner too tall on all devices (Medium)

**Section B — New findings (live review):**
- Services page exists at `/rentals-and-repairs/` but scope is too narrow; URL/nav label mismatch (Medium)
- Footer copyright reads "1975–2019" — outdated by 6+ years (High)
- Industry pages thin and templated — no real differentiation per vertical (High)
- No social proof anywhere on the site (High)
- No trust signals or certifications displayed prominently (High)
- Navigation depth — Distributed Products has 9 sub-items, unwieldy on mobile (Medium)
- No resources or content section (Medium)
- Product pages lack inline specs (Medium)
- Homepage value proposition too generic (Medium)
- No SEO structure visible across pages (Medium)
- Only LinkedIn, poorly surfaced (Low)

---

## Phase 3 — Sitemap Strategy

**Goal:** Before building the sitemap, align on the reasoning behind every page decision.

**Deliverable:** `03_Sitemap-Strategy.md`

Covers:
- Pages to keep, restructure, merge, or add — with rationale for each
- Why each page earns its place in the new site
- Proposed navigation structure
- 5 user journeys to prioritize
- How the sitemap supports brand and business goals

**Key decisions:**
- Add Products hub page and Industries hub page (currently both are nav-only, no landing page)
- Expand Services page beyond TONE Shear Wrench only; align URL with nav label
- Merge Specifications and Finishes/Coatings into relevant product pages (too granular as standalone nav items)
- Move News out from under About Us into a new Resources section
- Add Resources as a first-class nav item
- Add Thank You page for conversion tracking

---

## Phase 4 — Full Sitemap

**Goal:** A production-ready sitemap — not just page names, but a working spec for every page.

**Deliverable:** `04_Full-Sitemap.md`

**13 pages defined**, each with:
- Full section structure in order
- Purpose of each section
- Recommended CTA
- Content and UX notes
- Elementor implementation notes

**Pages covered:**
1. Home
2. Products (hub)
3. Fabricated Products (hub)
4. Individual Fabricated Product pages — template × 7
5. Distributed Products (hub)
6. Individual Distributed Product pages — template × 9
7. Services
8. Industries (hub)
9. Industry landing pages — template × 5
10. Resources
11. About Us
12. Contact
13. Thank You (hidden from nav)

**Global elements defined:** Header, Footer, Inner Page Banner template, spacing system, color system, typography setup, form recommendations, SEO tooling, and mobile breakpoints.

---

## Phase 5 — Brand Direction Review

**Goal:** Validate Phases 1–4 against the **Modern Industrial Authority** direction and propagate the resulting changes through the planning artifacts.

**Deliverable:** `05_Brand-Direction-Review.md`

**Key outcomes:**
- Brand attributes updated to Hardworking · Trusted · Relational · Serving · Innovative across all planning files
- Brand values updated to excellent customer service, unparalleled work ethic, customer-centered decision-making, innovative customized solutions, industry-leading reliability
- Tone-of-voice rule relaxed to allow defensible superlatives tied to brand claims
- Visual rule updated: industrial textures and technical patterns are allowed as low-opacity accents on navy sections; soft decorative elements (gradients, illustrations, ornaments) remain forbidden
- Homepage Why Bristol cards re-anchored to the five brand attributes
- About Us values cards re-anchored to the five brand attributes
- Datasheet styling specified for product specs and Resources document list
- Spec ribbons added to product cards on Products and Fabricated Products hubs
- Subtle technical-pattern overlay specified for navy backgrounds (Standards strip, Inner Page Banner template)
- Heading weight locked: HelveticaNeueLT-Heavy

---

## Phase 6 — Homepage Build (Static Reference)

**Goal:** Deliver a working static HTML/CSS implementation of the Homepage as a stakeholder-ready prototype and as the Elementor reference.

**Deliverable:** `06_Homepage-Build.md` + `Build/Homepage/index.html` + `Build/Homepage/style.css`

**Key outcomes:**
- All 8 homepage sections from the approved sitemap built in order, no deviations
- Final approved copy from `Copy/Homepage.md` used verbatim
- Real Bristol assets used throughout — logos, fonts, icons, and product photography from `Assets/`
- Navbar (sticky on scroll, mobile hamburger) and Footer (4 columns + dynamic copyright year) implemented as global components
- Modern Industrial Authority direction reflected: navy/black palette, Helvetica Neue LT Heavy headings, square corners, CSS blueprint-grid pattern on navy sections, industrial photography in hero and feature cards
- Tokenized design system on `:root` — direct one-to-one mapping to Elementor Global Colors
- Responsive across desktop, tablet, mobile (320px to 1440px)
- Inline JavaScript only — sticky header, mobile menu toggle, auto copyright year. No external dependencies
- **WCAG 2.1 Level AA audited and compliant** — three issues found and fixed (quote-card contrast, separator-dot contrast, skip link added). Full audit and known limitations documented in Phase 6
- Elementor migration notes included — every component pattern maps to a native Elementor Pro widget or template

---

## Pre-Build Decisions Still Open

Most pre-build decisions were resolved during Phase 6. Items still pending before site-wide build/launch:

1. ~~**Technical-pattern asset**~~ — Resolved on the homepage as a CSS-only blueprint grid; can be swapped for a custom SVG/PNG asset if Bristol prefers.
2. **Photography sourcing for inner pages** — Hero and What We Do cards on the homepage use existing Bristol photography. Industry landing pages, About, and product pages still need image selection / licensing for unique-per-page assets.
3. **Icon style audit for inner pages** — Homepage selection is consistent. Confirm the broader library at `Assets/Icons/` is uniformly line OR filled before building remaining pages.
4. **Real testimonials** — Replace the three "to confirm" placeholders with real client quotes before launch.

---

## Next Steps

With Phases 1–6 complete, the project moves into broader execution:

1. **Stakeholder approval** — Review the static Homepage in `Build/Homepage/` and sign off on the build direction
2. **Copy for remaining pages** — Apply the same copy framework used for the Homepage (`Copy/Homepage.md`) to Products, Industries, Services, Resources, About, and Contact
3. **Build remaining pages** — Replicate the design system from `Build/Homepage/` for each remaining page
4. **Migrate to WordPress / Elementor** — Implement the static reference inside Elementor Pro using the migration notes in `06_Homepage-Build.md`
5. **Content entry** — Populate pages with approved copy, images, spec sheets
6. **QA & launch** — Real-device testing, manual screen-reader audit (NVDA / VoiceOver / JAWS), SEO metadata, GA4 conversion tracking, performance pass (image compression, lazy-loading)
