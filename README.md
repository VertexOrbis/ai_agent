# VertexOrbis Technologies - Official Corporate Website

Official corporate website for **VertexOrbis Technologies** (`https://vertexorbis.com`), focusing on AI systems, cloud infrastructure, and workflow automation.

## Project Structure

```
vertexorbis/
├── index.html                  # Main responsive one-page corporate website
├── styles.css                  # Modern dark-tech stylesheet
├── robots.txt                  # Search engine crawler permissions
├── sitemap.xml                 # XML sitemap
├── assets/                     # Lightweight SVG graphics & icons
│   ├── logo.svg
│   ├── hero-tech.svg
│   ├── ai-agents.svg
│   ├── cloud-infrastructure.svg
│   └── automation.svg
├── docs/                       # Specifications and planning docs
├── .gitignore                  # Git ignore rules (.env, secrets)
└── README.md
```

## Local Development & Preview

You can preview the website locally using any standard static file server:

```bash
# Using Python
python3 -m http.server 8000

# Or using npx serve
npx serve .
```

Then visit `http://localhost:8000`.

## Cloudflare Pages Deployment

Deploy to Cloudflare Pages via Wrangler:

```bash
export CLOUDFLARE_ACCOUNT_ID="<your-account-id>"
export CLOUDFLARE_API_TOKEN="<your-api-token>"

# Deploy to Cloudflare Pages project 'vertexorbis'
npx wrangler pages deploy . --project-name=vertexorbis --commit-dirty=true
```

## Security & DNS Boundaries

- **Email Routing**: `vertexorbis.com` uses Cloudflare Email Routing for `business@vertexorbis.com`. Never modify or delete MX, SPF, or DKIM records.
- **Secrets Management**: API tokens and account credentials must remain in `.env` and must not be committed to Git or published in client-side code.
