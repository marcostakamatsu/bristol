# Bristol Machine Company — Website Redesign Plan
## Phase 3: Sitemap Strategy

---

## 1. Pages to Keep, Restructure, Merge, or Add

### Keep (with significant improvements)
| Page | Action | Reason |
|---|---|---|
| Home | Redesign | Core entry point — needs new hero, social proof, and trust signals |
| About Us | Redesign | Good bones, needs structure, testimonials, and certifications |
| Contact | Redesign | Strong CTA concept, weak execution |
| Fabricated Products | Rebuild | Good category, needs inline specs and better layout |
| Distributed Products | Rebuild | Good category, same issues as above |
| All 5 Industry Pages | Rebuild | Exist but are thin — need real landing page treatment |

### Restructure
| Page | Action | Reason |
|---|---|---|
| Products | Create hub page | Currently no top-level Products page, just sub-nav dropdowns |
| Services | Expand and restructure | Exists at `/rentals-and-repairs/` but covers only TONE Shear Wrench repair/rental; URL and nav label are misaligned; scope needs to reflect the full service offering |
| Industries | Create hub page | No top-level Industries overview — just sub-nav items |

### Merge
| Current | Merge Into | Reason |
|---|---|---|
| News (under About) | Resources section | Too buried as an About sub-page; better as its own lightweight section |
| Specifications (under Products) | Each product page | Inline specs belong on the product page itself, not a separate page |
| Finishes/Coatings (under Products) | Fabricated Products or Services | Too granular for its own nav item |

### Add (New)
| Page | Reason |
|---|---|
| Products hub page | Navigation anchor; SEO value; overview of both product lines |
| Industries hub page | Gives users a clear entry point before choosing a vertical |
| Resources page | Spec sheets, certifications, downloads — high SEO and trust value |
| Thank You page | Post-quote-form submission; needed for conversion tracking |

---

## 2. Why Each Page Earns Its Place

**Home** — The single highest-traffic page. Needs to do three things: establish who Bristol is, surface both product lines, and drive the quote CTA. Every section is purposeful.

**About Us** — B2B buyers research the company before buying. 44 years of history, a physical facility, and a values-based culture are competitive advantages. This page makes the trust case.

**Products (hub)** — Without a hub page, users who land on the site without knowing whether they need fabricated or distributed products have no clear starting point. The hub solves navigation for first-time visitors and anchors the Products section for SEO.

**Fabricated Products** — Custom fabrication is Bristol's hardest-to-replicate capability. It deserves its own well-structured home with product cards, spec tables, and a quote CTA.

**Distributed Products** — Brand-name products (Simpson Strong-Tie, ITW Red Head, etc.) signal legitimacy and purchasing power. Needs clear organization and product-level pages.

**Services** — Tool Repair & Rental is a unique differentiator and an active revenue stream. The page exists but is limited to TONE Shear Wrench repair and rental only, and its URL (`/rentals-and-repairs/`) doesn't match the "Services" nav label. The redesign should expand the scope, align the URL, and position the service offering more prominently.

**Industries (hub)** — Gives buyers in specific verticals a clear entry point. Also anchors five SEO-targeted sub-pages.

**5 Industry Landing Pages** — Each vertical (Alternative Energy, Curtain Wall, Industrial Fasteners, Marine, Structural Steel) has distinct product needs and search behavior. Proper landing pages capture high-intent traffic and speak directly to each buyer type.

**Resources** — Spec sheets and certifications are table stakes for procurement decisions in this industry. A downloadable resources page removes friction from the buying process and builds SEO authority.

**Contact** — The conversion endpoint for the entire site. Must be clean, fast, and trustworthy.

**Thank You** — Needed for Google Analytics / GA4 goal tracking after quote form submission. Often overlooked, always necessary.

---

## 3. Navigation Structure

```
Home
Products
  └── Fabricated Products
        └── Anchor Bolts
        └── Clevis Assemblies
        └── Full Thread Rod
        └── Hex Bolt Modifications
        └── Single-End Rods
        └── Double-End Rods
        └── U-Bolts
  └── Distributed Products
        └── All Thread Rod
        └── Powers Fasteners (Black & Decker)
        └── Concrete Anchors
        └── Drill Bits
        └── ITW Red Head
        └── Simpson Strong-Tie
        └── TC Bolts
        └── TONE Shear Wrenches
        └── Assorted Bolts, Screws, Nuts & Washers
Services
Industries
  └── Alternative Energy & Utilities
  └── Curtain Wall
  └── Industrial Fasteners
  └── Marine Fasteners
  └── Structural Steel Fastener Systems
Resources
About Us
Contact
```

This structure:
- Reduces the current nav from 6 top-level items with buried sub-items to a cleaner hierarchy
- Gives Products and Industries proper hub pages as landing points
- Removes Specifications and Finishes/Coatings as standalone nav items (absorbed into relevant pages)
- Surfaces Resources as a first-class nav item instead of burying News under About

---

## 4. User Journeys to Prioritize

**Journey 1: "I need a specific fastening product, fast"**
→ Home → Products (hub) → Fabricated or Distributed → Product page → Request a Quote
This is the highest-frequency journey. Every step must be frictionless.

**Journey 2: "I need a supplier for my industry"**
→ Home → Industries (hub) → Industry landing page → Products → Request a Quote
This journey converts well when industry pages speak the buyer's language.

**Journey 3: "I'm evaluating Bristol vs. a competitor"**
→ Home → About Us → Standards & Certifications → Contact
Trust signals, history, and values are the deciding factors here.

**Journey 4: "I need tool repair or a rental"**
→ Home → Services → Contact
Short and direct. Services must be findable in the main nav.

**Journey 5: "I need a spec sheet or certification document"**
→ Home → Resources → Download
Removes a friction point that currently doesn't have a solution on the site.

---

## 5. How the Sitemap Supports Brand and Business Goals

| Business Goal | Sitemap Solution |
|---|---|
| Generate quote requests | Every page ends with a Request a Quote CTA; Thank You page enables tracking |
| Communicate dual capability (distribute + fabricate) | Products hub makes both lines equally visible at the same level |
| Build trust with new buyers | About page + certifications section + testimonials |
| Capture SEO traffic from industry searches | 5 rebuilt industry landing pages with keyword-targeted content |
| Retain and serve existing clients | Resources page with spec sheets and downloadable docs |
| Reflect the personal service brand | Contact page design + phone number surfaced everywhere |
| Support future content marketing | Resources/News section provides infrastructure |
