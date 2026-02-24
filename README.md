# batchelor.it

Personal site for Jimmy Batchelor — IT leader, wildlife photographer, and occasional overthinker based in Kennesaw, GA.

**Live site:** [batchelor.it](https://batchelor.it)

---

Built with [Astro](https://astro.build) and [Tailwind CSS](https://tailwindcss.com), deployed on [Cloudflare Pages](https://pages.cloudflare.com). No WordPress, no subscriptions, no nonsense — just files, Git, and a domain I already owned.

## What's on the site

- **Thoughts** — writing about IT, projects, and whatever's on my mind
- **Photography** — wildlife, macro, landscape, and more
- **Resume** — work history and certs
- **About** — the non-resume version

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
npm install
npm run dev       # http://localhost:4321
npm run build     # Production build
```

Cloudflare Pages auto-deploys on every push to `main`.