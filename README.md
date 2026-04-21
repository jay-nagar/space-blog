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

## Deploy to Netlify
1. Push this project to a GitHub repo.
2. In Netlify, create a new site from that repo.
3. Build command: `npm run build`
4. Publish directory: `dist`
5. Set your production site URL in `astro.config.mjs`.
6. Update `public/admin/config.yml` with your GitHub repo name.

## Decap CMS setup
This starter uses the GitHub backend.

Update this line in `public/admin/config.yml`:
```yml
repo: your-github-username/your-repo-name
```

If you want editorial access without giving full repo access, you can later switch to a more advanced GitHub auth flow or a different CMS setup.

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
