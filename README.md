# RCPwiki

Source for the RCP Student Wiki — degree plans, RCP policies, important files, and student resources — built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/) and deployed to GitHub Pages.

## Structure

```
docs/
  index.md                 # home page
  degree-plans/             # degree plans & course sequences
  policies/                 # RCP program policies
  important-files/          # forms, templates, documents
  resources/                # student resources
mkdocs.yml                  # site config & navigation
.github/workflows/deploy.yml  # builds & deploys to GitHub Pages on push to main
```

## Adding a page

1. Create a Markdown file under the relevant `docs/` subfolder.
2. Add it to the `nav` section of `mkdocs.yml` so it shows up in the sidebar.
3. Commit and push to `main` — the site rebuilds and redeploys automatically.

## Local preview

```bash
pip install -r requirements.txt
mkdocs serve
```

Then open http://127.0.0.1:8000.

## Enabling GitHub Pages (one-time setup)

In the repo's **Settings → Pages**, set **Source** to **GitHub Actions**. The `deploy.yml` workflow will then publish the site on every push to `main`.
