# Personal academic website (Quarto)

## Preview locally
1. Install Quarto: https://quarto.org/docs/get-started/ (or `brew install --cask quarto`)
2. In this folder run `quarto preview` — the site opens in your browser and reloads as you edit.

## Where things live
| What | File |
|---|---|
| Home page / bio / profile links | `index.qmd` |
| Publication list | `publications/publications.yml` |
| Talks | `publications/index.qmd` |
| Photo (optional) | add `image: files/profile.jpg` to the top of `index.qmd` |
| Visualisations | one folder per item in `research/` (copy `example-visualisation`) |
| Affiliations & links | `affiliations.qmd` |
| Menu, title, theme | `_quarto.yml`, `styles.scss` |

Search the project for `TODO` to find every placeholder.

## Publish on GitHub Pages
1. Create a GitHub repository named `USERNAME.github.io` (your GitHub username).
2. In this folder:
   ```
   git init -b main
   git add .
   git commit -m "Initial site"
   git remote add origin https://github.com/USERNAME/USERNAME.github.io.git
   git push -u origin main
   ```
3. On GitHub: Settings → Pages → Source → **GitHub Actions**.
4. Every push to `main` now rebuilds the site at `https://USERNAME.github.io`.

If you add pages with Python/Julia code cells, run `quarto render` locally and
commit the `_freeze/` folder so GitHub does not need to re-run your code.
