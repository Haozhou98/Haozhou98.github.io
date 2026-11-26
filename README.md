# haozhou98.github.io

Personal site. Built with Jekyll and served by GitHub Pages from the `main` branch.

## Where things live

| To change | Edit |
|---|---|
| Front-page bio | `index.md` (plain Markdown; a note at the bottom lists the phrases that become links later) |
| Front-page photo | `photo` and `photo_alt` at the top of `index.md`; image files go in `assets/images/` |
| A post | one Markdown file in `_posts/` |
| Teaching clips | `_data/teaching.yml` |
| Misc page | `_data/misc.yml` |
| Colors, fonts, spacing | `assets/css/site.css` |

Writing and Teaching appear in the site nav once they have content: one published post, one clip.

## Writing a post

Create `_posts/YYYY-MM-DD-short-title.md`. It is published at `/writing/short-title/` and listed on the Writing page.

```yaml
---
title: The post title
date: 2026-12-01
# Optional. When paper_title is set, the post ends with "From the paper ...".
paper_title: Title of the source paper
paper_venue: Venue name
paper_year: 2025
paper_url: https://doi.org/...
code_url: https://github.com/...
---
```

Section headings are `##`. Code blocks and Markdown tables are styled as they are. For a figure with a caption:

```liquid
{% include figure.html src="/assets/images/posts/example.png" alt="What the image shows" caption="What the reader should notice." %}
```

Add `published: false` to keep a post out of the site while drafting. `_posts/2026-11-26-layout-test.md` is such a draft; it shows every element of the post layout.

Paper and code links for the two posts that have code:

| Paper | `paper_url` | `code_url` |
|---|---|---|
| Explainable time series features for hard disk drive failure prediction (2025) | `https://doi.org/10.1016/j.engappai.2025.110674` | `https://github.com/Haozhou98/pdm-edge-explainable-portfolio` |
| Hard Disk Drive Failure Prediction with Explainable Time-series Characteristics Tree and Large Language Model Hyperparameter Optimizer (2024) | `https://doi.org/10.21872/2024IISE_7850` | `https://github.com/Haozhou98/hdd-SMART-fd-with-dt-llm-hpo` |

## Previewing locally

The `Gemfile` installs the same Jekyll and plugin versions GitHub Pages uses.

```bash
bundle install
bundle exec jekyll serve          # http://localhost:4000
bundle exec jekyll serve --unpublished   # also shows drafts marked published: false
```
