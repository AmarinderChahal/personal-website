# personal-website

My personal blog: an About page plus blog posts.

It's a fully static site built with [Hugo](https://gohugo.io/) and the
[Hugo Bear Blog](https://github.com/janraasch/hugo-bearblog) theme (default
settings, no template overrides), deployed to GitHub Pages with GitHub Actions.
Search is powered by [Pagefind](https://pagefind.app/) and the newsletter by
[Buttondown](https://buttondown.com/). There is no server-side code.

## Local development

```sh
git clone --recurse-submodules https://github.com/AmarinderChahal/personal-website.git
cd personal-website
hugo server -D   # preview, including drafts
```

To test search locally, do a full build and serve `public/`:

```sh
hugo --gc --minify
npx -y pagefind --site public --glob "blog/*/index.html"
```

## Writing a post

Create `content/blog/<slug>/index.md` (images go in the same folder):

```yaml
---
title: "Post title"
date: 2026-10-10
description: "One-sentence summary"
tags: ["go"]
draft: true
---
```

Drafts show up with `hugo server -D` and never in production builds.

## Deploy

Pushing to `main` builds the site and deploys it to GitHub Pages
(Settings → Pages → Source: GitHub Actions).
