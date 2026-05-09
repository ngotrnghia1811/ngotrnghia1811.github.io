# Nghia Trung Ngo Personal Site

This folder contains a Quarto website intended to be published to GitHub Pages.

## Before publishing

1. Create a repository named `YOUR_GITHUB_USERNAME.github.io` or another Pages-enabled repository.
2. Use this folder as the root of that repository.
3. Update `site-url` in `_quarto.yml`.
4. Add your GitHub profile link to the navbar if you want it shown publicly.
5. Push to `main` so `.github/workflows/publish.yml` can render and deploy the site.

## Local preview

Install Quarto locally, then run:

```bash
quarto preview
```

## Notes

- The CV PDF and profile image are copied into `files/` and `images/` so the site can publish independently.
- The markdown notes `site-stack-survey.md` and `site-content-draft.md` are intentionally excluded from the public site via the explicit `project.render` list in `_quarto.yml`.