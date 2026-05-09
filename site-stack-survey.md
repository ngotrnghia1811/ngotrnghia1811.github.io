# Personal Site Stack Survey

Date: 2026-04-21

## 1. Requirements inferred from the current CV

From the CV files in this workspace, the site needs to support:

- An academic home page with a short research statement.
- A clear publications page, ideally driven from structured data.
- A downloadable CV PDF and a lighter web CV page.
- Sections for education, research experience, and selected projects or benchmarks.
- A blog for research notes, reading notes, benchmark updates, or project retrospectives.
- Easy hosting and low maintenance.
- Good support for equations, code snippets, figures, and paper links.

Strong signals from the current materials:

- You already have a LaTeX CV.
- You already have a BibTeX file at `2024 CV/own-bib.bib`.
- Your profile is research-oriented rather than product-portfolio-oriented.
- Blog support matters, but publications and academic identity are still core.

## 2. Candidate stacks surveyed

### Option A: Academic Pages on GitHub Pages

What it is:

- A Jekyll-based academic personal website template built on Minimal Mistakes.
- Designed for publications, talks, teaching, portfolio pages, blog posts, and a CV page.
- Hosted naturally on GitHub Pages.

Strengths:

- Very close to the standard academic website structure.
- Built-in content types for publications, talks, teaching, portfolio, and posts.
- Free GitHub Pages hosting is a natural fit.
- Strong community usage in academia.
- Good if you want a conventional academic site with minimal design work.

Weaknesses:

- Content model is more page-and-YAML heavy than blog-first writing tools.
- Publications are not as naturally BibTeX-native as some alternatives.
- Local development uses Ruby/Jekyll and can be a bit heavier to maintain.
- Keeping up with upstream template updates can be awkward after customization.

Best fit when:

- You want a classic academic website structure more than a writing-first site.
- You expect to use talks, teaching, and CV-style pages heavily.

### Option B: al-folio on GitHub Pages

What it is:

- A Jekyll theme for academics with built-in publications, CV, blog, and project pages.
- Hosted on GitHub Pages, with strong BibTeX-driven publication support.

Strengths:

- Publications page is generated automatically from BibTeX.
- Good match for your existing `own-bib.bib` file.
- Clean academic design with strong support for math, code, and blog posts.
- Good blog support, including richer article layouts.
- Strong community and active maintenance.

Weaknesses:

- CV workflow is not based on LaTeX directly; you would likely keep your current PDF and optionally maintain a separate web CV.
- Still a Jekyll/Ruby stack, so local setup is not as light as pure Markdown-to-static workflows.
- Slightly less purpose-built than Academic Pages for talks/teaching-specific content types.

Best fit when:

- You want the shortest path from BibTeX publications to a polished academic site.
- You care about blogging enough that the post experience should feel first-class.

### Option C: Quarto Website plus GitHub Pages

What it is:

- A document-first publishing system that can build websites and blogs.
- Can publish to GitHub Pages using `docs/`, `gh-pages`, or GitHub Actions.

Strengths:

- Best writing workflow of the options surveyed.
- Excellent for blog posts with equations, code, notebooks, and figures.
- Clean publishing model and very good support for research notes.
- Good RSS, categories, drafts, and frozen computational posts.
- Flexible deployment to GitHub Pages and other static hosts.

Weaknesses:

- Not as turnkey for academic homepages as Academic Pages or al-folio.
- Publications and CV pages need more custom structuring.
- You would need to design more of the academic information architecture yourself.

Best fit when:

- The blog is the center of the site.
- You plan to publish notebook-backed technical posts regularly.

### Option D: HugoBlox on GitHub Pages or Netlify

What it is:

- A Hugo-based site builder with academic CV and research templates.
- Supports deployment to GitHub Pages and other static hosts.

Strengths:

- Strong academic templates and modular page building.
- Explicit support for publication sync from BibTeX.
- Modern, polished presentation options.

Weaknesses:

- More framework overhead than you need for a single personal academic site.
- Documentation and ecosystem have become more productized than the simpler Jekyll options.
- Higher customization surface than is necessary for your current scope.

Best fit when:

- You want a more modular site-builder feel and are willing to accept more setup complexity.

