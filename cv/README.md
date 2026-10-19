# CV

- `main.tex`: the current LaTeX source.
- `../_data/cv.yml`: the same content for the website's `/cv/` page.
- `../assets/pdf/Resume_Marcus_Tiedemann_Oekland_Henriksboe.pdf`: the downloadable PDF linked by that page.

When changing the CV, update the LaTeX source and website data together, rebuild
the PDF, and commit all three. The empty `assets/json/resume.json` is not used by
the current CV page.

From the repository root, with TeX Live and `latexmk` installed:

```sh
latexmk -pdf -interaction=nonstopmode -halt-on-error -outdir=cv/.build cv/main.tex
cp cv/.build/main.pdf assets/pdf/Resume_Marcus_Tiedemann_Oekland_Henriksboe.pdf
```

Review both PDF pages before publishing. Build files in `.build/` are ignored.
