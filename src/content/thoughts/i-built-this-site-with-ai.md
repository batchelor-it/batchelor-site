---
title: "I Built This Site with AI"
date: 2026-02-22
description: "I built this site with AI. Here's why I'm not sorry about it."
tags: ["meta", "cloudflare", "astro", "ai"]
---

AI is overblown - that much is true. Every company is scrambling to slap it on something, and most of what comes out is marketing slop. I get the frustration.

But here's where I land on it: at its core, AI has this remarkable cantilever-like ability to help people punch above their weight. When I was researching self-hosting and website options, I'd occasionally see someone mention using AI in a comment thread. They'd get flamed immediately. And honestly? Fair. As of early 2026 the internet is drowning in AI-generated garbage - unoriginal at best, actively misleading at worst.

I know that. And I still used it to build this site.

Here's the thing - I know very little about coding. I've built sites before using WordPress and Squarespace. WordPress always ended up slow and bloated, Squarespace felt expensive for how little I actually needed. After some research I found I could host a static personal site on Cloudflare Pages and GitHub for free. No catch - except I knew nothing about GitHub and barely enough CSS to get myself into trouble.

So I used Claude to vibe code (apparently that's the term now) this entire site from scratch. A seasoned web developer would probably wince at the source code. I know it's basic - but my needs are basic. Somewhere to jot down thoughts, put my resume online, and maybe have my ramblings be useful to someone. That last part is kind of the whole point of IT anyway.

## So how does it actually work?

The site is built with Astro - a static site framework that spits out plain HTML, CSS, and JavaScript. No database, no server, no monthly bill. The styling is handled by Tailwind CSS, and blog posts like this one are written in plain Markdown files that I just drop into a folder.

The whole thing lives on GitHub, and every time I push a change, Cloudflare Pages automatically rebuilds and deploys it to batchelor.it in about a minute. The contact form runs through Formspree which forwards messages to my email. Total monthly cost: zero dollars.

The photography gallery reads directly from a folder of images - to add a new photo I just drop a file in the right place and it appears automatically. Same with posts - write a Markdown file, save it, done.

Is it the most elegant codebase? Probably not. But it loads fast, it's mine, and I can change anything about it without asking anyone's permission or paying for a subscription. That's honestly pretty cool.

If you're curious about the specific tools - Astro, Cloudflare Pages, GitHub, and Formspree all have solid free tiers and decent documentation. Claude helped me wire it all together, but those are the building blocks.

Is it perfect? Not even close. But it's a start, and honestly I'm pretty happy with how it turned out for someone who had to ask an AI what a git repository was when I first started on this little journey. If you've got thoughts, feedback, or just want to tell me the code is terrible - I'd love to hear it. The contact form works, I checked. Comments would be even better, but I haven't figured that out yet - coming soon to a website near you.
