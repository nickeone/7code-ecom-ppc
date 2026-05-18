# DEV NOTES — 7code E-commerce PPC Landing Page

## Deployment

The repo is connected to Vercel. Every push to `main` auto-deploys to:
- **Production**: https://7code-ecom-ppc.vercel.app/

### Manual deploy (if needed)
```bash
vercel --prod
```

## Environment / Placeholders

Replace these before going live:

| Placeholder | Where | What to replace with |
|---|---|---|
| `YOUR_PIXEL_ID` | `index.html` lines 22 & 26 | Real Meta Pixel ID from Meta Events Manager |
| `YOUR_FORM_ID` | `index.html` JS submit handler | Real Formspree form ID (e.g. `xeqwnkpz`) |

## Meta Pixel Setup

1. Go to [Meta Events Manager](https://business.facebook.com/events_manager)
2. Create or select your Pixel
3. Copy the 15-digit Pixel ID
4. Replace `YOUR_PIXEL_ID` in index.html (2 occurrences)
5. Use Meta Pixel Helper Chrome extension to verify PageView and Lead events fire

## Form Setup (Formspree)

1. Create account at [formspree.io](https://formspree.io)
2. Create new form → copy the form ID from the endpoint URL
3. Replace `YOUR_FORM_ID` in the fetch call in index.html
4. Configure email notifications in Formspree dashboard
5. Test with a real submission

## Hero A/B Variants

Test different headlines by appending `utm_content` to the URL:

| UTM | Headline |
|---|---|
| `?utm_content=variant-A` | "Fire your PPC agency — or fix them for free." |
| `?utm_content=variant-B` | "Stop funding your agency's wasted spend." |
| `?utm_content=variant-C` | "Your ROAS should be 4× or higher. Is it?" |
| (none) | Default: "We scale your e-commerce revenue with paid ads." |

Use these as separate ad sets in Meta to A/B test headline performance.

## Logo

The nav/footer currently use the "7c" monogram (CSS gradient box) as a fallback.
To replace with the real 7code brand logo:
1. Download the logo SVG from 7code.tech assets
2. Save as `assets/7code-logo.svg`
3. Replace the `.logo-mark` + `.logo-text` markup with:
   ```html
   <img src="/assets/7code-logo.svg" alt="7code" style="height:32px;width:auto;" />
   ```

## Files

```
index.html          — Campaign landing page (953 lines)
privacy.html        — GDPR privacy policy
assets/             — Static assets (logo, images)
DEV_NOTES.md        — This file
EXECUTION_PLAN.md   — Campaign launch plan
MASTER_PROMPT.md    — Claude prompts for campaign work
```
