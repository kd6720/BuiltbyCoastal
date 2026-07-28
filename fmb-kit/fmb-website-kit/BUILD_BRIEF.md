# Build Brief — Fort Myers Beach Insider
### Instructions for Claude Code (claude-fable-5) · Prepared by Carter Dewey · July 2026

You are building a public marketing website that promotes Fort Myers Beach and the surrounding Fort Myers area as an incredible real estate investment opportunity — specifically **beach property as a dual-use asset: use it when you want, run it as a short-term rental when you're not there.**

Everything you need is in this kit. Do not invent statistics — every number you publish must come from `content.json` or `docs/FMB_Research_Appendix_July2026.md`.

---

## 1. Goal & audience

**Goal:** Position Fort Myers Beach as the smartest beach-property buy on the Gulf Coast in 2026, and capture leads (email signups / contact requests) from prospective buyers and investors.

**Audience:** Beach-property buyers and STR investors in Southwest Florida and feeder markets (Midwest, Northeast, East Coast Florida); second-home and 1031 buyers; agents and referral partners.

**Core message (use this framing everywhere):**
> A beach house here isn't either/or. Block the weeks you want. Rent the rest. Weekly rentals are legal by right in the Gulf-side zone, and large new homes gross $80K–$166K a year — on an island where prices are down 9–18%, hotel supply is 41% below pre-Ian levels, and $1.7B of airport capacity is being built 25 minutes away.

## 2. Tone rules (non-negotiable)

- Write like an experienced operator, not a marketing intern. Confident, specific, no hype.
- No buzzwords, no fake urgency, no exaggerated claims. Never claim amenities or venues that aren't open yet.
- Every stat visible on the site must trace to `content.json`. Cite "Data as of July 2026" near data blocks.
- Include this disclaimer in the footer and on the investment pages: *"Informational only — not financial, legal, or tax advice. Data as of July 2026 from public sources; verify independently before transacting."*
- **Financial-claims guardrails (added July 2026 — highest priority):** Any pro-forma figure published on the site must appear with its source label. Sponsor-published returns (12.17% cash-on-cash, 9.38% cap) may only be shown side-by-side with the stress-tested column (6.61% / 7.71%) from `pro_forma_large_format`. Never publish a cash-on-cash or cap rate as a standalone promise. Never present $347,910 of gross revenue as typical — it is top-1% performance; the market 6BR+ average is $123,197 and the 5BR average is $166,328. Do not repeat the "$800–$950 ADR at 78–85% occupancy" pairing: it does not reconcile to $347,910 (that revenue needs ~$1,121/night at 85%). No projected-return claim may appear in a headline, hero, or CTA — only inside the underwriting section with the disclaimer visible on the same screen.
- Accuracy guardrails: RSW's Concourse E (14 gates) completes end of 2027 — the Phase 1 checkpoint finishes 2029; don't say the whole expansion is "done." The Seagate/Red Coconut condo project is approved but its site was listed for sale May 2026 — don't cite it as certain. Present the -10.2% 2026 metro forecast honestly as the buyer's-market entry argument.

## 3. Site structure (single-page-first; sections can become routes later)

1. **Hero** — full-bleed beach image (`assets/prospectus-pages/page-11.png` bottom image aesthetic, or page-01 hero). Headline: "Own the beach. Use it when you want. Rent it when you don't." Sub: one-sentence thesis + CTA button ("Get the 2026 Prospectus").
2. **The Opportunity** — the four thesis pillars from `content.json > core_thesis.pillars` as stat cards.
3. **Dual-Use Math** — the lifestyle + income pitch: STR ADR $370–$425 market-wide, average listing grosses $33K–$46K/yr, weekly rentals legal Gulf-side. Simple visual: "Your weeks" vs "Rental weeks" calendar graphic. **Then step the reader up the size curve** using `market_snapshot.rentals.by_bedroom_annual_revenue` — this is the single most persuasive data block in the kit: 3BR $63,899 → 4BR $82,316 → 5BR $166,328, with only 47 listings island-wide at 5BR+. State the owner-use cost honestly: a peak-season owner week costs roughly $950–$1,500/night in foregone revenue.

3a. **The Numbers, Underwritten** (new section — use `pro_forma_large_format`) — a two-column pro forma for a 6BR/3,100 sq ft new build at $2,706,375: "Sponsor case" vs "Stress-tested." Publish **both columns**, never the sponsor column alone. Headline the stress-tested figures: **7.71% cap rate, 6.61% cash-on-cash, 1.35x DSCR, 7.71% unlevered cash yield.** Include the breakeven callouts ($258K gross to service debt, $323K for a 1.25x DSCR) and the `honest_read` paragraph verbatim or close to it. This section is the credibility engine of the whole site — an investor who sees a re-underwrite next to a sponsor number trusts everything else on the page.
4. **The Island Is Back** — rebuild proof: $23M beach complete, Margaritaville, new $17.7M pier (2027–28), Times Square rebuild, 40+ restaurants, parks program, events calendar. Use `island_rebuild` from content.json.
5. **Market Snapshot** — housing table (median $546K–$575K, SF $1.23M, condo $579K, lots $745K median, 95% of sales below list, 11–13 months supply). Frame as the 2026 entry window.
6. **The Regional Engine** — three cards: RSW ($1.7B expansion, record 11.15M passengers), Lee County growth (+15.1%, Babcock Ranch, $820M hospital), Downtown Fort Myers ($6B redevelopment, River District). Use `regional_engine`.
7. **Ways In** — the investment ladder table from `investment_ladder` (older condo → condo-hotel → legacy SF → lot + build → new elevated 5-6BR sweet spot). Be honest about condo SIRS/assessment risk. Add the performance-tier table from `market_snapshot.rentals.performance_tiers` so readers see the spread between median ($4,122/mo) and top-decile ($12,436+/mo) — the site's argument is that asset quality and revenue management move you up that ladder, not that the market carries you.
8. **The Prospectus** — embed/preview the 13 page images (`assets/prospectus-pages/page-01.png` … `page-13.png`) as a flip-through gallery; button downloads the full PDF from Supabase Storage. Pages 12–13 are the underwriting pages — they can also be rendered inline as the artwork for section 3a.
9. **Risks, stated plainly** — short section: insurance volatility, pier timing, storm exposure, project uncertainty. This builds credibility; keep it.
10. **Lead capture + footer** — email capture ("Get the prospectus + market updates"), contact link, disclaimer, "Data sources" list from `content.json > sources`.

