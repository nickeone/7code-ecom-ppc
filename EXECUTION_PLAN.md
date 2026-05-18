# EXECUTION PLAN — Meta Ads Validation Sprint 1
**Run ID:** ppc-audit-uknl-20260518  
**Goal:** Validate Meta Ads as a lead acquisition channel for 7code's PPC audit offer  
**Budget:** €150–200 test spend  
**Timeline:** 2 weeks

---

## Sprint 1 Objectives

1. Deploy campaign-ready landing page ✓
2. Install Meta Pixel and verify event tracking
3. Launch 3 ad variants (A/B/C headline test)
4. Capture ≥10 audit form submissions
5. Measure cost-per-lead (CPL) and lead quality

---

## Campaign Structure

### Ad Account Setup
- Business Manager: 7code
- Pixel: installed on landing page (replace YOUR_PIXEL_ID)
- Conversion event: `Lead` (fires on form submit)
- Attribution: 7-day click, 1-day view

### Campaign: PPC Audit — Validation Sprint 1
- Objective: **Leads**
- Budget: €150 total / €10–15/day
- Audience: E-commerce founders + CMOs, EU markets (RO, PL, CZ, UK, DE)
  - Interests: e-commerce, Google Ads, Facebook Ads, Shopify
  - Job title: Founder, CEO, CMO, Marketing Director, Head of Growth

### Ad Sets (3 — one per headline variant)
| Ad Set | UTM | Headline in ad copy |
|---|---|---|
| Variant A | `utm_content=variant-A` | "Fire your PPC agency" |
| Variant B | `utm_content=variant-B` | "wasted spend" angle |
| Variant C | `utm_content=variant-C` | "ROAS benchmark" angle |

Each ad set links to:
```
https://7code-ecom-ppc.vercel.app/?utm_source=meta&utm_medium=paid&utm_campaign=ppc-audit-sprint1&utm_content=variant-X
```

### Creative Specs
- Format: Single image (1080×1080) or short video (15s)
- Primary text: 2–3 sentences, problem-aware hook
- CTA button: "Learn More" → landing page

---

## Success Metrics

| Metric | Target |
|---|---|
| Link CTR | ≥ 1.5% |
| Landing page CVR | ≥ 8% |
| Cost per Lead (CPL) | ≤ €20 |
| Lead quality score | ≥ 60% qualified (€5k+/mo spend) |

---

## Week 1 Tasks

- [ ] Replace `YOUR_PIXEL_ID` in index.html
- [ ] Replace `YOUR_FORM_ID` in index.html
- [ ] Verify Pixel fires (PageView + Lead) via Meta Pixel Helper
- [ ] Upload ad creatives to Meta Ads Manager
- [ ] Create 3 ad sets with variant UTM links
- [ ] Launch campaign

## Week 2 Tasks

- [ ] Review CPL and CTR by variant (pause losers at €30 spend)
- [ ] Scale winning variant to €200 total
- [ ] Review form leads for quality
- [ ] Decide: continue Meta, add Google, or pivot offer

---

## Contacts

- **Pixel ID**: [set in Meta Events Manager]
- **Form endpoint**: [set in Formspree]
- **Vercel project**: 7code-ecom-ppc
