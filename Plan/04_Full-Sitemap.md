# Bristol Machine Company — Website Redesign Plan
## Phase 4: Full Sitemap

---

## Design Direction

All pages below follow the **Modern Industrial Authority** direction defined in `01_Brand-Analysis.md` and reviewed in `05_Brand-Direction-Review.md`:

- Industrial, technical, trustworthy, direct, professional, established, conversion-focused
- Helvetica Neue LT — Heavy for headings, Roman for body, Light for captions
- Navy `#1f3b70` + Black `#000000` as the dominant industrial palette
- Square or lightly rounded (2–4px) corners on cards, buttons, form fields
- Subtle technical patterns / metal textures as accents on navy sections (low opacity)
- Industrial photography only — facility, fastener macro, application contexts
- Brand attributes (Hardworking · Trusted · Relational · Serving · Innovative) anchor the homepage Why Bristol cards and the About Us attribute cards

---

## Site Structure Overview

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
Thank You (hidden from nav)
```

---

## Global Elements

### Header (all pages)
- Logo left — color version (navy background, white type)
- Navigation center/right — Products, Services, Industries, Resources, About Us
- Right side — LinkedIn icon + phone number (909.598.8601) + "Request a Quote" button (navy, bold, square corners)
- Sticky on scroll; collapses to hamburger on mobile
- Elementor note: Use Elementor Pro Header template. Sticky behavior via Elementor Sticky settings. Mobile breakpoint at 768px. All headings/buttons in HelveticaNeueLT-Heavy.

### Footer (all pages)
- Column 1: Logo (white version) + one-line company description
- Column 2: Quick Links — Products, Services, Industries, Resources, About Us, Contact
- Column 3: Contact info — address, phone, email, hours
- Column 4: LinkedIn icon + "Request a Quote" button
- Bottom bar: Copyright © 1975–[current year] Bristol Machine Company | Privacy Policy
- Background: Navy `#1f3b70` | Text: White
- Elementor note: Use dynamic year widget or PHP shortcode for auto-updating copyright year.

---

## Page 1 — Home

**Purpose:** Establish who Bristol is, communicate the dual distribute + fabricate capability, surface industries and products, and drive quote requests.

**Primary CTA:** Request a Quote
**Secondary CTA:** Explore Products

---

### Section 1 — Hero
- Full-width, edge-to-edge
- Background: dark industrial photography (facility, product, or application context) with navy + black gradient overlay, or navy with darkened metal-texture overlay
- Uppercase eyebrow label above H1 (e.g., *"DISTRIBUTOR · FABRICATOR · SINCE 1975"*) in HelveticaNeueLT-Heavy, small caps, light blue `#a5b1c6`
- H1: Specific, differentiating headline — e.g., *"Southern California's Trusted Fastening Distributor & Fabricator Since 1975"*
- Subheadline: One sentence on the value prop — availability, fabrication, service
- CTA buttons: "Request a Quote" (primary, white fill, square corners) + "Explore Products" (secondary, outlined white)
- Elementor note: Elementor Section with background image, navy `#1f3b70` to black `#000000` gradient overlay at 75–85% opacity. H1 in HelveticaNeueLT-Heavy, white, tight tracking. Min-height 600px desktop, 400px mobile.

### Section 2 — Trust Bar
- Narrow full-width strip, light gray `#e9e9e9` background
- 4–5 items inline: *Founded 1975 · Southern California · ASTM Certified · AISC Compliant · No Voicemail — Real People Answer*
- Elementor note: Single-row Elementor section, icon list or text columns. 60px height desktop.

### Section 3 — What We Do
- Two equal columns, white background
- Section eyebrow line above the cards: *"Distributed. Fabricated. Both, under one roof."* — reinforces the dual-capability differentiator before the cards split apart
- Left card: **Fabricated Products** — icon, headline, 2-line description, "Explore Fabricated Products" link
- Right card: **Distributed Products** — icon, headline, 2-line description, "Explore Distributed Products" link
- Each card has a subtle border, square corners, and hover elevate effect
- Elementor note: 2-column section with a single-line heading row above. Card hover animation via Elementor motion effects (translate Y, subtle, 200–300ms ease).

