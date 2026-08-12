# Algorithmic Economics — restructuring guide

## Important

The package intentionally does **not** include `.github/`, your GitHub Actions workflow, `styles.css`, `.git/`, `CITATION.cff`, or `README.md`. Keep your existing versions.

The only existing files you should deliberately replace are `_quarto.yml` and `index.qmd`.

## 1. Commit your current working site first

In GitHub Desktop, commit and push the current state. Suggested message:

`Checkpoint before two-part site restructure`

## 2. Do not delete your old `modules/` folder yet

Keep it as a temporary source for migration. In particular, retain your populated Stage 1 and ML-foundations material.

Suggested mapping:

- old `modules/01-computing/` → `part2/01-research-computing/`
- old ML-foundations bridge → `part2/02-ml-foundations/`
- old statistical learning → `part2/03-statistical-learning/`
- old causal ML → `part2/04-causal-ml/`
- old deep learning → `part2/05-deep-learning/`
- old optimisation/algorithms → `part2/06-optimisation-algorithms/`
- old bandits/RL → `part2/07-bandits-rl/`
- old MARL → `part2/08-multi-agent-learning/`
- old foundation-model material → `part2/09-structured-foundation-models/`
- old specialisations → `part2/10-research-specialisations/`

Algorithmic game theory and computational mechanism design now belong principally in Part I.

## 3. Copy the new files into the repository root

Copy:

- `_quarto.yml` — replace existing
- `index.qmd` — replace existing
- `404.qmd`
- `about.qmd`
- `part1/`
- `part2/`
- `projects/`
- `resources/`

For `references/references.bib`: if your existing bibliography already contains entries, keep it. Do not replace it with the empty placeholder.

Keep untouched: `.github/`, `.git/`, `styles.css`, `.gitattributes`, `README.md`, `CITATION.cff`.

## 4. Inspect the structure in VS Code

In `_quarto.yml`:

- `navbar:` controls the top menu.
- `sidebar:` defines independent Part I, Part II, Projects, and Resources sidebars.
- `collapse-level: 1` keeps large sidebar sections collapsed initially.
- `reader-mode: true` lets readers hide navigation for focused reading.
- `page-navigation: true` adds Previous/Next navigation.

In module pages, `sidebar: part1` or `sidebar: part2` selects the appropriate sidebar.

Collapsed content uses:

`::: {.callout-note collapse="true"}`

## 5. Commit and push

Suggested commit message:

`Restructure site into Algorithmic Economics Parts I and II`

Then click **Push origin**.

## 6. Check GitHub Actions

Open the repository on GitHub → **Actions** → newest Pages workflow. Wait for a green successful run. Do not change the existing workflow merely because the site structure changed.

## 7. Test the published site

Open:

https://rubenmtzc.github.io/algorithmic-economics-online/

Check:

1. Home displays `Algorithmic Economics`.
2. Part I opens with its own sidebar.
3. Part I sections expand/collapse.
4. Modules 1 and 16 open.
5. Part II opens with its own sidebar.
6. Part II Module 1 opens.
7. Projects opens.
8. Additional Resources opens.
9. Mathematics displays the MIT Real Analysis resource.
10. Search is visible.
11. GitHub links work.
12. Light/dark mode still works.
13. Previous/Next navigation appears on module pages.
14. Collapsible callouts expand and close.

## 8. Migrate old content only after the new site works

Copy useful content from the old `modules/` pages into the new Part II pages. Once everything is migrated, delete the obsolete `modules/` folder in a later, separate commit.
