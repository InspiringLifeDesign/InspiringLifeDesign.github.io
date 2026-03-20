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
tags:
  - "2026"        # year tag always required
  - tag-name      # must match a file in _tag_pages/
affiliate: true   # only add if post contains affiliate links
---
```

Standard post structure:
1. Centered header image: `<center><img src='/i/YEAR/filename.jpg' alt='...'></center>`
2. Body content mixing Markdown and HTML
3. Italic closing question to readers: `<i>Question for readers...</i>`
4. Share buttons: `{% include sharethis.html %}`
5. Email sign-up include: `{% include listsignup.html list_id="type1" %}`
5. Previous & Next post links
6. Ad include: `{% include advert.html ad_id="latest1" %}`

Note: Pinterest pin images are no longer included in posts. Pins are batch-created separately after multiple posts are published.

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
- `{% include youtube.html videoid="XXXXXXX" %}` — embeds a YouTube video
- `{% include vimeo.html videoid="XXXXXXX" %}` — embeds a Vimeo video

## Affiliate posts

Adding `affiliate: true` to front matter automatically:
- Adds "Ad – Contains affiliate links and previous paid partnerships" at the top of the post
- Adds an affiliate disclosure note at the bottom of the post content