### Section 4 — Industries We Serve
- Light gray `#e9e9e9` background
- Section title: "Industries We Serve"
- 5-card icon grid: Alternative Energy & Utilities, Curtain Wall, Industrial Fasteners, Marine Fasteners, Structural Steel
- Each card: industry icon (from icon library), industry name, 1-line description, arrow link
- Elementor note: Elementor grid widget or 5-column inner section. Use existing SVG icons. Cards link to respective industry landing pages.

### Section 5 — Why Bristol
- White background
- Section title: "Why Work With Bristol"
- 6 feature cards in 3×2 grid, each anchored to a brand attribute:
  - **Hardworking** — *"Unparalleled Work Ethic"*
  - **Trusted** — *"Industry-Leading Reliability"* (certifications + traceability)
  - **Relational** — *"Real People, No Voicemail"*
  - **Serving** — *"Customer-Centered From Quote to Delivery"*
  - **Innovative** — *"Custom Fabrication Built to Your Spec"*
  - **Established** — *"44+ Years Serving Southern California"*
- Each card: icon, bold title, 1-sentence description
- Elementor note: Use icon box widget. Icons from existing library, single style mode (line OR filled, not mixed). Grid layout 3 columns desktop, 2 tablet, 1 mobile. Square corners on cards.

### Section 6 — Standards & Certifications
- Navy `#1f3b70` background with subtle technical pattern overlay (blueprint grid, fastener silhouette, or thin diagonal hatching at <10% opacity), white text
- Section title: "Standards We Fabricate To"
- Badge/logo strip or styled text list: ASTM · AISC · AASHTO · F1554-36 · F1554-55 · F1554-105 · A193-B7 · A354-BD · A449 · A325 · A490
- One-line description: "Every fabricated product ships with full traceability and certification documentation."
- Elementor note: Icon list or styled text columns. White text on navy. Background pattern via Elementor section background image (PNG/SVG) at low opacity. No actual external logos needed — typographic treatment is sufficient.

### Section 7 — Testimonials
- Light gray `#e9e9e9` background
- Section title: "What Our Clients Say"
- 2–3 testimonial cards: quote, client name, company, industry
- Elementor note: Testimonial carousel or static 3-column grid. Client content to be provided by Bristol. Placeholder copy needed at build time.

### Section 8 — CTA Banner
- Full-width, navy `#1f3b70` background
- Headline: *"Ready to find the right fastening solution?"*
- Subtext: *"Our team responds fast. And yes — a real person will answer when you call."*
- CTA: "Request a Quote" (white button) + phone number prominent
- Elementor note: Full-width section. Centered text layout. Button links to Contact page.

---

## Page 2 — Products (Hub)

**Purpose:** Orient first-time visitors between the two product lines and direct them efficiently to the right category.

**Primary CTA:** Explore Fabricated Products / Explore Distributed Products

---

### Section 1 — Inner Page Banner
- Full-width, navy background with subtle technical pattern overlay (blueprint grid / fastener silhouette / diagonal hatching at <10% opacity), or industrial photo with navy + black gradient overlay
- H1: "Our Products"
- Subtitle: "From custom-fabricated anchor systems to name-brand distributed hardware — everything your project needs, in one place."
- Elementor note: Reusable inner banner template — applied to every non-homepage page. H1 in HelveticaNeueLT-Heavy white, subtitle white at reduced opacity. 300px height desktop. Background pattern stored as a global SVG/PNG asset and reused across all inner banners.

### Section 2 — Product Lines Split
- Two large cards side by side, white background
- Left: **Fabricated Products** — image, headline, description (what fabrication means, why it matters), "Explore Fabricated Products" button
- Right: **Distributed Products** — image, headline, description (brands stocked, availability), "Explore Distributed Products" button
- Elementor note: 2-column section. Cards with border and hover effect. Equal heights via Elementor stretch columns.

