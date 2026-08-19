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

1. Add a file under `_posts/` named **exactly** `YYYY-MM-DD-short-slug.md`.
   - The date must be real (`2026-08-19` is fine; `2024-07-35` is not).
   - Use hyphens, not spaces: `2026-08-19-test-second.md` works, `Test _second.md` does not.
   - Jekyll ignores any file in `_posts/` that does not match this pattern, so it will never show up on the site.
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

## Getting the site onto Google

Google has not indexed https://ak4032.github.io yet. That is normal for a new personal site with few inbound links. Verification is **not** something I can finish for you: Google Search Console only accepts the Google account that owns the site.

The repo already has `robots.txt` and a sitemap at https://ak4032.github.io/sitemap.xml. To verify with the **URL prefix** method:

1. Open [Google Search Console](https://search.google.com/search-console) while signed into your Google account.
2. Click **Add property** → **URL prefix** → enter `https://ak4032.github.io`.
3. Choose **HTML tag**.
4. Copy only the `content="..."` value (a long string), not the whole tag.
5. Paste it into `_config.yml` as `google_site_verification: "THAT_STRING"` (uncomment that line) and push to `main`.
6. Wait a minute for GitHub Pages to rebuild, then click **Verify** in Search Console.
7. After it verifies, go to **Sitemaps**, submit `https://ak4032.github.io/sitemap.xml`, then **URL Inspection** → `https://ak4032.github.io/` → **Request indexing**.

If you paste the verification string here, I can drop it into `_config.yml` for you. Indexing can still take days after a successful request.
