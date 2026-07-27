# Purpose Built by Coastal — Design System

**Prepared by:** Agent 4 (Design System & Art Direction)
**Date:** July 27, 2026
**Inputs:** `strategy.md`, live site CSS extraction (macaly.app), `tokens.css`

---

## 1. Design Principles

1. **Sharp and architectural** — flat edges (radius: 0), structured layouts, confident geometry. Reflects new construction — nothing soft or rounded.
2. **Coastal, not beachy** — navy and sand evoke the Gulf Coast without tourist-shop clichés. Premium, not playful.
3. **Let the concept breathe** — generous whitespace, short sections, scannable rhythm. Investors skim before they commit.
4. **Gold as the signal** — gold is used sparingly as the accent — buttons, key lines, highlights. Never decorative. Always functional.

---

## 2. Color Palette

| Token | Hex | Role |
|---|---|---|
| `--navy` | `#1e3a4f` | Primary text, dark backgrounds, headers |
| `--slate` | `#5b7b8c` | Muted text, secondary UI elements |
| `--gold` | `#c4a77d` | CTAs, accents, key highlights, hover states |
| `--gold-hover` | `#b3966e` | Gold button hover |
| `--sand` | `#f5f0e8` | Alternate section backgrounds, warmth |
| `--white` | `#ffffff` | Primary background, light text on dark |
| `--border` | `#e5e0d8` | Subtle borders/dividers |
| `--border-light` | `#f0ebe4` | Very light borders on sand backgrounds |

### Contrast Pairs (Accessibility)
| Foreground | Background | Ratio | Use |
|---|---|---|---|
| Navy `#1e3a4f` | White `#ffffff` | 11.2:1 ✅ AAA | Body text |
| Navy `#1e3a4f` | Sand `#f5f0e8` | 10.5:1 ✅ AAA | Alt section text |
| White `#ffffff` | Navy `#1e3a4f` | 11.2:1 ✅ AAA | Dark section text |
| White `#ffffff` | Gold `#c4a77d` | 2.3:1 ❌ | **Never use — gold buttons get dark text or are decorative only** |
| Slate `#5b7b8c` | White `#ffffff` | 4.8:1 ✅ AA | Muted text on white |
| Gold `#c4a77d` | Navy `#1e3a4f` | 4.5:1 ✅ AA | Gold accents on dark |

**Rule:** White-on-gold text is never allowed. Gold buttons use white text only at large sizes (≥18px bold) — otherwise use navy text on gold.

---

## 3. Typography

| Level | Size | Weight | Line Height | Use |
|---|---|---|---|---|
| Display | 4.5rem (72px) | 700 | 1.15 | Hero headlines (home only) |
| H1 | 3rem (48px) | 700 | 1.15 | Page titles |
| H2 | 2.25rem (36px) | 700 | 1.15 | Section headers |
| H3 | 1.875rem (30px) | 600 | 1.35 | Sub-section headers |
| H4 | 1.5rem (24px) | 600 | 1.35 | Card titles, feature headers |
| H5 | 1.25rem (20px) | 500 | 1.6 | Minor headers |
| Body LG | 1.125rem (18px) | 400 | 1.75 | Lead paragraphs, feature descriptions |
| Body | 1rem (16px) | 400 | 1.75 | Standard body copy |
| Body SM | 0.875rem (14px) | 400 | 1.6 | Secondary copy, captions |
| Caption | 0.75rem (12px) | 400 | 1.6 | Labels, meta, footnotes |

### Font Family
- Primary: **Inter** (300, 400, 500, 600, 700)
- Monospace: SF Mono, Consolas (for any code/data display)
- Loaded from Google Fonts: `Inter:wght@300;400;500;600;700`

### Typography Rules
- Headlines use `letter-spacing: -0.02em` (tight) for a premium feel
- Body copy uses default spacing
- Never use all-caps for headlines — it fights the premium tone
- Maximum line length: 72 characters for body copy
- Gold accent color reserved for CTAs and key navigational elements — never used on body text

---

## 4. Spacing System

Based on a 4px grid. Consistent vertical rhythm.

| Token | Value | Use |
|---|---|---|
| `space-1` | 4px | Tight gaps, icon spacing |
| `space-2` | 8px | Small gaps |
| `space-3` | 12px | Element padding |
| `space-4` | 16px | Standard gap, card padding |
| `space-5` | 20px | Comfortable gap |
| `space-6` | 24px | Section element gap, container padding |
| `space-8` | 32px | Large gaps |
| `space-10` | 40px | Section sub-spacing |
| `space-12` | 48px | Major section internal spacing |
| `space-16` | 64px | Between major content blocks |
| `space-20` | 80px | Standard section padding (`--section-y`) |
| `space-24` | 96px | Large section padding (`--section-y-lg`) |

---

## 5. Component Inventory