### Section 3 — Fabricated Products Preview
- Section title: "Custom Fabricated"
- 4-card horizontal grid: featured fabricated products (Anchor Bolts, Clevis Assemblies, Full Thread Rod, U-Bolts)
- Each card: product image/icon, name, 1-line description, **spec ribbon** (single line of meta — material grades, finishes, or applicable standards), "View Product" link
- Elementor note: 4-column inner section. Card style consistent with homepage cards. Spec ribbon as a single-line text row inside the card, separated by middle dots.

### Section 4 — Distributed Products Preview
- Section title: "Distributed Brands & Products"
- 4-card horizontal grid: featured brands (Simpson Strong-Tie, ITW Red Head, Powers Fasteners, TC Bolts)
- Each card: brand logo or product image, name, 1-line description, "View Product" link
- Elementor note: Same card style as above.

### Section 5 — Standards Strip
- Navy background
- "We fabricate to ASTM, AISC, AASHTO, and all major structural standards. Full certification packages available."
- Elementor note: Same as homepage Standards section — reuse template.

### Section 6 — CTA Banner
- Headline: *"Can't find what you're looking for?"*
- Subtext: "Our team can source or fabricate almost any fastening product. Get in touch."
- CTA: "Request a Quote" + phone number

---

## Page 3 — Fabricated Products (Hub)

**Purpose:** Showcase Bristol's custom fabrication capability and provide entry points to all 7 product types.

**Primary CTA:** Request a Quote

---

### Section 1 — Inner Page Banner
- H1: "Fabricated Products"
- Subtitle: "Custom-engineered fastening solutions fabricated in-house to your exact specifications."

### Section 2 — Fabrication Intro
- Two-column: text left, facility/shop image right
- Text: What "in-house fabrication" means for the buyer — speed, spec control, traceability, certification packages
- Highlight: "Rapid-turn fabrication shop. Your parts, built to spec, ready when you need them."
- Elementor note: 2-column section, image on right with object-fit cover.

### Section 3 — Product Grid
- Section title: "Our Fabricated Products"
- 7 product cards in a 3–4 column grid: Anchor Bolts, Clevis Assemblies, Full Thread Rod, Hex Bolt Modifications, Single-End Rods, Double-End Rods, U-Bolts
- Each card: product image or icon, product name, 1-line description, **spec ribbon** (material grades · finishes · applicable standards), "View Details" button
- Elementor note: Elementor grid or posts widget if products are built as CPT. Cards link to individual product pages. Square corners, spec ribbon as single-line text row.

### Section 4 — Finishes & Coatings
- Section title: "Available Finishes & Coatings"
- List or icon grid: Hot-Dip Galvanized, Zinc Plated, Plain/Black, Stainless Steel, Others on request
- One-line note: "All finishes available with full traceability documentation."
- Elementor note: Icon list widget or styled column list.

### Section 5 — Standards
- Section title: "Standards We Fabricate To"
- Styled badge list: F1554-36, F1554-55, F1554-105, A193-B7, A354-BD, A449, A307, A325, A490
- Elementor note: Navy background strip — reuse global template.

### Section 6 — CTA Banner
- Headline: *"Need a custom specification? We can build it."*
- CTA: "Request a Quote" + phone

---

## Page 4 — Individual Fabricated Product Pages (Template × 7)

*Applies to: Anchor Bolts, Clevis Assemblies, Full Thread Rod, Hex Bolt Modifications, Single-End Rods, Double-End Rods, U-Bolts*

**Purpose:** Convert a buyer who knows what they need into a quote request. Provide enough technical detail to confirm Bristol can meet the spec.

**Primary CTA:** Request a Quote for [Product Name]

---

### Section 1 — Inner Page Banner
- H1: Product name
- Breadcrumb: Products > Fabricated Products > [Product Name]
- Elementor note: Breadcrumb widget via Elementor Pro or custom HTML.

### Section 2 — Product Overview
- Two-column: description left, product image right
- Description: what it is, how it's used, industries that use it
- Elementor note: Image on right with lightbox option for close-up.

### Section 3 — Specifications Table
- Section title: "Specifications"
- Table: Material grades, diameter range, length range, thread type, applicable standards
- Visual treatment: **datasheet style** — navy `#1f3b70` header row with white text, monospace font for spec values where appropriate, thin gray `#a5a5a4` row dividers, no zebra striping or pastel fills
- Elementor note: HTML table or Elementor table widget. Styled with brand colors for header row. Monospace via Elementor Custom CSS or class.

