# Deployment Guide - Kingsley Chinaka Portfolio

This guide walks through running the site locally, pushing the source to GitHub, and connecting the repository to Cloudflare Workers for automatic deployments.

## 1. Run Locally

Clone the repository, then from the project root run:

```bash
npm install
npm run dev
```

The Astro dev server starts at http://localhost:4321.

## 2. Push to GitHub

From the project root, initialize a Git repository and push it to GitHub. Suggested repository name: **`kingsley-chinaka-portfolio`**.

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/<your-username>/kingsley-chinaka-portfolio.git
git push -u origin main
```

Replace `<your-username>` with your GitHub username.

## 3. Connect Cloudflare Workers

1. Sign in to the Cloudflare dashboard.
2. Go to **Workers & Pages** > **Create**.
3. Choose **Connect to Git**.
4. Select the `kingsley-chinaka-portfolio` repository.
5. Configure the build settings:
   - **Build command:** `npx astro build`
   - **Deploy command:** `npx wrangler deploy`
6. Click **Save and Deploy**.

Cloudflare will install dependencies, build the site into `./dist`, and deploy it as a Worker.

## 4. Auto-Redeploy

Once connected, every push to the `main` branch triggers a new build and deployment automatically — no manual steps needed.

## 5. Alternative local deploy

Authenticate Wrangler, then build and deploy:

```bash
npx wrangler login
npm run deploy
```

## Notes

- **Contact form:** the form uses `mailto:` and opens the visitor's default email client. There is **no backend**, so no secrets or API keys are required.
- **workers.dev address:** the site is live at `https://portfolio.kheengz.workers.dev`. A custom domain can be attached later from the Workers settings.
