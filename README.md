# Adi Krishnamoorthy

Personal website, deployed with GitHub Pages: [https://ak4032.github.io](https://ak4032.github.io)

## How to edit

| What | File |
|------|------|
| Name, LinkedIn, Google Scholar, GitHub | `_config.yml` |
| Homepage bio | `index.md` |
| Tabs / navbar | `_layouts/default.html` |
| Colors, fonts | `assets/css/style.css` |
| Profile photo | replace `assets/imgs/profile.png` |
| CV | `pages/cv.md` (or link a PDF from the navbar) |
| Blog / bookmarks pages | files in `pages/` |
| General blog posts (bubbles) | files in `_posts/` |

To add a new tab, create a markdown file in `pages/` with this header:

```yaml
---
layout: default
title: My New Page
---
```

Then add a link in `_layouts/default.html`. Jekyll turns `pages/my-new-page.md` into `/pages/my-new-page.html`.

## How to add a General blog bubble

Clicking **Blog** or **Blog → General** opens a page of post “bubbles,” like [aritang.github.io](https://aritang.github.io/). Travel, Restaurants, and Festivals stay as their own dropdown pages. Anything else goes here.

1. Add a file under `_posts/` named `YYYY-MM-DD-short-slug.md` (the date is when it shows up on the bubble).
2. Use this header, then write the post below it:

```yaml
---
layout: default
title: My new post
excerpt: One or two sentences that appear on the bubble.
---
```

3. Push to GitHub. A new bubble appears on the General blog page and links to `/blog/short-slug.html`.

There is already a sample post at `_posts/2026-08-19-hello-from-the-blog.md`. Edit or delete that file when you write a real one.
