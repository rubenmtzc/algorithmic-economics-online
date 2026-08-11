# Computational Economics, Causal ML and AI

A research-level learning programme covering research computing, statistical learning, causal ML, deep learning, optimisation, reinforcement learning, algorithmic game theory, multi-agent learning, and structured/foundation models.

## Local preview

1. Install [Quarto](https://quarto.org/docs/get-started/) and Git.
2. Clone this repository.
3. In a terminal, run:

```bash
quarto preview
```

Quarto will render the site and open a local preview.

## Publish with GitHub Pages

1. Replace every `rubenmtzc` in `_quarto.yml` with your GitHub username.
2. Create a GitHub repository named `algorithmic-economics-online`.
3. Push this folder to its `main` branch.
4. On GitHub go to **Settings → Pages → Build and deployment → Source → GitHub Actions**.
5. Push any subsequent change to `main`; `.github/workflows/pages.yml` will render and deploy the site.

Your project-site URL will normally be:

`https://rubenmtzc.github.io/algorithmic-economics-online/`

## Editing workflow

```bash
git pull
quarto preview
# edit .qmd files
git add .
git commit -m "Update causal ML module"
git push
```

## Content model

Every module should follow:

**Learn → Implement → Replicate → Extend → Research**

Use `modules/module-template.qmd` when adding new modules.

## References

The shared bibliography is `references/references.bib`. Cite with Quarto/Pandoc keys, for example:

```text
[@chernozhukov2018dml]
```

## Licence

Suggested: CC BY 4.0 for written teaching material and an MIT/BSD-style licence for original code. Add formal licence files before public release.