## 3. Comparison against your needs

| Stack | Publications | Blog | CV fit | Hosting fit | Migration fit from current files | Maintenance burden | Overall fit |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Academic Pages + GitHub Pages | Strong | Good | Strong | Excellent | Good | Medium | Very good |
| al-folio + GitHub Pages | Excellent | Very good | Good | Excellent | Excellent | Medium | Best overall |
| Quarto + GitHub Pages | Moderate | Excellent | Moderate | Excellent | Moderate | Low to medium | Very good if blog-first |
| HugoBlox | Very good | Very good | Very good | Good | Very good | Medium to high | Good |

## 4. Recommendation

### Hosting decision

GitHub Pages is a good fit for you.

Why:

- Your site is content-heavy and mostly static.
- You do not need a database-backed CMS.
- You want free hosting, version control, and easy custom-domain support.
- Blog posts, publication pages, CV PDFs, and research summaries all work well in a static setup.

I would not move you away from GitHub Pages unless you later need:

- gated content,
- forms-heavy workflows,
- server-side applications,
- or a CMS/editor experience for multiple non-technical collaborators.

### Template decision

GitHub Pages is the right host, but Academic Pages is not the single best template for your current materials.

My recommendation order is:

1. **al-folio + GitHub Pages**
2. **Academic Pages + GitHub Pages**
3. **Quarto + GitHub Pages** if you want a blog-first research writing workflow

Why al-folio comes out first for you:

- Your existing BibTeX file is immediately valuable.
- Your profile is academic and publication-centered.
- You want blog posts, and al-folio treats blogging as a strong first-class feature.
- It gives you a polished academic site without forcing you to manually reshape each publication into a custom page format.

Why Academic Pages still remains a strong second choice:

- If you want the most recognizable "academic homepage" structure with dedicated sections for talks, teaching, CV, and publications, it is still excellent.
- If your future site will emphasize talks, courses, teaching, and a structured CV page more than a blog, Academic Pages may be the better long-term choice.

Why Quarto is not the default recommendation here:

- It is the strongest authoring environment for technical blogging.
- But for your current assets, it creates more work around publications and academic profile pages than the Jekyll academic templates.

## 5. What I would build for your site

Recommended top navigation:

- Home
- Research
- Publications
- CV
- Blog
- Projects or Benchmarks
- Contact

Recommended home page content:

- Name, title, affiliation, email, GitHub, Google Scholar.
- A 4-6 sentence research summary based on your current CV.
- 3 selected research themes:
  - Domain adaptation and generalized learning
  - Multilingual and multi-task learning
  - LLM benchmarking and retrieval-augmented systems
- 3 to 5 selected papers with links.
- A short "Current work" block on medical RAG, multilingual knowledge integration, and reasoning benchmarks.

Recommended publications workflow:

- Use the BibTeX file as the source of truth.
- Add paper links, PDF links, code links, and slides where available.
- Mark selected papers on the home page and keep the full list on Publications.

Recommended blog use cases for your profile:

- Benchmark design notes for multilingual or medical RAG.
- Paper reading notes on evaluation and transfer learning.
- Short research updates from ongoing projects.
- Conference reflections and research process posts.

## 6. Concrete recommendation for the next implementation step

If the goal is the best balance of speed, quality, and reuse of your current materials, I would proceed as follows:

1. Use GitHub Pages for hosting.
2. Use al-folio as the template.
3. Keep your existing LaTeX CV as the downloadable PDF.
4. Use `own-bib.bib` as the publications source.
5. Write blog posts in Markdown.
6. Add a simple custom domain later, after the site content stabilizes.

If you specifically prefer the structure of Academic Pages, that is still a valid choice. In that case I would recommend it only if you expect to use the talks, teaching, and structured academic-page content model heavily.

## 7. Sources checked

- Academic Pages site and GitHub repository
- GitHub Pages documentation
- Quarto website and blog documentation
- HugoBlox templates overview
- al-folio demo site and GitHub repository

## 8. Bottom line

- **Best host for you:** GitHub Pages
- **Best template for your current materials:** al-folio
- **Best alternative if you want a classic academic structure:** Academic Pages
- **Best alternative if blogging becomes the center of the site:** Quarto