### Navigation
- **Type:** Sticky top nav, white background with subtle bottom border
- **Structure:** Logo (left) + nav links (center/right) + CTA button (right)
- **Mobile:** Hamburger menu, full-screen overlay
- **States:** Active link underlined with gold accent, hover darkens text
- **Height:** 5rem (80px)

### Hero Section
- **Type:** Full-width, dark overlay on background image
- **Structure:** Headline + subheadline + dual CTAs (primary gold + secondary outline)
- **Background:** High-quality property/coastal imagery with navy gradient overlay (`from-navy/90 to-navy/60`)
- **Height:** Minimum 80vh, content vertically centered
- **Animation:** Headline fades in up, subheadline follows with 200ms delay

### Section Block (Standard)
- **Type:** Alternating backgrounds (white → sand → white)
- **Structure:** Section label (gold, small caps feel) → H2 headline → body copy → optional CTA
- **Max width:** 56rem (896px) for centered copy; full container width for multi-column

### Feature Cards (3-up)
- **Type:** Icon + headline + description in a 3-column grid
- **Structure:** Gold icon (top) → H4 title → body-sm description
- **Background:** Optional sand card background, or transparent with gold left-border accent
- **Responsive:** Stacks to 1-column on mobile, 3-column on desktop

### Stat / Proof Cards
- **Type:** Large number + label, used to display market data
- **Structure:** Display-sized navy number → caption label in slate
- **Grid:** 2-4 per row depending on count
- **Use cases:** FEMA rating, development pipeline count, restaurant count, park investment

### Testimonial Block
- **Type:** Pull quote with attribution
- **Structure:** Gold leading mark → italic quote text → name + role in slate
- **Background:** Sand section background
- **Max width:** 42rem (narrow for readability)

### FAQ Accordion
- **Type:** Expandable Q&A items
- **Structure:** Question in H5 → expand/collapse icon (gold) → answer body
- **States:** Closed (icon: +), open (icon: −), hover darkens question text
- **Background:** White or sand

### CTA Section (Bottom-of-Page)
- **Type:** Navy background, centered
- **Structure:** H2 in white → body-lg in white/slate → gold CTA button
- **Spacing:** Generous — section-lg padding

### Contact Form
- **Type:** Clean, minimal form
- **Fields:** Name, Email, Phone (optional), Interest dropdown, Timeline dropdown, Message
- **Style:** Sharp input borders (navy/20), gold focus ring, gold submit button
- **Validation:** Inline error messages in slate, success state with confirmation message

### Footer
- **Type:** Navy background, multi-column
- **Structure:** Logo + description (left), nav columns (center), contact (right)
- **Bottom bar:** Copyright + legal links
- **Columns:** 4 — Explore, Company, Contact, Legal

---

## 6. Imagery Direction

### Photography Style
- **Architectural:** Clean lines, strong geometry, elevated perspectives
- **Coastal context:** Water, sky, beach as backdrop — never the subject
- **Lighting:** Golden hour or crisp daylight. No overcast, no harsh midday shadows.
- **Human presence:** Subtle — people in context (dining, walking, enjoying), never staged lifestyle shots
- **No clichés:** No stock sunset photos, no "happy family on beach," no generic "For Sale" sign imagery

### Graphics & Icons
- **Style:** Minimal, line-based, gold or navy
- **Icons:** Lucide icon set (consistent stroke width, clean geometry)
- **Data visualization:** Simple bar or timeline graphics, clean sans-serif labels, navy + gold palette
- **Background treatments:** Subtle geometric patterns, gold line accents, section dividers

### Image Formats
- **Photos:** WebP (primary), JPEG fallback
- **Icons/logos:** SVG
- **OG images:** 1200×630 PNG, unique per page

---

## 7. Responsive Behavior

| Breakpoint | Width | Layout Changes |
|---|---|---|
| Base (mobile) | < 640px | Single column, stacked nav, full-width CTAs, reduced type scale |
| SM | ≥ 640px | 2-column grids available, inline CTAs |
| MD | ≥ 768px | 3-column grids, full nav visible |
| LG | ≥ 1024px | 4-column grids, max type scale, max section padding |
| XL | ≥ 1280px | Container max-width caps at 1280px, extra whitespace on wide screens |

### Mobile Adjustments
- Hero height: 80vh → 60vh (smaller screens)
- H1: 3rem → 2.25rem
- Section padding: 80px → 48px
- Feature cards: 3-col → 1-col stack
- Nav: sticky hamburger menu with full-screen overlay
- Forms: full-width inputs

---

## 8. One-Off Exception Log

*No exceptions logged. All pages must build from this system. If a page requires an exception, log it here with justification and Hermes approval.*

| Date | Page | Exception | Justification | Approved |
|---|---|---|---|---|
| — | — | — | — | — |

---

## 9. References

- **Tokens file:** `/tokens.css` — all CSS custom properties, utility classes, animations
- **Font:** Inter from Google Fonts — `https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap`
- **Icons:** Lucide — `https://lucide.dev`
- **Inspiration site:** macaly.app (current production site for Purpose Built by Coastal)
