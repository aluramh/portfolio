# Deploying

## How it works

This project is connected to Vercel via GitHub. **Pushing to `main` automatically deploys to production.** No manual steps needed for normal updates.

## Normal workflow

```
# Make changes on a feature branch
git checkout -b my-changes
# ... edit files ...
git add -A
git commit -m "..."
git push origin my-changes
```

Then merge the branch into `main` on GitHub — Vercel picks it up automatically within ~1 minute.

## Manual deploy (from local machine)

If you need to deploy without going through GitHub:

```bash
vercel --prod --yes
```

Requires the Vercel CLI (`npm install -g vercel`) and being logged in (`vercel login`).

## Custom domain (alexram.dev)

The domain needs to be added once in the Vercel dashboard:

1. Go to [vercel.com](https://vercel.com) → your `portfolio-new` project
2. Settings → Domains → Add `alexram.dev`
3. Follow the DNS instructions Vercel shows (usually a CNAME or A record at your registrar)

Once DNS propagates (~minutes to hours depending on registrar), `alexram.dev` will serve the live site.

## Vercel project

- **Project:** `portfolio-new` under `alex-ramirezs-projects-c7927572`
- **Dashboard:** https://vercel.com/alex-ramirezs-projects-c7927572/portfolio-new
- **Current production URL:** https://portfolio-new-ten-smoky.vercel.app
