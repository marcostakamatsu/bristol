# Bristol Homepage — Session Handoff

> Short, living document. Update at the end of every session. **Do not** paste diffs here — use `git log -p` for history.

## Current status
- **Phase completed:** Products page (Hub) built — `products.html` at repo root following Plan/04 Page 2 sitemap. New CSS: `.inner-banner`, `.product-preview`, `.product-card`, `.grid--4`, `.card__eyebrow`, `.img-placeholder`. Copy lives in `Copy/Products.md`. Image prompts in `Build/Products/IMAGE-PROMPTS.md` — 10 placeholders awaiting generation under `Assets/Photos/products/`.
- **Suggested next phase:** Generate Products images → swap placeholders for `<img>` → Fabricated Products detail (Plan Page 3) or Distributed Products detail (Plan Page 5)
- **Last updated:** 2026-05-01

## Stack & structure
- Static HTML/CSS, no build step
- Main files: `index.html`, `style.css` (at repo root, served by GitHub Pages)
- Assets in `Assets/Photos/`, `Assets/Icons/`, `Assets/Logos/` (relative paths `Assets/...`)
- This handoff lives at `Build/Homepage/HANDOFF.md` (project doc, not deployed)

## Design tokens (in `:root`)
- **Colors:** `--navy`, `--navy-deep`, `--blue-pale`, `--white`, `--black`, `--gray-bg`, `--gray-border`, `--gray-text`
- **Motion:** `--dur-fast`, `--dur-base`, `--dur-slow`, `--ease`, `--ease-out`
- **Layout:** `--section-pad-y` (80/72/64 responsive), `--container-pad`, `--radius`, `--header-h`, `--header-h-mobile`
- **Typography:** `--font-stack` (Inter / sans fallback)

## Established conventions
- **Card hover:** `translateY(-8px)` + shadow `28px/56px` + border → navy + image `scale(1.06)` + gradient overlay
- **Industries layout:** flex split (`.industries__split`) — `.industries__media` (photo, `order: 1`) left, `.industries__list` (`order: 2`) right with stacked `.industry-row` cards
- **Industry row card (dark):** navy bg, 56px icon column + body, white title, white-icon via `filter: brightness(0) invert(1)`, hover → `translateX(4px)` + `--navy-deep` bg + white accent bar `scaleY` from left
- **Why card:** `translateY(-6px)`, 3px navy accent bar on the left (scaleY), icon rotates/scales
- **Testimonial feature:** 1.15fr/1fr split, featured quote + photo on the right, hover `translateY(-4px)` + image `scale(1.04)` + quote mark scale
- **Testimonial slider:** flex track with `translateX`, dots + prev/next buttons (44px circle, navy fill on hover), arrow keys when focused, viewport `overflow:hidden`
- **Reveals:** `[data-reveal]` + `[data-reveal-delay="1..6"]` (stagger ~80ms), `is-revealed` class applied via IntersectionObserver
- **Reduced-motion:** scoped block at the end of `style.css` (do not use a global `* { transition: none }`)
- **Focus visible:** 2px navy outline, white on dark sections (hero, standards, cta, footer)
- **Buttons:** primary lift `-2px` + shadow on hover; ghost with fill transition

## Accessibility (WCAG)
- Skip link present (2.4.1)
- Focus states on every interactive element (2.4.7)
- `prefers-reduced-motion` respected (2.3.3)
- Contrast verified for copy on dark sections (notes in the CSS)
- Empty alt text on decorative icons (`aria-hidden`)

## JS on the page
- Sticky header shadow on scroll
- Mobile nav toggle (hamburger)
- Auto copyright year
- Scroll reveal via IntersectionObserver with fallback (reduced-motion + no IO)
- Testimonial slider (prev/next, dots, arrow keys)

## Open items
- [ ] Testimonials marked as "Sample — to confirm" (real copy pending from client)
- [ ] "Request a Quote" CTA points to `#contact` — no real form yet
- [ ] Internal pages (Products, Industries detail, About) do not exist
- [ ] Hero image may need an optimized/webp version
- [ ] LinkedIn link points to the generic homepage

## DO NOT
- ❌ Reintroduce a global `* { transition: none !important }` — it breaks focus-visible and the scroll cue. The current reduced-motion block is intentionally scoped.
- ❌ Add `Co-Authored-By: Claude` to commits (user preference, recorded in memory)
- ❌ Paste long diffs as context between sessions — use this handoff + `git log` + current repo state
- ❌ Reopen the entire `style.css` file just to "check the state" — use Grep/Read with offset

## Workflow for upcoming sessions
1. **Read this HANDOFF.md first** (the only mandatory step)
0. **Desktop-only mode:** do not add new `@media` rules or extend existing responsive blocks. Edit/build for desktop (~1024px+) only. Wait for the user to ask "passa nos breakpoints" before doing a responsive sweep.
2. For bulk mechanical changes → lighter model (Sonnet/Haiku)
3. For design/a11y/architecture decisions → Opus
4. Commit at the end of every phase to preserve context in `git log`
5. **Update this file** with new status + open items before closing the session
