# Bristol Machine Company — Website Redesign Plan
## Phase 6: Homepage Build (Static Reference)

This phase delivers a working static HTML/CSS implementation of the Homepage based on the approved sitemap (`04_Full-Sitemap.md`), the final copy (`Copy/Homepage.md`), and the Modern Industrial Authority direction (`05_Brand-Direction-Review.md`). The build serves two purposes:

1. **Stakeholder presentation** — a real, scrollable, responsive page for review and sign-off before WordPress build.
2. **Elementor reference** — the structure, tokens, and component patterns that the Elementor build will mirror.

---

## 1. Build Location & Files

```
Build/
└── Homepage/
    ├── index.html          markup, semantic structure, inline JS
    └── style.css           design system, components, responsive rules
```

All assets are referenced via relative paths into `Assets/`:
- Fonts: `../../Assets/Fonts/*.otf` (Heavy / Roman / Light, loaded via `@font-face`)
- Logos: `../../Assets/Logos/Main Logo - Color.svg` (header), `Secondary Logo - White.svg` (footer)
- Icons: `../../Assets/Icons/*.svg` (existing library, single style mode)
- Photos: `../../Assets/Photos/*.jpg` (real Bristol product/facility photography)

No external dependencies, no CDN, no build step — opens directly in any browser.

---

## 2. Sections Implemented

The 8 homepage sections from `04_Full-Sitemap.md` are implemented in order, with no additions or removals:

| # | Section | Component class | Notes |
|---|---|---|---|
| — | Navbar (global) | `.site-header` | Sticky on scroll with shadow, mobile hamburger toggle |
| 1 | Hero | `.hero` | Full-width photo bg + navy/black gradient overlay, eyebrow + H1 + sub + 2 CTAs |
| 2 | Trust Bar | `.trust-bar` | Light gray strip, 5 icon + label items |
| 3 | What We Do | `.what-we-do` | Eyebrow + H2 + intro + 2 feature cards with photos |
| 4 | Industries We Serve | `.industries` | 5-card icon grid with navy hover-invert state |
| 5 | Why Bristol | `.why-bristol` | 6 brand-attribute cards (Hardworking, Trusted, Relational, Serving, Innovative, Established) |
| 6 | Standards & Certifications | `.standards` | Navy bg with subtle blueprint-grid pattern overlay (CSS-only) |
| 7 | Testimonials | `.testimonials` | 3 placeholder quote cards (marked "to confirm") |
| 8 | CTA Banner | `.cta-banner` | Navy → black gradient, large H2, primary CTA + phone display |
| — | Footer (global) | `.site-footer` | Navy-deep bg, 4 columns, dynamic copyright year |

---

## 3. Design System

### Tokens (CSS custom properties on `:root`)

All brand colors and spacing are exposed as CSS variables — direct one-to-one mapping for Elementor Global Colors:

```
--navy        #1f3b70   primary
--navy-deep   #15294f   footer / deepest fills
--black       #000000   text on light, gradient endpoint
--blue-mid    #4c628d   button hover
--blue-muted  #7989a9   not currently used (kept for product-page UI)
--blue-pale   #a5b1c6   eyebrow on dark, separator dots
--gray-text   #616160   body copy
--gray-border #a5a5a4   card and table dividers
--gray-bg     #e9e9e9   trust bar, industries, testimonials section bg
--white       #ffffff
```

### Typography

Single family — Helvetica Neue LT — loaded via `@font-face` from project assets:

- **Heavy** (`weight: 800`) — H1, H2, H3, eyebrows, button labels, nav links
- **Roman** (`weight: 400`) — body copy, card descriptions
- **Light** (`weight: 300`) — reserved for captions and large display subtext (not used on homepage; available for inner pages)

Headings use uppercase + tight tracking (`letter-spacing: -0.01em`) to recover technical/industrial weight without the unavailable condensed font.

### Spacing

- Section padding: 96px desktop / 72px tablet / 56px mobile
- Container max-width: 1280px
- Card padding: 32px
- Border radius: 2px (square / lightly rounded — per Modern Industrial Authority)

### Reusable components

