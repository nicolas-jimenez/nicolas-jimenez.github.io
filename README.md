# nicolas-jimenez.github.io

Academic website for Nicolas Jimenez. Plain static HTML/CSS — no build step, no
dependencies, no framework. Edit the `.html` files directly and push.

## Files

| File | What it is |
|---|---|
| `index.html` | Home / about, fields, committee, contact |
| `research.html` | Job market paper, work in progress, presentations, funding |
| `teaching.html` | Teaching and research experience |
| `style.css` | All styling (light + dark mode, responsive) |
| `img/portrait.jpg` | **Placeholder** — replace with a real photo, same filename |
| `files/Jimenez_Nicolas_CV.pdf` | CV, converted from the `.docx` |
| `.nojekyll` | Tells GitHub Pages to serve the files as-is |

## Preview locally

```
cd nicolas-jimenez.github.io && python3 -m http.server 8000
```

Then open http://localhost:8000.

## Deploy

The repo must be named exactly `nicolas-jimenez.github.io` for GitHub to serve it at
that address from the repository root.

1. Create an **empty** public repo at https://github.com/new named
   `nicolas-jimenez.github.io` (no README, no .gitignore, no license).
2. From this folder:

```
git remote add origin https://github.com/nicolas-jimenez/nicolas-jimenez.github.io.git
git branch -M main
git push -u origin main
```

3. GitHub Pages turns on automatically for a `<username>.github.io` repo. If it does
   not, go to Settings → Pages and set Source = "Deploy from a branch", branch `main`,
   folder `/ (root)`.
4. The site appears at https://nicolas-jimenez.github.io (first build takes a minute or
   two).

Every later `git push` republishes.

## Before going live — open items

- [ ] Replace `img/portrait.jpg` with a real photo (portrait crop, ~800px wide is plenty)
- [ ] Decide whether the personal phone number in the CV PDF should stay (it is a
      public page)
- [ ] Re-export the CV to PDF from Word if the LibreOffice conversion lost formatting
- [ ] Add the JMP PDF to `files/` and uncomment the PDF link in `research.html`
- [ ] Write the Kenya project blurb (`research.html`, marked with a TODO comment)
- [ ] Uncomment the job-market line in `index.html` once that decision is made
- [ ] Update the "Last updated" line in the footer of each page
