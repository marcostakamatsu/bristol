# Bristol Homepage — Session Handoff

> Short, living document. Update at the end of every session. **Do not** paste diffs here — use `git log -p` for history.

## Current status
- **Phase completed:** Industries hover refined — icon background removed, softer hover (no full navy fill)
- **Suggested next phase:** Visual QA in browser → real form integration → Products page
- **Last updated:** 2026-04-30

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
- **Industry card:** icon with no background (44px), gentle hover — `translateY(-4px)` + navy border + light shadow, icon `scale(1.06)`, title → navy, arrow translate (no flip to navy fill)
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
2. For bulk mechanical changes → lighter model (Sonnet/Haiku)
3. For design/a11y/architecture decisions → Opus
4. Commit at the end of every phase to preserve context in `git log`
5. **Update this file** with new status + open items before closing the session
