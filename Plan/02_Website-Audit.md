# Bristol Machine Company — Website Redesign Plan
## Phase 2: Website Audit

---

## Structure

The audit is divided into two clear sections:

- **A — Confirmed findings** from the two existing audit documents
- **B — New findings** from my own live review of the site

---

## A. Confirmed Findings (from Audit Documents)

### A1. Layout — Boxed/Card-Style Structure
The entire site is constrained to a centered container with spacing on all sides. The layout feels boxed and outdated. Hero and banner sections suffer most — they should be full-width and edge-to-edge.
**Recommendation:** Convert to full-width layout. Use edge-to-edge sections strategically, especially for the hero, CTAs, and footer.

---

### A2. Header — Height, Alignment & Icon Inconsistency
The header is too tall. The logo is on the left, the nav is aligned toward the logo rather than right-aligned, social icons are on the opposite side from the contact icon, and the contact icon uses a different style from the social icons.
**Recommendation:** Reduce header height. Right-align navigation and all icons. Unify icon style across the entire header.

---

### A3. Banner / Hero Section — Oversized with Weak Content
The hero banner is disproportionately tall relative to the content inside it. Headlines and body text are too small, leaving excessive empty space. The overall impression is flat and unengaging.
**Recommendation:** Redesign the hero as a full-width, high-impact section. Increase typography scale. Add a clear, styled CTA button. Consider a background image or dark overlay.

---

### A4. Content Boxes — Outdated Design
The card/box components used throughout the site look dated — flat, unstyled, with no depth or visual hierarchy.
**Recommendation:** Redesign with modern card styles — subtle border, shadow, or elevated effect. Keep consistent across all pages.

---

### A5. Content Sections — Unbalanced Layout & Oversized Text
Several content sections use a single-column layout with font sizes that are too large for body copy, resulting in a "zoomed-in" feel. CTAs within these sections are poorly styled and easy to miss.
**Recommendation:** Move to a two-column layout (text + image). Reduce body font size to standard readable scale. Style CTA buttons consistently.

---

### A6. Footer — Completely Empty
The footer has no content whatsoever. This is a significant usability and trust issue. Users expect to find navigation, contact info, and social links in the footer.
**Recommendation:** Build a full footer with: logo + tagline, navigation links, contact details, social media icons, and copyright. Optional: newsletter signup.

---

### A7. Inner Pages — No Banner Section
All inner pages (About, Products, Industries, Contact) lack a page banner below the header. This makes inner pages feel disconnected from the design system and visually plain.
**Recommendation:** Add a consistent inner page banner to every non-homepage page — page title, optional subtitle, and relevant background.

---

### A8. Contact Page — Wide, Unstructured Layout
The contact page stretches content across the full width without column structure, making it feel unorganized and visually disconnected from the rest of the site.
**Recommendation:** Redesign with a two-column layout — contact form on one side, contact details and map on the other.

---

### A9. Section Spacing — Inconsistent Padding
Top and bottom spacing between sections is inconsistent throughout the site. Some sections appear cramped, others float in excessive whitespace.
**Recommendation:** Establish a consistent spacing system in Elementor (e.g., 80px top/bottom for major sections, 40px for minor). Apply globally.

---

### A10. Submenu Hover States — Too Subtle
When hovering over dropdown navigation items, the color change is minimal and barely perceptible. Users can't easily tell what's selected.
**Recommendation:** Apply a visible background highlight or clear color shift on hover for all submenu items.

---

### A11. Typography — Too Many Font Families
The current site uses multiple font families across headings, creating visual inconsistency and a lack of brand cohesion.
**Recommendation:** Enforce a single font family across the entire site — Helvetica Neue LT, Heavy for headings, Roman for body, Light for captions and large display subtext. No exceptions.

---

### A12. Banner Height — Excessive on All Devices
The banner height is oversized on desktop, tablet, and mobile. With limited content inside, the result looks empty on every device.
**Recommendation:** Scale banner height proportionally to content volume. On mobile especially, tighten height significantly.

---

## B. New Findings (Live Review)

### B1. Services Page — Exists but Narrow in Scope
The Services page exists at `/rentals-and-repairs/` but the nav labels it simply "Services," creating a mismatch between user expectation and content. The page covers only TONE Shear Wrench repair and rental — a very specific service. There is no mention of other potential services (custom fabrication support, tool calibration, etc.), and the URL slug does not reflect the nav label.
**Severity:** Medium
**Recommendation:** Rebuild the Services page with a broader scope that reflects the full service offering. Align the URL slug with the nav label. The TONE Shear Wrench content should be one card within a fuller services overview — not the entire page.

---

### B2. Footer Copyright — Outdated by 6+ Years
The footer copyright reads "1975–2019." It is currently 2026. This signals to visitors that the site is not actively maintained.
**Severity:** High
**Recommendation:** Update copyright to dynamic current year. Ensure all date references on the site are accurate.

---

