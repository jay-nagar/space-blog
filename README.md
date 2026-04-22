# Space Explorer Blog

A kid-friendly space blog built with Astro + Decap CMS + GitHub + Netlify.

## What this includes
- Static Astro blog site
- Simple featured homepage layout
- Markdown-based blog posts
- Decap CMS admin panel at `/admin`
- Netlify-ready deploy config
- GitHub-friendly content workflow

## Local development
```bash
npm install
npm run dev
```

## Local CMS editing
For `/admin` on localhost, run the Decap local backend proxy in a second terminal:

```bash
npm run cms:proxy
```

Then open `http://localhost:4321/admin/`.

This avoids Netlify auth during local development and lets Decap edit the local Git repo directly.

## Deploy to Netlify
1. Push this project to a GitHub repo.
2. In Netlify, create a new site from that repo.
3. Build command: `npm run build`
4. Publish directory: `dist`
5. Set your production site URL in `astro.config.mjs`.

## Decap CMS setup
This project is configured for:
- `local_backend` on localhost while developing
- `git-gateway` in production on Netlify

### Netlify production checklist
1. In Netlify, open your site and enable `Identity`.
2. Set registration to `Invite only` unless you want public signups.
3. Enable `Git Gateway` under Identity services.
4. Invite yourself as an Identity user from the Netlify dashboard.
5. Open `https://your-site.netlify.app/admin/` and complete login there.

The admin page includes the Netlify Identity widget, and the main site includes the redirect script Decap expects after login.

## Content editing
Articles live in:
```bash
src/content/posts/
```

Each post is a markdown file with frontmatter.

## Good next upgrades
- Add article cover image uploads via a media folder
- Add author bio page
- Add tags
- Add related posts
- Add a NASA/APOD widget on the homepage