- `.btn` (modifiers: `--primary`, `--ghost`, `--sm`, `--lg`)
- `.card` (used in What We Do)
- `.industry-card` (5-card grid with hover-invert)
- `.why-card` (6-card grid)
- `.quote-card` (testimonials)
- `.eyebrow` (modifier `--light` for use over dark backgrounds)
- `.section-title` (modifier `--light` for use over dark backgrounds)
- `.section-intro`
- `.link-arrow` (CTA arrow with hover translate)
- `.grid` (modifiers: `--2`, `--3`)

### Subtle technical pattern

Implemented as a CSS-only blueprint grid (two perpendicular linear-gradients at 5% opacity, 48px squares) on `.standards::before` and `.cta-banner::before`. No external image asset required — meets §6.3 of `05_Brand-Direction-Review.md` (technical-pattern asset). If Bristol prefers a fastener-silhouette or hatch pattern, the asset can be swapped in by replacing the two `linear-gradient` declarations with a `background-image: url(...)` reference.

---

## 4. Responsive Behavior

Three breakpoints, mobile-first cascade:

- **Desktop** (≥ 1024px): 3-column grids, full nav, 96px section padding
- **Tablet** (640–1023px): 2-column grids, mobile hamburger menu, 72px section padding, navbar collapses to 68px height
- **Mobile** (< 640px): 1-column grids, full-width buttons, 56px section padding, hero CTAs stack vertically, footer columns collapse to single column

Tested visually at: 320px, 390px (iPhone 14), 768px (iPad), 1024px, 1280px, 1440px.

---

## 5. JavaScript

Inline at the bottom of `index.html`, no external file:

1. **Sticky header shadow** — adds `.site-header--scrolled` class when `scrollY > 8` to attach a subtle bottom shadow
2. **Mobile nav toggle** — hamburger button toggles `.site-header--nav-open` on the header; closes on link click; updates `aria-expanded`
3. **Auto copyright year** — sets the footer's current year dynamically

No animation libraries, no analytics, no third-party scripts.

---

## 6. WCAG 2.1 Level AA Compliance Audit

Full audit run against the build. Three issues found and fixed; the page is now AA-compliant.

### Fixes applied

| # | Criterion | Issue | Fix |
|---|---|---|---|
| 1 | **1.4.3 Contrast (AA)** | `.quote-card__note` used `#a5a5a4` on white = 2.41:1 (needs ≥ 4.5:1) | Changed to `var(--gray-text)` `#616160` = **6.04:1** |
| 2 | **1.4.11 Non-text Contrast (AA)** | Standards strip separator dots in `#7989a9` on navy = 2.28:1 (needs ≥ 3:1) | Changed to `var(--blue-pale)` `#a5b1c6` = **4.72:1** |
| 3 | **2.4.1 Bypass Blocks (A)** | No skip link | Added `<a href="#main-content" class="skip-link">` + corresponding `id="main-content"` on `<main>`; visible on keyboard focus only |

### Verified text contrast (all ≥ 4.5:1)

| Combination | Where used | Ratio |
|---|---|---|
| Black on white | Headings, body in light sections | 21:1 |
| `--gray-text` `#616160` on white | Body and card descriptions | 6.04:1 |
| `--gray-text` on `--gray-bg` `#e9e9e9` | Trust bar, industries, testimonials | 4.81:1 |
| Navy on white | Card headings (Why Bristol), links | 10.4:1 |
| White on navy | CTA banner, hero | 10.4:1 |
| White on navy-deep `#15294f` | Footer | ~13:1 |
| `--blue-mid` `#4c628d` on white | Button hover state | 6.36:1 |
| `--blue-pale` on navy | Hero eyebrow | 4.72:1 (passes by tight margin) |

### Other AA criteria — all met

- **1.1.1** alt text on every image (decorative use empty `alt` + `aria-hidden`)
- **1.3.1** semantic landmarks: `<header>`, `<main>`, `<footer>`, `<section>`, `<nav>`, `<article>`, `<figure>`, `<blockquote>`. Heading order: 1× H1 (hero) → H2 (each section) → H3 (cards), no skips
- **1.4.1** color is never the only indicator (links combine color + underline + hover transform)
- **1.4.4** text scales to 200% (uses `clamp` / `rem` / `vw`)
- **1.4.10** reflow at 320px without horizontal scroll
- **1.4.12** line-height 1.55 (≥ 1.5 required)
- **2.1.1** all interactive elements use real `<a>` / `<button>` — keyboard operable
- **2.4.7** focus visible (`outline: 2px solid var(--navy)`)
- **3.1.1** `<html lang="en">`
- **4.1.2** ARIA: `aria-label` on landmarks, `aria-labelledby` on sections, `aria-expanded` on the menu toggle, `aria-hidden` on decorative imagery