## 4. Tech stack & deployment

- **Repo:** `https://github.com/kd6720/Fort-Myers-Beach-Insider` (owner: kd6720). Commit the site here.
- **Stack:** Static site — plain HTML/CSS/JS or Astro/Vite (your choice; keep the build simple and fast). Fully responsive, mobile-first. Lighthouse 90+ on performance and SEO.
- **Hosting:** GitHub Pages. Add a GitHub Actions workflow (`.github/workflows/deploy.yml`) that builds and publishes to Pages on push to `main`. Enable Pages via the workflow (`actions/deploy-pages`).
- **Design language:** match the prospectus — white/soft sand backgrounds, deep navy headlines, ocean teal accents, generous whitespace, thin wave-line motifs. Fonts: a clean geometric sans (e.g., Inter/Archivo). No dark corporate templates.
- **Images:** use the 11 exported prospectus pages in `assets/prospectus-pages/` (794×1123 PNG) for the gallery; crop page hero imagery for section backgrounds where useful. Optimize (WebP conversions welcome) and lazy-load.

### Supabase (file storage + optional leads)

- Create a Supabase project; create a **public storage bucket** named `fmb-insider`.
- Upload: `docs/Fort Myers Beach - 2026 Investment Prospectus.pdf`, `docs/FMB_Research_Appendix_July2026.md`, and the page PNGs. Use the public URLs for the site's "Download the Prospectus" button and gallery (or serve PNGs locally from the repo and keep only the PDF on Supabase — your call, but the PDF download must come from Supabase Storage per the owner's request).
- Store the Supabase URL + anon key in the site via environment/config constants; **never commit the service-role key**.
- Optional but preferred: a `leads` table (email text, created_at timestamptz, source text) with Row Level Security enabled and an insert-only policy for anon; wire the email-capture form to it via `@supabase/supabase-js`. If you skip this, use a mailto/Formspree fallback — but leave the Supabase wiring stubbed and documented.

## 5. SEO

- Title: "Fort Myers Beach Real Estate Investment — Own the Beach, Rent It When You're Away | Fort Myers Beach Insider"
- Meta description (~155 chars): "Fort Myers Beach 2026: prices down, hotel supply 41% below pre-Ian, weekly rentals legal Gulf-side. The dual-use beach investment, explained with data."
- Target queries: "Fort Myers Beach real estate investment", "Fort Myers Beach vacation rental investment", "beach house investment Florida", "Fort Myers Beach new construction homes".
- Add OpenGraph/Twitter cards (use page-01.png as OG image), JSON-LD (WebSite + Article), sitemap.xml, robots.txt, canonical URL.

## 6. Files in this kit

| Path | What it is |
|---|---|
| `BUILD_BRIEF.md` | This brief — your instructions |
| `content.json` | ALL site copy data: thesis, market stats, rebuild status, regional engine, investment ladder, risks, sources |
| `docs/Fort Myers Beach - 2026 Investment Prospectus.pdf` | The 13-page designed prospectus (the downloadable asset) |
| `docs/FMB_Research_Appendix_July2026.md` | Full research detail + source list (use for deeper copy; publish as a "Data Room" page if desired) |
| `assets/prospectus-pages/page-01.png … page-13.png` | Page images of the prospectus (794×1123) for gallery/section art |

Page map: 01 cover · 02 exec summary · 03 infrastructure · 04 development pipeline · 05 parks & dining (photo collage — good for lifestyle sections) · 06 housing market table · 07 hotels & rentals table · 08 RSW · 09 regional growth · 10 downtown Fort Myers · 11 bottom line (beach photo — good hero candidate) · **12 underwriting the large-format play (performance by bedroom count, performance tiers, top-performer callout)** · **13 example pro forma — sponsor case vs. stress-tested, breakevens, the honest read**.

## 7. Definition of done

- Site builds clean, deploys to GitHub Pages from `main` via Actions, renders correctly on mobile and desktop.
- Prospectus PDF downloads from Supabase Storage; gallery shows all 13 pages.
- Every published number matches `content.json`; disclaimer and risks section present; sources listed.
- Lead capture works (Supabase table or documented fallback).
- README.md documents: local dev, deploy, Supabase setup (bucket + keys + leads table SQL), and how to update `content.json` for future data refreshes.
