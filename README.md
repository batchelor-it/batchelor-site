# batchelor.it

Personal site for Jimmy Batchelor - IT leader, wildlife photographer, and occasional overthinker based in Kennesaw, GA.

**Live site:** [batchelor.it](https://batchelor.it)

---

Built with [Astro](https://astro.build) and [Tailwind CSS](https://tailwindcss.com), deployed on [Cloudflare Pages](https://pages.cloudflare.com). No WordPress, no subscriptions - just files, Git, and a domain I already had lying around.

## What's on the site

- **Thoughts** - writing about IT, projects, and whatever's on my mind
- **Photography** - wildlife, macro, landscape, and more
- **Resume** - work history and certs
- **About** - the non-resume version

## Stack

| Tool | Purpose |
|------|---------|
| Astro | Static site framework |
| Tailwind CSS v4 | Styling |
| MDX | Blog posts |
| Cloudflare Pages | Hosting + auto-deploy |
| Formspree | Contact form |

## Local dev

```bash
cd ~/Sites/batchelor-site
npm install       # First time setup
npm run dev       # Start dev server at http://localhost:4321
npm run build     # Production build (Cloudflare does this automatically)
```

## Deploying

Cloudflare Pages auto-deploys on every push to `main`. Just commit and push:

```bash
git add .
git commit -m "your message"
git push
```

Done. Wait about a minute and it's live.

## Common workflows

**Add a blog post**
```bash
# Create the file
touch src/content/thoughts/your-post-title.md

# Required frontmatter:
# ---
# title: "Your Post Title"
# date: 2026-02-23
# description: "One sentence description."
# tags: ["tag1", "tag2"]
# ---
```
Then commit and push - it auto-appears on `/thoughts` and the home page.

**Add a photo**
```bash
# Rename to lowercase with hyphens, drop into the right folder
cp ~/Downloads/my-photo.jpg public/photography/wildlife/my-photo.jpg
```
Then commit and push - it auto-appears in the gallery.

**Add a new photo collection**
1. Create the folder: `mkdir public/photography/your-collection`
2. Add the collection to the arrays in `src/pages/photography.astro` and `src/pages/photography/[collection].astro`
3. Commit and push

**Pull before you push (if editing on GitHub directly)**
```bash
git pull --rebase origin main
git push
```

## Project structure

```
src/
├── layouts/
│   └── Layout.astro          # Global layout, nav, footer
├── pages/
│   ├── index.astro           # Home page
│   ├── thoughts.astro        # Blog listing
│   ├── photography.astro     # Photo gallery
│   ├── about.astro
│   ├── resume.astro
│   ├── contact.astro
│   ├── thoughts/
│   │   ├── [slug].astro      # Individual post pages
│   │   └── tag/
│   │       └── [tag].astro   # Tag filtered listing
│   └── photography/
│       └── [collection].astro
├── content/
│   └── thoughts/             # Blog post markdown files
└── styles/
    └── global.css

public/
├── photography/              # Drop photos here by collection
│   ├── wildlife/
│   ├── luna/
│   ├── macro/
│   ├── plantlife/
│   ├── landscape/
│   ├── astro/
│   ├── street/
│   └── travel/
└── images/                   # About page photos
```