### Section 4 — Finishes Available
- Small section or inline callout: list of finishes available for this product
- Elementor note: Can be collapsed into Section 3 table as an additional row.

### Section 5 — Related Products
- Section title: "You May Also Need"
- 3 cards linking to other fabricated products
- Elementor note: Static cards — no need for dynamic posts if volume is small.

### Section 6 — CTA Banner
- Headline: *"Request a Quote for [Product Name]"*
- Subtext: "Specify your requirements and our team will respond promptly."
- CTA: "Request a Quote" + phone

---

## Page 5 — Distributed Products (Hub)

**Purpose:** Present the range of name-brand products Bristol stocks and direct buyers to specific product pages.

**Primary CTA:** Request a Quote

---

### Section 1 — Inner Page Banner
- H1: "Distributed Products"
- Subtitle: "Name-brand construction and industrial hardware, stocked and ready to ship from our Rancho Cucamonga facility."

### Section 2 — Distribution Intro
- Two-column: text + warehouse/inventory image
- Text: What "distributed" means (authorized distributor, deep stock, fast availability), brands carried, why this matters for project procurement
- Elementor note: Mirror layout of Fabricated Products intro.

### Section 3 — Product Grid
- 9 product/brand cards: All Thread Rod, Powers Fasteners (Black & Decker), Concrete Anchors, Drill Bits, ITW Red Head, Simpson Strong-Tie, TC Bolts, TONE Shear Wrenches, Assorted Hardware
- Each card: brand logo or product image, name, 1-line description, "View Details" button
- Elementor note: Same card style as fabricated products grid.

### Section 4 — CTA Banner
- Headline: *"Looking for a specific brand or product?"*
- Subtext: "If we stock it, we can ship it fast. If we don't, we'll source it."
- CTA: "Request a Quote" + phone

---

## Page 6 — Individual Distributed Product Pages (Template × 9)

*Applies to: All Thread Rod, Powers Fasteners, Concrete Anchors, Drill Bits, ITW Red Head, Simpson Strong-Tie, TC Bolts, TONE Shear Wrenches, Assorted Hardware*

**Purpose:** Confirm product availability and specifications for a buyer ready to order or quote.

**Primary CTA:** Request a Quote

---

### Section 1 — Inner Page Banner
- H1: Product or brand name
- Breadcrumb: Products > Distributed Products > [Product Name]

### Section 2 — Product Overview
- Two-column: description left, product/brand image right
- Description: product type, typical applications, why Bristol stocks it

### Section 3 — Product Variants / Available SKUs
- Table or bulleted list: sizes, grades, configurations available
- Visual treatment: same **datasheet style** as Fabricated Products — navy header row, monospace spec values, thin gray dividers
- Elementor note: Styled table consistent with fabricated product pages.

### Section 4 — Applications
- Where this product is typically used (industries, project types)
- Elementor note: Icon list or simple 3-column card grid.

### Section 5 — Related Products
- 3 cards linking to other distributed products

### Section 6 — CTA Banner
- Headline: *"Ready to order or need a custom quote?"*
- CTA: "Request a Quote" + phone

---

## Page 7 — Services

**Purpose:** Present the full Bristol service offering (currently only repair/rental — scope to be expanded). Convert visitors with specific service needs into contact requests.

**Primary CTA:** Contact Us / Request a Quote

---

### Section 1 — Inner Page Banner
- H1: "Services"
- Subtitle: "Custom problem-solving, rapid-turn fabrication, and hands-on support — beyond just product supply."

### Section 2 — Services Overview
- Brief intro paragraph leading with **innovative customized solutions and rapid-turn capability**, not just repair/rental: Bristol's service offering exists to solve the problems standard catalogs can't — custom fabrication consultations, certification packaging, and specialized tool service that keeps projects moving.
- Elementor note: Centered single-column text, max-width 800px.

