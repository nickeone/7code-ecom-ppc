# 7code PPC Landing Page — Claude Code Guide

## Project overview

Single-page PPC lead generation site for 7code, a senior e-commerce PPC agency.
Live URL: https://ppc.7code.tech/

**Stack:** Pure HTML/CSS/JS — no build step, no framework. One file per page.

Key files:
- `index.html` — main landing page (all styles inline, all JS at bottom)
- `privacy.html` — privacy policy
- `assets/7code-logo.svg` — wordmark for light backgrounds
- `assets/7code-logo-white.svg` — wordmark for dark backgrounds (footer/hero)

## Design tokens

All CSS custom properties are defined in `:root` inside `index.html`:

```
--teal-start: #006EA6   --teal-end: #00C4CA   --teal-mid: #009BB5
--navy: #0F1C2E         --navy-light: #1A2D42
--accent: #FF6B35       --success: #00A86B    --danger: #E63946
--gradient: linear-gradient(135deg, #006EA6 0%, #00C4CA 100%)
```

Logo accent color: `#2AC8D9`

## Rules

- Never introduce a build tool, bundler, or external dependency.
- Keep all styles in the `<style>` block in `<head>`. No external CSS files.
- Keep all JS in the `<script>` block at the bottom of `<body>`. No external JS files.
- Do not add comments explaining what code does — only add a comment if the WHY is non-obvious.
- Match the existing code style exactly: 2-space indent, single quotes in JS, double quotes in HTML attributes.
- The form submits to Formspree (`https://formspree.io/f/xbdblezl`). Do not change the endpoint.
- UTM parameters must always be captured and forwarded in the form payload.
- Meta Pixel ID: `1676195232675668`. Microsoft Clarity ID: `wtjp0yl622`. Never remove these.
- Always test mobile layout at 375px width before marking a task complete.

## A/B variant system

The page supports three hero variants driven by `utm_content`:
- `default` — standard copy
- `A` (utm_content=variant-a or a) — "Fire your agency" angle
- `B` (utm_content=variant-b or b) — "€5,000 Guarantee" angle

Variants are defined in `heroVariants` object in the JS block. Each variant sets: `tag`, `h1`, `sub`, `formH2`, `formSub`.

## Form qualification logic

`isQualified()` returns true only when ALL three match:
- `revenue`: `1m_3m` or `3m_plus`
- `platform`: `shopify` or `woocommerce`
- `ad_spend`: `2k_10k` or `10k_plus`

The `qualified` boolean is sent in the payload and used to tag Clarity sessions and Meta Pixel events.

## Common tasks

**Add a new section:** Insert between existing `<section>` blocks. Follow the pattern: `.section-tag` → `h2` → `.section-desc` → content grid. Wrap content in `<div class="section-inner">`.

**Add a new A/B variant:** Add a new key to `heroVariants` in the JS, add the corresponding `utm_content` value to the detection block above it.

**Update pricing:** Edit the three `.tier` blocks in the `#pricing` section. The featured tier has class `featured` and a `.tier-badge` child.

**Change form fields:** Add/remove `<div class="form-row">` blocks. Always add a matching `<input type="hidden">` if a new tracking field is needed, and populate it in the UTM capture block.

## Deployment

Deployed via Vercel. Push to `main` triggers auto-deploy. No build command — static output directory is `/` (root).
