# Adi Krishnamoorthy

Personal website, deployed with GitHub Pages: [https://ak4032.github.io](https://ak4032.github.io)

## How to edit

| What | File |
|------|------|
| Name, email, LinkedIn, GitHub | `_config.yml` |
| Homepage bio | `index.md` |
| Tabs / navbar | `_layouts/default.html` |
| Colors, fonts | `assets/css/style.css` |
| Profile photo | replace `assets/imgs/profile.png` |
| CV | `pages/cv.md` (or link a PDF from the navbar) |
| Blog / bookmarks pages | files in `pages/` |

To add a new tab, create a markdown file in `pages/` with this header:

```yaml
---
layout: default
title: My New Page
---
```

Then add a link in `_layouts/default.html`. Jekyll turns `pages/my-new-page.md` into `/pages/my-new-page.html`.
