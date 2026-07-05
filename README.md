# Amara Hub Blog

The Amara Hub blog, served at **https://blog.amarahub.org**. Built with Jekyll on the theme structure of the [Artsy engineering blog](https://github.com/artsy/artsy.github.io) (MIT/CC licensed — see LICENSE), rebranded to Amara Hub's brand guidelines (January 2021): League Spartan headings, Source Sans Pro body, and the navy/blue/sky/teal/yellow palette.

## Writing a post

Add a markdown file to `_posts/` named `YYYY-MM-DD-title.md`:

```markdown
---
layout: post
title: "Post Title"
date: 2026-07-05 12:00
author: amarahub   # or an author key from _config.yml
categories: [news]
---

Intro paragraph shown on the index page.

<!-- more -->

Rest of the post.
```

Push to the `source` branch — GitHub Actions builds and deploys automatically.

## Local development

```bash
bundle install
bundle exec rake serve   # http://localhost:4000 (skips slow category pages)
```

## Deployment

- Pushes to `source` trigger `.github/workflows/deploy.yml`, which builds with Jekyll and publishes to GitHub Pages.
- Repo **Settings → Pages** must have Source set to **GitHub Actions**, with custom domain `blog.amarahub.org`.
- DNS: CNAME record `blog` → `<org>.github.io` at the domain host.

## Authors

Add authors in `_config.yml` under `authors:`, then reference the key in a post's `author:` front matter.
