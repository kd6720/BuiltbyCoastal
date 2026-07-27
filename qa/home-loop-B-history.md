# QA Report — Loop B: SEO Audit

**Reviewer:** Agent 7 (QA — SEO Auditor hat)
**Date:** July 27, 2026
**Method:** Code audit of HTML source, meta tags, schema, internal linking, heading structure.
**Exit criterion:** Score ≥90 AND zero critical findings AND schema validates.

---

## Home (`/`)

| Dimension | Score (/20) | Notes |
|---|---|---|
| On-page SEO (20) | **19** | Title: 55 chars ✅. Meta description: 148 chars ✅. H1: "Investment Homes Built for Performance" — contains implicit keyword. Primary keyword "vacation rental investment homes Fort Myers Beach" appears in first paragraph body text ✅. H2/H3 structure logical. Alt text on hero image present and descriptive ✅. Minor: H1 could front-load "Fort Myers Beach" more explicitly — current H1 is strong marketing copy but keyword is in subheadline, not H1. |
| Technical SEO (20) | **19** | Canonical self-referencing ✅. Schema: Organization with email and address ✅. Sitemap lists page ✅. Robots.txt allows all ✅. Clean URL `/` ✅. No broken internal links detected ✅. Minor: Missing breadcrumb schema. |
| Content quality & intent (20) | **19** | Intent match: commercial — investor researching STR properties ✅. Depth: 390 words, 4 sections, covers concept → framework → market → CTA ✅. Internal links: 6 out (all nav + contextual) ✅. E-E-A-T signals: Local expertise (Fort Myers Beach specific), clear value proposition ✅. |
| Performance/CWV (20) | **15** | **Can't verify live — estimated based on code.** Total HTML: ~11.5KB ✅. CSS: ~16KB ✅. WebP images: 109-217KB each ✅. No render-blocking JS beyond minimal inline scripts ✅. Estimated LCP < 2s, CLS ≈ 0 (no dynamic content), total weight well under 1.5MB ✅. Assigned conservative score pending live Lighthouse run. |
| Uniqueness (20) | **20** | Title unique across site ✅. Meta description unique ✅. H1 unique ✅. No keyword cannibalization with other pages ✅. |
| **TOTAL** | **92** | ✅ PASS |

**Critical findings:** None. **Major:** None.

---

## About (`/about`)

| Dimension | Score (/20) | Notes |
|---|---|---|
| On-page SEO (20) | **18** | Title: 58 chars ✅. Meta: 152 chars ✅. H1: "Built on experience. Driven by performance." — branded but doesn't contain primary keyword "Purpose Built by Coastal development team" explicitly. Keyword appears in body text ✅. Alt text: not applicable (no images on this page) ⚠️ — no images means no alt text issue, but also no visual SEO signals. |
| Technical SEO (20) | **18** | Canonical ✅. Schema: Organization ✅. Sitemap ✅. No images on page — missed opportunity for image SEO. |
| Content quality (20) | **17** | Intent match: commercial — investor evaluating credibility ✅. Depth: ~250 words — light but adequate for an About page ✅. Internal links: 4 out ✅. Minor: Could be deeper — no team bios, no timeline, no project count. |
| Performance (20) | **17** | Very light page (~6.5KB HTML) — will load instantly ✅. No images to optimize. |
| Uniqueness (20) | **20** | Title unique ✅. Meta unique ✅. H1 unique ✅. |
| **TOTAL** | **90** | ✅ PASS (borderline) |

**Critical findings:** None.

---

## What Is Purpose Built (`/what-is-purpose-built`)

| Dimension | Score (/20) | Notes |
|---|---|---|
| On-page SEO (20) | **19** | Title: 60 chars ✅. Meta: 155 chars ✅. H1: "Not a conversion. Not a rehab. Purpose built." — branded but primary keyword "what is a purpose built vacation rental" is more embedded in the narrative. Keyword "purpose built" in H1 ✅. "ground-up" and "from the ground up" in body text ✅. Contrast with conversions/rehabs in first section ✅. |
| Technical SEO (20) | **18** | Canonical ✅. Schema: Organization only — this page is informational and could benefit from Article or FAQ schema ⚠️. |
| Content quality (20) | **19** | Intent match: informational — someone asking "what is this concept" ✅. Depth: ~520 words, strong contrast structure (problem → solution) ✅. Internal links: 3 contextual ✅. |
| Performance (20) | **17** | ~6.7KB HTML — very fast ✅. No images — missed visual opportunity. |
| Uniqueness (20) | **20** | Title unique ✅. Meta unique ✅. H1 unique ✅. |
| **TOTAL** | **93** | ✅ PASS |

---

## Three Pillars (`/three-pillars`)

| Dimension | Score (/20) | Notes |
|---|---|---|
| On-page SEO (20) | **19** | Title: 58 chars ✅. Meta: 158 chars ✅. H1: "Three pillars. One outcome." — doesn't contain primary keyword "vacation rental investment ROI design." Keyword appears in body. Three H2 sections (one per pillar) clearly delineated ✅. Image alt text present on both images ✅. |
| Technical SEO (20) | **18** | Canonical ✅. Schema: Organization only — could benefit from Article or ItemList schema for the three pillars. Images have lazy loading ✅. |
| Content quality (20) | **20** | **Best content page.** ~700 words, deep pillar-by-pillar treatment with concrete examples, interconnection callout, clear CTA to next page ✅. Internal links: 3 contextual ✅. |
| Performance (20) | **16** | ~9.2KB HTML + 2 WebP images (109KB + 187KB) — total page weight ~300KB ✅. Images lazy-loaded ✅. |
| Uniqueness (20) | **20** | Title unique ✅. Meta unique ✅. H1 unique ✅. |
| **TOTAL** | **93** | ✅ PASS |