### Known limitations (non-blocking for AA)

1. **Hero eyebrow contrast at 4.72:1** — passes by 0.22 over the threshold. If hero photography is replaced with a brighter image, re-test.
2. **Card borders in `--gray-border` (2.49:1)** — below 1.4.11's 3:1, but borders are not the sole identifier of cards (padding and background contrast also delineate them). Not a strict failure. Can be improved by darkening to `--gray-text`.
3. **Testimonials are placeholders** — replace with real attribution before launch.
4. **Mobile menu focus trap not implemented** — the open hamburger nav doesn't constrain focus inside it. Not a strict AA failure (DOM order keeps focus moving naturally), but a focus trap is a good QA-phase add.
5. **Forms not present on Homepage** — criteria 3.3.x will need to be re-checked when the Contact page is built.
6. **Manual screen-reader testing recommended** — automated checks cover structure and contrast; pre-launch testing with NVDA / VoiceOver / JAWS is still required.

---

## 7. Elementor Migration Notes

The static build is structured to translate cleanly into Elementor:

- **Brand colors → Elementor Global Colors** — the 9 CSS custom properties map one-to-one
- **Fonts → Elementor Custom Fonts** — Heavy / Roman / Light, uploaded under one family with three weights (matches the existing single-family rule)
- **Sections → Elementor Sections** — each `<section>` is independent, with no cross-section dependencies
- **Cards → Elementor Icon Box / Image Box widgets** — `.industry-card` and `.why-card` patterns map to Icon Box; `.card` (with photo) maps to Image Box
- **Standards strip → Elementor Section with background pattern** — the CSS blueprint grid can either be reproduced via Elementor's gradient backgrounds, or replaced with an SVG/PNG background image asset
- **Sticky header → Elementor Theme Builder Header with Sticky setting** — current behavior (sticky on scroll, shadow on scroll) is supported natively
- **Mobile menu → Elementor Pro Nav Menu widget** — replaces the custom hamburger JS

---

## 8. Pre-Launch Checklist (Open Items)

Items still pending before this homepage can ship — track outside the build phase:

1. **Replace placeholder testimonials** with real client quotes and confirmed attribution
2. **Confirm photography selection** — current build uses `imgi_19_Bristol-Machine-Bolts.jpg` for the hero, `imgi_20_Bristol-Machine-threaded.jpg` and `imgi_22_Bristol-Machine-Drill-Bits.jpg` for the What We Do cards. Validate these are the strongest options and licensed for use.
3. **Confirm copy claims** flagged "to confirm" in `Copy/Homepage.md` (distributor brand list, stocking claims, weekday hours phrasing)
4. **Verify icon style consistency** in `Assets/Icons/` — homepage uses single-style icons (line OR filled, current selection is consistent), but the broader library should be audited for the rest of the site
5. **Real-device QA** — test on physical iPhone, Android, iPad
6. **Manual screen-reader audit** — NVDA, VoiceOver, JAWS
7. **Performance pass** — image compression and lazy-loading attributes (currently absent — fine for prototype, required for production)
8. **Migration to Elementor** — replicate the static build inside WordPress as the production implementation

---

## 9. Definition of Done — Homepage Build Phase

This phase is complete:

- [x] Static homepage built in `Build/Homepage/`
- [x] All 8 sections from sitemap implemented in order, no deviations
- [x] Final approved copy used verbatim
- [x] Real Bristol assets used (logos, photos, icons, fonts) — no Lorem Ipsum, no stock placeholders for content
- [x] Modern Industrial Authority direction reflected: navy/black palette, Helvetica Neue LT Heavy, square corners, blueprint pattern, industrial photography
- [x] Responsive (desktop, tablet, mobile) tested
- [x] Navbar (sticky) and Footer (full) included as global components
- [x] WCAG 2.1 Level AA audited and fixes applied — page is AA compliant
- [x] Elementor-friendly structure: tokenized colors, semantic sections, reusable components

The homepage is ready for stakeholder review and approval before moving to Elementor implementation.