### B3. Industry Pages — Thin, Templated Content
Each of the five industry pages follows the same template with minimal differentiation. Copy is generic and interchangeable. There is no industry-specific product callout, no application context, and no unique selling point per vertical.
**Severity:** High
**Recommendation:** Rebuild each industry page as a proper landing page — specific use cases, relevant products, industry certifications, and targeted CTA. These pages are a major SEO opportunity being wasted.

---

### B4. No Social Proof Anywhere on the Site
The site has no testimonials, no client logos, no case studies, and no project references. For a 44-year-old company with "long-term clients," this is a missed trust-building opportunity.
**Severity:** High
**Recommendation:** Add a testimonials section to the homepage and About page. Consider a "Clients & Partners" logo strip. Case studies would be ideal but optional for V1.

---

### B5. No Trust Signals / Certifications
Material standards (F1554, A193-B7, A354-BD, A325, A490, ASTM, AISC, AASHTO) are mentioned in product copy but not displayed as visible trust badges or callouts. These are critical purchase criteria for the target audience.
**Severity:** High
**Recommendation:** Create a "Standards & Certifications" section or badge strip, visible on the homepage, product pages, and About page.

---

### B6. Navigation Depth — Distributed Products Buried
The Distributed Products submenu has 9 items and Fabricated Products has 7. This creates a long, unwieldy dropdown with no visual hierarchy. On mobile, this is especially problematic.
**Severity:** Medium
**Recommendation:** Restructure the Products section with a megamenu or dedicated Products landing page that acts as a hub, reducing dropdown depth.

---

### B7. No Resources or Content Section
There is no blog, knowledge base, spec sheet library, or downloadable resources. Competitors who publish technical content (installation guides, material comparisons, spec charts) own search results for high-intent queries.
**Severity:** Medium
**Recommendation:** Add a Resources section in V1 — at minimum a spec sheet downloads page and a simple news/updates section (the site already has a News sub-page under About that is unexploited).

---

### B8. Product Pages — No Inline Specs
Product pages name the product but provide no inline technical specifications. Users must already know what they're looking for. There is no filtering, no spec table, no downloadable datasheet.
**Severity:** Medium
**Recommendation:** Each product page should include a basic spec table and a link to download the relevant certification document or spec sheet.

---

### B9. Homepage Value Proposition — Generic
The current hero copy ("Solutions that optimize availability, productivity, cost and quality from a team dedicated to your success!") is well-intentioned but generic — it could describe almost any B2B service company. It does not mention fastening, fabrication, or what makes Bristol specifically different.
**Severity:** Medium
**Recommendation:** Rewrite the hero headline to be specific and differentiating. Lead with the dual capability (distribute + fabricate), the industry context, and the service commitment.

---

### B10. No SEO Structure Visible
Page titles, H1s, and meta descriptions appear to be generic or missing across the site. The industry pages in particular represent high-value keyword opportunities (e.g., "structural steel fasteners Southern California") that are currently not being captured.
**Severity:** Medium
**Recommendation:** Define SEO metadata for every page in the sitemap. Industry and product pages should be built around specific keyword targets.

---

### B11. LinkedIn Is the Only Social Channel Listed
The site references LinkedIn only. For an industrial B2B company, this is acceptable, but the link is in the footer area — which is currently empty — making it effectively invisible.
**Severity:** Low
**Recommendation:** Surface the LinkedIn link in the header and footer consistently. Evaluate whether other channels (YouTube for product demos, Instagram for facility/culture) are worth adding.

---

## Summary Table

| # | Finding | Source | Severity |
|---|---|---|---|
| A1 | Boxed layout, not full-width | Audit | High |
| A2 | Header misaligned, icons inconsistent | Audit | High |
| A3 | Hero oversized, typography too small | Audit | High |
| A4 | Content boxes outdated | Audit | Medium |
| A5 | Content sections unbalanced, font too large | Audit | Medium |
| A6 | Footer completely empty | Audit | Critical |
| A7 | No inner page banners | Audit | Medium |
| A8 | Contact page unstructured | Audit | Medium |
| A9 | Section spacing inconsistent | Audit | Medium |
| A10 | Submenu hover too subtle | Audit | Low |
| A11 | Multiple font families | Audit | High |
| A12 | Banner too tall on all devices | Audit | Medium |
| B1 | Services page exists but is narrow in scope; URL/nav mismatch | Live review | Medium |
| B2 | Footer copyright "1975–2019" | Live review | High |
| B3 | Industry pages thin and templated | Live review | High |
| B4 | No social proof anywhere | Live review | High |
| B5 | No trust signals / certifications | Live review | High |
| B6 | Navigation too deep, unwieldy dropdowns | Live review | Medium |
| B7 | No resources or content section | Live review | Medium |
| B8 | Product pages lack inline specs | Live review | Medium |
| B9 | Homepage value prop too generic | Live review | Medium |
| B10 | No SEO structure visible | Live review | Medium |
| B11 | Only LinkedIn, poorly surfaced | Live review | Low |