### Section 3 — Service Cards
- 2–4 cards (expandable as Bristol adds services):
  - **TONE Shear Wrench Repair** — icon, description, turnaround info, CTA
  - **TONE Shear Wrench Rental** — icon, description, rental terms, CTA
  - *(Future)* Custom Fabrication Consultation
  - *(Future)* Certification & Documentation Packages
- Elementor note: 2-column card grid desktop, 1-column mobile. Cards with border and icon. Mark future services as "Coming Soon" or omit until ready.

### Section 4 — How It Works
- Section title: "How Our Service Process Works"
- 3-step horizontal flow: 1. Contact Us → 2. We Assess & Quote → 3. Service Delivered
- Elementor note: Icon + number + text layout. Navy step numbers.

### Section 5 — CTA Banner
- Headline: *"Need a repair, rental, or don't see what you're looking for?"*
- Subtext: "Call us. A real person will answer."
- CTA: "Contact Us" + phone number prominently displayed

---

## Page 8 — Industries (Hub)

**Purpose:** Give industry-specific buyers a clear entry point and orient them toward the landing page most relevant to their work.

**Primary CTA:** Explore [Industry]

---

### Section 1 — Inner Page Banner
- H1: "Industries We Serve"
- Subtitle: "Specialized fastening solutions for the projects that build and power Southern California."

### Section 2 — Industries Intro
- One short paragraph: Bristol serves specialized industrial verticals with products and fabrication capabilities tailored to each application's unique demands.
- Elementor note: Centered text, max-width 700px.

### Section 3 — Industry Cards Grid
- 5 large cards: one per industry
- Each card: industry icon (from icon library), industry name, 2-line description of what Bristol provides for this vertical, "Learn More" button
- Elementor note: 3-column grid desktop (3+2 layout), 2-column tablet, 1-column mobile. Cards with hover effect — navy background on hover, white text.

### Section 4 — Standards Strip
- "From solar arrays to structural steel — we fabricate and supply to the standards your projects demand."
- Standards badge list
- Elementor note: Navy background strip, same as global template.

### Section 5 — CTA Banner
- Headline: *"Don't see your industry listed?"*
- Subtext: "We work across many industrial and construction sectors. Get in touch to discuss your requirements."
- CTA: "Contact Us"

---

## Page 9 — Industry Landing Pages (Template × 5)

*Applies to: Alternative Energy & Utilities, Curtain Wall, Industrial Fasteners, Marine Fasteners, Structural Steel Fastener Systems*

**Purpose:** Convert a buyer who arrives from search or nav with a specific industry need. Page must speak their language and demonstrate Bristol's domain knowledge.

**Primary CTA:** Request a Quote

---

### Section 1 — Inner Page Banner
- H1: Industry name
- Subtitle: Industry-specific value statement (unique per page)
- Background: industry-relevant photo with navy overlay

### Section 2 — Industry Overview
- Two-column: text left, **one industry-specific application photograph** right (solar farm, steel structure, marine dock, curtain wall facade, etc.) — must be unique per industry, not stock or recycled
- Text: What Bristol provides for this specific industry, key challenges Bristol solves, relevant experience
- Content must be unique per industry — not templated copy. Templated copy here breaks the trustworthy/established feel more than any other failure on the site.
- Elementor note: Photo should show the industry context. Avoid generic warehouse or hand-shake stock.

### Section 3 — Products for This Industry
- Section title: "Products Commonly Used in [Industry]"
- 4–6 product cards linking to relevant product pages
- Elementor note: Static card grid. Product selection unique per industry page.

### Section 4 — Applications
- Section title: "Typical Applications"
- 3-column icon + text list of specific use cases
- Example for Structural Steel: *Beam-to-column connections · High-strength bolted assemblies · Tension control installations · Bridge and highway structures*
- Elementor note: Icon list widget, 3 columns.

### Section 5 — Why Bristol for [Industry]
- 3–4 differentiator callouts specific to this vertical
- Example for Alternative Energy: certifications relevant to solar/wind, inventory of stainless and A307 fasteners, experience with ground-mount and rooftop arrays
- Elementor note: Feature list or small card grid. Not generic — content unique per page.

