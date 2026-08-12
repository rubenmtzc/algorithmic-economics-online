# First publication: minimum steps

## 1. Install once

- Git: https://git-scm.com/downloads
- Quarto: https://quarto.org/docs/get-started/

Optional but recommended: VS Code.

## 2. Personalise

Open `_quarto.yml` and replace every `YOUR-USERNAME` with your GitHub username.

Open `CITATION.cff` and replace the name placeholders.

## 3. Test locally

From PowerShell/Terminal inside the project folder:

```powershell
quarto preview
```

Your browser should open the local site. Press Ctrl+C in the terminal to stop the preview.

## 4. Create the GitHub repository

On GitHub create an **empty public repository** named:

`computational-economics-roadmap`

Do not add a README or `.gitignore` there; they already exist locally.

## 5. Push the site

Replace `YOUR-USERNAME` below, then run:

```powershell
git init
git add .
git commit -m "Initial learning programme"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/computational-economics-roadmap.git
git push -u origin main
```

## 6. Turn on GitHub Pages

In the repository:

**Settings → Pages → Build and deployment → Source → GitHub Actions**

Then open **Actions**. If the first workflow ran before Pages was enabled, re-run it once.

The site should appear at:

`https://YOUR-USERNAME.github.io/computational-economics-roadmap/`

## Everyday workflow

```powershell
quarto preview
# edit files
git add .
git commit -m "Describe the change"
git push
```

Every push to `main` triggers the publishing workflow.
