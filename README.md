# bemorin.com

> **"Impossible is nothing when you have a system. Let me show you how you can do it."**

This is the engine behind my personal brand. Built with **Astro**, deployed on **Vercel**, and powered by **Coda**.

## 🛠 The Tech Stack
- **Framework:** [Astro](https://astro.build/) (Ultra-fast static generation)
- **Styling:** [Tailwind CSS](https://tailwindcss.com/)
- **Data Source:** [Coda API](https://coda.io/developers/apis/v1) (Headless CMS)
- **Deployment:** [Vercel](https://vercel.com/)
- Zero JS dependencies

## Setup

```bash
npm install
npm run dev       # local dev at localhost:4321
npm run build     # production build → /dist
npm run preview   # preview build locally
```

## Deploy to Vercel
1. Push repo to GitHub
2. Import project on [vercel.com](https://vercel.com)
3. Framework preset: **Astro**
4. Build command: `npm run build`
5. Output dir: `dist`

## Deploy to Netlify
1. Push repo to GitHub
2. Import on [netlify.com](https://netlify.com)
3. Build command: `npm run build`
4. Publish dir: `dist`

## Email list
Replace the form handler in `src/components/Newsletter.astro` with your actual provider:
- **ConvertKit**: embed form action URL
- **Beehiiv**: use their embed API
- **Mailchimp**: replace fetch URL with Mailchimp endpoint

## Customization
- Colors / fonts → `src/styles/global.css` (CSS variables at top)
- Products → `src/components/Business.astro` and `src/components/Life.astro`
- Nav links → `src/components/Nav.astro`

## Structure
```
src/
  components/
    Nav.astro          ← sticky navigation
    Hero.astro         ← hero + Business/Life choice panels
    Ticker.astro       ← scrolling marquee strip
    About.astro        ← about section
    Business.astro     ← 4 business products
    Life.astro         ← 4 life products
    Newsletter.astro   ← email capture
    Footer.astro       ← footer
  layouts/
    Base.astro         ← HTML shell + meta tags
  styles/
    global.css         ← design tokens + global styles
  pages/
    index.astro        ← assembles everything
```