---

## Why Fort Myers Beach (`/why-fort-myers-beach`)

| Dimension | Score (/20) | Notes |
|---|---|---|
| On-page SEO (20) | **20** | Title: 60 chars ✅. Meta: 160 chars ✅ — includes all key data points. H1: "A once-in-a-generation rebuild." — branded but "Fort Myers Beach" implicit in hero subheadline. Primary keyword in body ✅. All prospectus data points present (FEMA, Margaritaville, Fishing Pier, restaurants, festivals, Estero, San Carlos) ✅. Image alt text on hero ✅. H2 structure clean: Infrastructure → Development Pipeline → Parks & Dining → Why It Matters ✅. |
| Technical SEO (20) | **19** | Canonical ✅. **FAQ schema present and valid** ✅ — 3 Q&A pairs (FEMA rating, developments, restaurants). Sitemap ✅. Minor: schema could add more Q&A pairs. |
| Content quality (20) | **20** | Intent match: commercial/informational — investor doing market diligence ✅. Depth: ~620 words with concrete data points (not just claims) ✅. Feature cards for infrastructure and pipeline sections make data scannable ✅. Internal links: 4 contextual ✅. |
| Performance (20) | **16** | ~10.5KB HTML + 1 WebP hero (216KB) ≈ 230KB total ✅. Image lazy-loaded ✅. |
| Uniqueness (20) | **20** | Title unique ✅. Meta unique ✅. H1 unique ✅. **No competitor cannibalization** — this page owns "Fort Myers Beach investment property opportunity" ✅. |
| **TOTAL** | **95** | ✅ PASS |

**Best SEO score.** FAQ schema, data-rich content, strong internal linking.

---

## Investor Overview (`/investor-overview`)

| Dimension | Score (/20) | Notes |
|---|---|---|
| On-page SEO (20) | **19** | Title: 58 chars ✅. Meta: 153 chars ✅. H1: "Turnkey vacation rental investment in Fort Myers Beach." — contains primary keyword ✅. "vacation rental investment" and "Fort Myers Beach" in body ✅. FAQ schema present with 3 Q&A pairs ✅. |
| Technical SEO (20) | **19** | Canonical ✅. FAQ schema valid ✅. Process steps use semantic structure. Minor: no image on page — missed OG/share opportunity. |
| Content quality (20) | **19** | Intent match: commercial/transactional ✅. Depth: ~580 words covering investment overview, process, property types, FAQ ✅. 5-step process is clear and scannable ✅. Internal links: 4 contextual ✅. |
| Performance (20) | **17** | ~10.6KB HTML, no images — very fast ✅. |
| Uniqueness (20) | **20** | Title unique ✅. Meta unique ✅. H1 unique ✅. |
| **TOTAL** | **94** | ✅ PASS |

---

## Contact (`/contact`)

| Dimension | Score (/20) | Notes |
|---|---|---|
| On-page SEO (20) | **18** | Title: 55 chars ✅. Meta: 142 chars ✅. H1: "Start the conversation." — branded but doesn't contain primary keyword "contact Purpose Built by Coastal." Keyword appears in body ("Prefer to reach out directly? Email us at...") ✅. Form labels are descriptive ✅. |
| Technical SEO (20) | **18** | Canonical ✅. ContactPage schema present ✅. Form uses Formspree placeholder — needs real endpoint ⚠️. Form has proper labels, required attributes, and field types ✅. |
| Content quality (20) | **18** | Intent match: transactional ✅. Form includes qualifying fields (interest, timeline) without creating barriers ✅. Alternative contact provided ✅. Response-time expectation set ("within 24 hours") ✅. |
| Performance (20) | **17** | ~6.5KB HTML, no heavy assets ✅. |
| Uniqueness (20) | **20** | Title unique ✅. Meta unique ✅. H1 unique ✅. |
| **TOTAL** | **91** | ✅ PASS |

**Finding — Major:** Form endpoint (`formspree.io/f/your-form-id`) is a placeholder and needs to be replaced with a real form handler before launch.

---

## Loop B — Summary

| Page | Score | Status |
|---|---|---|
| Home | 92 | ✅ |
| About | 90 | ✅ |
| What Is Purpose Built | 93 | ✅ |
| Three Pillars | 93 | ✅ |
| Why Fort Myers Beach | 95 | ✅ |
| Investor Overview | 94 | ✅ |
| Contact | 91 | ✅ |

**All pages pass Loop B (≥90, zero critical findings, schema validates on pages that have it).**

### Critical Findings: **NONE**
### Major Findings: **1**
1. **Contact form endpoint is a placeholder** (`formspree.io/f/your-form-id`) — must be replaced with a real form handler before launch.

### Minor Findings (3 items):
1. Home H1 could front-load "Fort Myers Beach" more explicitly
2. About page has no images — missed visual/SEO opportunity
3. What Is Purpose Built could add FAQ or Article schema

### Schema Validation Status
| Page | Schema Type | Valid |
|---|---|---|
| Home | Organization | ✅ |
| About | Organization | ✅ |
| Why Fort Myers Beach | FAQPage (3 Q&A) | ✅ |
| Investor Overview | FAQPage (3 Q&A) | ✅ |
| Contact | ContactPage | ✅ |
