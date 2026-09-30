# Kingsley Chinaka - Personal Portfolio

Welcome to the source repository for my personal portfolio website. It is a lightweight, fast, and accessible site that showcases my work, background, and how to get in touch.

🌐 **Live site:** https://portfolio.kheengz.workers.dev

## Features

- **Hero section** – a strong first impression with name, role, and a short pitch.
- **About section** – a short bio with skill chips that highlight core competencies.
- **Six-card Portfolio grid** – a curated grid showcasing six projects.
- **Contact form** – opens the visitor's default email client via `mailto:` (no backend required).
- **Light/dark toggle** – theme switching that respects user preference.
- **Responsive layout** – works smoothly across mobile, tablet, and desktop.

## Tech Stack

- **Astro** – static site generator used to build the site.
- **Cloudflare Workers** – hosts the static build at the workers.dev address.

## Project Structure

```
.
├── astro.config.mjs        # Astro configuration (static output)
├── wrangler.jsonc          # Cloudflare Workers configuration (assets: ./dist)
├── package.json            # Dependencies and scripts (astro, wrangler)
└── src/
    └── pages/
        └── index.astro     # Main page (inline scripts, global styles)
```

## Quick Start

Clone the repository, then run the following from the project root:

```bash
npm install
npm run dev
```

The dev server starts at **http://localhost:4321**.

To produce a production build into `./dist`:

```bash
npm run build
```

## Deployment

See [DEPLOYMENT.md](./DEPLOYMENT.md) for the full step-by-step guide to deploying this site to Cloudflare Workers via Git.