### Section 6 — Standards & Certifications
- Standards relevant to this industry (varies per vertical) — at least **one industry-specific standard or certification highlighted prominently** to anchor authority for that vertical
- Elementor note: Inline styled list or badge strip. Navy background with the same subtle technical pattern overlay used in the global standards strip.

### Section 7 — CTA Banner
- Headline: *"Ready to source for your [Industry] project?"*
- Subtext: "Request a quote and our team will respond promptly with exactly what you need."
- CTA: "Request a Quote" + phone

---

## Page 10 — Resources

**Purpose:** Provide spec sheets, certifications, and standards references that support procurement decisions. Surface news/updates. Build SEO authority through technical content.

**Primary CTA:** Download / Contact Us

---

### Section 1 — Inner Page Banner
- H1: "Resources"
- Subtitle: "Spec sheets, certification documents, standards references, and company updates."

### Section 2 — Spec Sheets & Downloads
- Section title: "Spec Sheets & Technical Documents"
- Filterable or categorized list of downloadable PDFs presented in **datasheet style** — each row reads like a real spec entry (title, standard reference, file size, format, download button), not a marketing card
- Categories: Fabricated Products · Distributed Products · Material Standards · Certifications
- Visual treatment: navy header row, monospace metadata where appropriate, thin gray dividers, square buttons. Consistent with the product specifications table styling.
- Elementor note: Can be built with Elementor repeater or a simple ACF/custom field setup in WordPress. PDF files hosted in WordPress Media Library. Avoid blog-style cards — this should feel like a procurement document portal.

### Section 3 — Standards Reference
- Section title: "Standards We Fabricate To"
- Table: Standard name, description, applicable products
- Example rows: F1554-36 (Anchor bolts, 36 ksi yield), A193-B7 (Alloy steel stud bolts for high-temp), A325 (Structural bolts, high-strength), etc.
- Elementor note: HTML table styled with brand colors.

### Section 4 — News & Updates
- Section title: "News & Updates"
- 3–6 news cards: title, date, excerpt, "Read More" link
- Absorbs the current News sub-page from under About Us
- Elementor note: WordPress Posts widget filtered by "News" category. Card layout.

### Section 5 — CTA Banner
- Headline: *"Can't find the document you need?"*
- Subtext: "Contact our team and we'll get you the right certification or spec sheet."
- CTA: "Contact Us" + email address

---

## Page 11 — About Us

**Purpose:** Build trust with buyers evaluating Bristol against competitors. Tell the company story, demonstrate expertise, and humanize the brand.

**Primary CTA:** Request a Quote / Contact Us

---

### Section 1 — Inner Page Banner
- H1: "About Bristol Machine Company"
- Subtitle: "44 years of fastening expertise, built on honesty, quality, and a commitment to your project's success."

### Section 2 — Company Story
- Two-column: text left, facility image right
- Text: Founded 1975, Rancho Cucamonga CA, grew from local fabricator to regional distributor + fabricator, what makes the team and facility unique
- Pull quote: *"We don't have voicemail. When you call, a person answers."*
- Elementor note: Image right with slight navy accent border or overlay. Pull quote styled in larger italic text.

### Section 3 — By the Numbers
- Stats strip, navy background
- 4 stats: 44+ Years in Business · Southern California's Leading Fastening Supplier · Thousands of Products in Inventory · 100% Quality Guaranteed
- Elementor note: Counter widget or static text. White numbers on navy. Animate on scroll optional.

### Section 4 — Brand Attributes
- Section title: "What Defines Bristol"
- 5 cards: **Hardworking · Trusted · Relational · Serving · Innovative**
- Each: icon (from existing icon library), attribute name in bold, 2-line description tying to one of the brand values (excellent customer service, unparalleled work ethic, customer-centered decision-making, innovative customized solutions, industry-leading reliability)
- Elementor note: 5-column grid desktop (or 3+2 layout), 2–3 column tablet, 1-column mobile. Square corners. Single icon style mode.

### Section 5 — Our Facility
- Section title: "Our Facility"
- Image gallery or 2–3 column photo grid: fabrication shop, inventory, team
- Brief text: "Our Rancho Cucamonga facility houses one of the region's most extensive fastener inventories alongside a rapid-turn fabrication shop."
- Elementor note: Elementor image gallery widget or 3-column image grid.

