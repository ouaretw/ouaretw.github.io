# ouaretw.github.io

Personal academic website of Walid Ouaret, built with [Quarto](https://quarto.org) and served by GitHub Pages from the `docs/` folder.

## Structure

| Path | Content |
|---|---|
| `_quarto.yml` | site config, navbar, themes |
| `theme-light.scss`, `theme-dark.scss` | color tokens for light / dark mode |
| `styles.scss` | shared layout: cards, status chips, publication and CV styles |
| `index.qmd` | home / about |
| `projects/` | Research page (`index.qmd`) and one page per project |
| `publications.qmd` | publications |
| `media.qmd` | talks, posters, workshops, service |
| `cv.qmd` | CV |
| `blog/posts/` | blog posts, one folder per post |
| `assets/images/` | profile photo, favicon, placeholder |
| `docs/` | **generated**, do not edit by hand |

## Edit → preview → publish

```powershell
cd D:\personal_website
quarto preview          # live preview at http://localhost:xxxx, reloads on save
quarto render           # rebuild everything into docs/
git add -A
git commit -m "Update site"
git push
```

GitHub Pages setting: **Settings → Pages → Deploy from a branch → `main` / `/docs`**.

## Adding content

- **Blog post:** copy `blog/posts/2026-11-18-welcome/` to `blog/posts/YYYY-MM-DD-slug/` and edit `index.qmd`.
- **Publication:** copy a `::: {.wo-pub}` block in `publications.qmd`.
- **Project:** add a card in `projects/index.qmd`; for a detail page, add `projects/<name>.qmd`.
- **Status chips:** `[Current]{.wo-status .current}`, `.prev`, `.submitted`.
- **PDF CV:** add a public version (no phone or home address) as `assets/cv.pdf` and uncomment the link in `cv.qmd`.
