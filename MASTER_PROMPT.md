# MASTER PROMPT — 7code PPC Campaign AI Prompts

A library of Claude prompts for ongoing campaign work.

---

## 1. Ad Copy Generator

```
You are writing Meta ad copy for 7code, a senior PPC agency for e-commerce brands.

Offer: Free 30-minute PPC audit (Google + Meta accounts reviewed)
Target: E-commerce founders and CMOs spending €2k–€30k/month on ads
Tone: Confident, direct, no fluff. Speak like a trusted advisor, not a salesperson.

Write 3 versions of ad copy for a Meta single-image ad:
- Primary text: 2–3 sentences, hook + problem + CTA
- Headline (40 chars max): direct benefit or challenge
- Description (30 chars max): urgency or proof

Use these angles:
- Version A: "Fire your agency" — challenge them to question their current agency
- Version B: "Wasted spend" — focus on the money being lost right now
- Version C: "ROAS benchmark" — data-led, compare to what's possible

Each version should end with a clear call to action directing to the free audit.
```

---

## 2. Lead Follow-up Email

```
Write a follow-up email to send within 1 business day of a PPC audit form submission.

Context:
- They submitted at: {{submission_time}}
- Their website: {{website}}
- Their ad spend: {{adSpend}}
- Their challenge: {{challenge}}

The email should:
1. Confirm receipt and set expectations (we'll prep the audit before the call)
2. Offer 2–3 call time slots (Mon–Fri, 10:00–17:00 CET)
3. Ask them to send Google Ads and Meta Ads view access
4. Feel personal, not automated

Sender: Nicu from 7code
Keep under 150 words.
```

---

## 3. Audit Findings Summary

```
Based on the following PPC account data, write a structured audit summary for a client call.

Account: {{client_name}} — {{website}}
Channels: Google Shopping, Meta Ads
Data provided: {{paste data here}}

Format:
1. Account Health Score (1–10) with brief rationale
2. Top 3 Issues Found (ranked by revenue impact)
3. Top 3 Quick Wins (implementable in <2 weeks)
4. 90-Day ROAS Potential (conservative estimate)
5. Recommended Plan Tier: Starter / Growth / Scale

Be specific. Use numbers. No vague advice.
```

---

## 4. Variant Performance Review

```
Here are the results from our Meta Ads A/B headline test (Sprint 1):

Variant A — "Fire your PPC agency": CTR {{a_ctr}}%, CPL €{{a_cpl}}, Leads: {{a_leads}}
Variant B — "Wasted spend": CTR {{b_ctr}}%, CPL €{{b_cpl}}, Leads: {{b_leads}}
Variant C — "ROAS benchmark": CTR {{c_ctr}}%, CPL €{{c_cpl}}, Leads: {{c_leads}}

Total spend: €{{total_spend}}

Analyse the results:
1. Which variant wins and why?
2. What does the data suggest about audience intent?
3. What should we test in Sprint 2?
4. Should we scale, pivot offer, or change audience?

Be direct. No hedging.
```

---

## 5. Landing Page CRO Review

```
Review this landing page for conversion rate optimisation opportunities.

URL: https://7code-ecom-ppc.vercel.app/
Offer: Free PPC audit
Current CVR: {{cvr}}%
Traffic source: Meta Ads (paid)

Evaluate:
1. Hero section — clarity and hook strength (1–10)
2. Trust signals — are they sufficient for a cold audience?
3. Form friction — is the form too long/short?
4. CTA placement and copy
5. Mobile experience (based on code review)
6. Top 3 specific changes to test next

Be specific about what to change and why, referencing the actual page sections.
```
