# Nghia Trung Ngo — Personal Site

Source for the personal academic website at **[ngotrnghia1811.github.io](https://ngotrnghia1811.github.io/)**.

Built with [Quarto](https://quarto.org/). The rendered site lives in `docs/` and is served via GitHub Pages from the `main` branch.

## Pages

- **Home** — research overview, current directions, selected publications
- **Research** — detailed theme descriptions with project links
- **Publications** — full list by year
- **Projects** — all 14 research projects and software, grouped by theme
- **CV** — curriculum vitae
- **Blog** — research notes

## Local development

Install [Quarto](https://quarto.org/docs/get-started/) (v1.9+), then:

```bash
# Preview with live reload
quarto preview

# Build the site
quarto render
```

The rendered output goes into `docs/`. After rendering, commit `docs/` and push to deploy.

## Deploy

This site uses the **local build + push** approach:

1. Edit `.qmd` source files
2. Run `quarto render`
3. Commit everything (source + `docs/`) and push to `main`

GitHub Pages serves from `docs/` on the `main` branch.
