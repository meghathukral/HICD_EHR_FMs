# HICD project page

GitHub Pages site for **Hierarchical Modeling of ICD Codes in EHR Foundation Models**
(Thukral et al., 2026).

## Local preview

```bash
cd /coc/pcba1/mthukral3/gh_pages_projects/HICD_EHR_FMs
python3 -m http.server 8000
# then open http://localhost:8000
```

## Files

```
HICD_EHR_FMs/
├── index.html       # single-page site
├── style.css        # all styling, no JS
├── assets/          # figures (teaser.png, icd_structure.png, embedding_analysis.png)
└── README.md
```

## Figures to add

The page currently references three images in `assets/`. Replace each with the
matching figure from the paper:

- `assets/teaser.png` — paper Figure 2 (HICD-BERT vs HICD-Graph side-by-side)
- `assets/icd_structure.png` — paper Figure 1 (ICD-10-CM code anatomy)
- `assets/embedding_analysis.png` — paper Figure 3 (embedding similarity bars)

Missing assets render with the figure background color and the figcaption still
shows — broken-image icons won't appear in modern browsers but it's worth
populating these before publishing.

## Update links

`index.html` has placeholder `href="#"` for:

- the paper PDF
- the arXiv link

Replace those with real URLs once you have them. The code link
(`https://github.com/meghathukral/HICD_EHR_FMs`) is already in place.

## Deploy to GitHub Pages

Pick one of:

### Option A — serve `gh-pages` branch (simplest, recommended)

```bash
# from the project root with index.html
git init
git remote add origin https://github.com/meghathukral/HICD_EHR_FMs.git
git checkout -b gh-pages
git add .
git commit -m "site: initial HICD project page"
git push -u origin gh-pages
```

In the repo settings → Pages → Source: choose `gh-pages` branch, root folder.
Site goes live at `https://meghathukral.github.io/HICD_EHR_FMs/`.

### Option B — serve `/docs/` on main branch

Copy `index.html`, `style.css`, and `assets/` into a `docs/` folder on `main`,
push, and set Pages source to `main` branch + `/docs` folder.