### Section 6 — Certifications & Standards
- Same as homepage — reuse global template
- Elementor note: Global section template.

### Section 7 — Testimonials
- Same 2–3 testimonial cards as homepage
- Elementor note: Reuse global testimonial template.

### Section 8 — CTA Banner
- Headline: *"Ready to work with a team that actually picks up the phone?"*
- CTA: "Request a Quote" + phone

---

## Page 12 — Contact

**Purpose:** Convert. Every visitor who reaches this page should leave as a lead. Minimize friction, maximize trust.

**Primary CTA:** Submit Quote Request Form

---

### Section 1 — Inner Page Banner
- H1: "Contact Us"
- Subtitle: "We respond fast. And when you call — a real person answers."

### Section 2 — Contact Split
- Two-column layout:
  - **Left — Request a Quote Form:** Name, Email, Phone, Company Name, Message / Project Details, File Upload (optional). Form styled like a **quote sheet** — clean labels above each field, square corners, navy submit button. No multi-step wizard or progress bar — overkill for B2B quote requests.
  - **Right — Contact Details:** Address (with Google Map embed below), Phone, Email, Business Hours
- Elementor note: 60/40 column split (form wider). Form via WPForms or Gravity Forms. Map via Google Maps Elementor widget. Sticky right column optional on desktop.

### Section 3 — Trust Reinforcement
- Narrow strip: *"We do not have voicemail. Monday–Friday, 7am–5pm, a real person will answer at 909.598.8601."*
- Elementor note: Light gray background, centered text, icon (phone). Simple and direct.

---

## Page 13 — Thank You (Hidden from Navigation)

**Purpose:** Confirm form submission, set expectations, and keep the visitor engaged. Required for conversion tracking in GA4.

**URL:** /thank-you/

---

### Section 1 — Confirmation
- Large centered section, white background
- Icon: checkmark (from icon library)
- H1: "Thank You — We've Received Your Request"
- Subtext: "A member of our team will review your request and get back to you shortly."
- Elementor note: Full-height section. Centered layout. No header CTA button on this page.

### Section 2 — What Happens Next
- 3-step horizontal flow:
  1. We review your request
  2. We prepare your quote
  3. We reach out — usually within 1 business day
- Elementor note: Icon + step number + text. Consistent with Services "How It Works" layout.

### Section 3 — Continue Exploring
- Section title: "While You Wait"
- 3 cards: Browse Products → Browse Industries → Download Resources
- Elementor note: 3-column card grid. Internal links only.

### Section 4 — Direct Contact
- Narrow strip: "Need to reach us directly? Call 909.598.8601 — no voicemail, no bots."
- Elementor note: Navy background, white text, phone number prominent.

---

## Implementation Notes (Elementor / WordPress)

| Item | Recommendation |
|---|---|
| Page builder | Elementor Pro |
| Theme | Hello Elementor (lightweight, fully compatible) |
| Header/Footer | Elementor Theme Builder — single global template |
| Inner page banner | Elementor Theme Builder — reusable template with dynamic title |
| Typography | Upload Helvetica Neue LT font files from `Assets/Fonts/` (Heavy, Roman, Light) via Elementor > Custom Fonts. Define each weight as a custom font family entry. |
| Color system | Define all brand colors in Elementor > Global Colors |
| Spacing system | Define consistent section padding in Elementor > Global Settings (80px desktop, 50px tablet, 36px mobile) |
| Product pages | Build as WordPress Custom Post Type (CPT) if future scaling is planned; static Elementor pages acceptable for V1 |
| Forms | WPForms or Gravity Forms — both integrate natively with Elementor |
| Thank You tracking | GA4 conversion event on /thank-you/ page load |
| SEO | Yoast SEO or Rank Math — define metadata for every page at build time |
| Map | Google Maps Elementor widget on Contact page |
| Downloads | Host PDFs in WordPress Media Library; link directly |
| Mobile | Test all pages at 390px (iPhone 14) and 768px (iPad) breakpoints |
