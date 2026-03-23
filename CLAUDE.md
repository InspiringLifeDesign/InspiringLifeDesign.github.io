# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Running the site locally

The site runs via Docker using a GitHub Pages-compatible Jekyll image:

```bash
docker-compose up
```

The site is then available at `http://localhost:4001`. The `_site/` directory is the build output — never edit files there directly.

## Architecture

This is a Jekyll static site. Key directories:

- `_posts/YEAR/` — blog posts, one subdirectory per year
- `_layouts/` — page templates (`post`, `default`, `home`, `tag_page`, `no_sidebar`, `landing_page`, `redirect`)
- `_includes/` — reusable partials
- `_data/navigation.json` — drives the entire site navigation including submenus
- `_tag_pages/` — one `.md` file per tag; required for tag pages to be generated
- `_config.yml` — site config, permalink structure (`/posts/:title.html`), pagination

## Writing a new blog post

Create `_posts/YEAR/YYYY-MM-DD-post-slug.markdown` with this front matter:

```yaml
---
layout: "post"
title: "Post Title Here"
description: "150-160 character keyword-rich summary of the post."
image: /i/YEAR/header-image.jpg
tags:
  - "2026"        # year tag always required
  - tag-name      # must match a file in _tag_pages/
affiliate: true   # only add if post contains affiliate links
---
```

Standard post structure:
1. Centered header image: `<center><img src='/i/YEAR/filename.jpg' alt='...'></center>`
2. Body content mixing Markdown and HTML
3. AI disclosure line (if AI-assisted): `And yes - I used Claude to help me write this post. It felt only right to practise what I preach.`
4. Italic closing question to readers: `<i>Question for readers...</i>`
5. Share buttons: `{% include sharethis.html %}`
6. Email sign-up include: `{% include listsignup.html list_id="type1" %}`
7. Previous & Next post links
8. Ad include: `{% include advert.html ad_id="latest1" %}`

Note: Pinterest pin images are no longer included in posts. Pins are batch-created separately after multiple posts are published.

## SEO requirements

Every post must have:
- `description` in front matter: 150-160 characters, keyword-rich, no em dashes
- `image` in front matter: path to the header image (enables OpenGraph sharing)
- Title leading with searchable keywords
- Subheadings (H3s) containing relevant keywords where natural
- Descriptive, keyword-relevant image alt text

Do a final SEO check before publishing any post.

## Publishing rules

- NEVER use `git add _posts/` broadly — always stage post files individually to avoid accidentally publishing drafts
- Before publishing, rename the file to today's date (e.g. `2026-03-22-slug.markdown`) even if the draft was started earlier
- NEVER push a NEXT post link until the post it links to is also published
- Add the NEXT link to the previous post at the same time as publishing the new post

## Writing style

- Do not use em dashes (—); use hyphens (-) instead
- Prefer commas or brackets over hyphens when structuring sentences

Images go in `i/YEAR/` for post images and `i/ads/` for ad banners.

## Adding a new tag

Every tag used in a post's front matter needs a matching file in `_tag_pages/`. To add a new tag (e.g. "ai for life design"):

Create `_tag_pages/ai for life design.md`:
```yaml
---
layout: tag_page
title: ai for life design
---
```

The `tag_page` layout automatically lists all posts with that tag.

## Updating navigation

Edit `_data/navigation.json`. The structure supports up to three levels of nesting (`submenu` within `submenu`). Each entry has `title` and `url`; add a `submenu` array for dropdown items.

## Key includes reference

- `{% include advert.html ad_id="latest1" %}` — renders an ad by ID (IDs defined in `_includes/advert.html`)
- `{% include listsignup.html list_id="type1" %}` — newsletter sign-up embed (Mastermind platform)
- `{% include sharethis.html %}` — share buttons (Pinterest, Facebook, WhatsApp)
- `{% include youtube.html videoid="XXXXXXX" %}` — embeds a YouTube video
- `{% include vimeo.html videoid="XXXXXXX" %}` — embeds a Vimeo video

## Affiliate posts

Adding `affiliate: true` to front matter automatically:
- Adds "Ad – Contains affiliate links and previous paid partnerships" at the top of the post
- Adds an affiliate disclosure note at the bottom of the post content
