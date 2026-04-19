# web.hallidayinc.com — Project Guide

## What This Is
Single-page conversion-focused landing page for Halliday's Managed Website Program. Target buyer: small business owners, solo consultants, coaches, small nonprofits. The page's only job is to convert visitors (from referrals, organic, or paid ads) into booked calls or inquiries.

## This Is NOT
- A thought leadership site (no blog, no insights, no "about our philosophy")
- A portfolio site
- A general Halliday company site (that's hallidayinc.com)
- A site with multiple services or offerings

## Tech Stack
- **Framework:** Astro (latest stable)
- **Styling:** Plain CSS with CSS custom properties (no Tailwind, no frameworks)
- **JavaScript:** Vanilla JS only
- **Fonts:** Google Fonts — Cormorant Garamond (display) + Outfit (body) — matches Halliday brand
- **Deployment:** Static hosting via GitHub Pages (subdomain: web.hallidayinc.com)
- **Images:** Stored in `public/images/`

## Design System

### Colors (Halliday brand)
```css
--navy: #1B2A4A;          /* primary dark */
--navy-deep: #0F1A30;     /* darker navy */
--teal: #2A9D8F;          /* primary accent */
--teal-deep: #21867A;     /* darker teal */
--teal-light: #E6F4F2;    /* soft teal tint */
--coral: #E76F51;         /* CTA accent, use sparingly */
--cream: #FAF9F6;         /* warm background */
--white: #FFFFFF;
--grey-warm: #6B7D85;
--grey-mid: #94A3A9;
--grey-pale: #E9EDEF;
--charcoal: #2C3E44;
```

### Typography
- **Display/headings:** 'Cormorant Garamond', Georgia, serif (weights 300, 400, 500)
- **Body/UI:** 'Outfit', 'Helvetica Neue', sans-serif (weights 300, 400, 500, 600)
- Section headings use `<em>` for italic accent words colored `--teal`

### Design Principles
- **Conversion > decoration.** Every section serves the funnel.
- **Single CTA.** All buttons drive to the same destination (inquiry form or mailto).
- **Story first, features second.** Lead with the gap narrative.
- **Trust signals early.** Klara's site must appear above the fold or immediately below.
- **Mobile-first.** Over half of ad traffic is mobile — the mobile experience cannot be an afterthought.
- **Fast load.** Static site, optimized images, minimal JS. Target Lighthouse > 95.

## Page Sections (in order)

1. **Nav** — minimal. Just logo + "Get Started" CTA button.
2. **Hero** — the hook. Strong headline, single CTA, trust signal.
3. **The Gap** — 3-column comparison (DIY / Managed / Custom).
4. **What You Get** — grid of included features with icons.
5. **How It Works** — 5-step process (same as one-pager).
6. **Real Example** — Klara's site as the social proof anchor.
7. **Who This Is For** — self-qualification checklist.
8. **FAQ** — handle objections that ad traffic will surface.
9. **Final CTA** — inquiry form section.
10. **Footer** — minimal, with one-line Halliday attribution.

## Contact Flow
All CTAs route to: `mailto:web@hallidayinc.com?subject=Managed%20Website%20Program%20Inquiry`

(In Phase 2, we'll swap this for a form + tracking. For Phase 1, mailto is fine.)

## Commands
- `npm run dev` — local dev
- `npm run build` — production build
- `npm run preview` — preview build

## Deployment (astro.config.mjs)
```js
export default defineConfig({
  site: 'https://web.hallidayinc.com',
  output: 'static',
});
```

## Content Notes
- Klara Farkas has granted permission to be named and linked as the reference example.
- Her site: klarityinternational.com
- Real testimonial pending — use a brief placeholder with italic note until replaced.
- Halliday contact email: chris@hallidayinc.com (general), web@hallidayinc.com (program-specific)
