# Kingsley Chinaka Portfolio

## What this is

This is an Astro starter kit that wraps Kingsley Chinaka's existing single-page portfolio without redesigning or changing its visible content. It builds as a fully static site and is ready to deploy to Cloudflare Workers Static Assets from a GitHub repository.

## Prerequisites

- Node.js 18 or newer
- A GitHub account
- A Cloudflare account (the free tier is fine)

## Run locally

```bash
npm install
npm run dev
```

Open [http://localhost:4321](http://localhost:4321) in your browser.

## Push to GitHub

Run these commands from the project directory:

```bash
git init
git add .
git commit -m "Initial commit"
```

Create an empty GitHub repository named `kingsley-chinaka-portfolio`, then run:

```bash
git remote add origin https://github.com/<your-username>/kingsley-chinaka-portfolio.git
git branch -M main
git push -u origin main
```

## Deploy to Cloudflare Workers from GitHub (recommended)

1. Open the Cloudflare dashboard.
2. Go to **Workers & Pages**.
3. Select **Create application**.
4. Select **Workers**, then **Connect to Git**.
5. Select the `kingsley-chinaka-portfolio` repository.
6. Set the build command to:

   ```bash
   npx astro build
   ```

7. Set the deploy command to:

   ```bash
   npx wrangler deploy
   ```

8. Select **Save and Deploy**.

Every future Git push to `main` redeploys the site automatically.

## Alternative local deploy

Authenticate Wrangler, then build and deploy:

```bash
npx wrangler login
npm run deploy
```

## Notes

- The site is fully static.
- The contact form opens the visitor's email client using a `mailto:` link, so no backend is needed.
- A custom domain can be added later in the Cloudflare Workers settings.
