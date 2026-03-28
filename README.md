# Resume — PDF from LaTeX

This folder has two PDF options:

| File | Style | Notes |
|------|--------|--------|
| `Venkateswara_Reddy_M_moderncv.tex` | **moderncv** (classic) | Icon header, traditional CV look; needs the **moderncv** class. |
| `Venkateswara_Reddy_M_article.tex` | **article** (custom) | Clean sans layout, accent section rules, date/role alignment; only standard packages. |

The Markdown file `Venkateswara_Reddy_M_Staff_Frontend_Costco.md` is a content reference; edit the `.tex` files for PDF output.

## Prerequisites

- A full TeX distribution (**MacTeX**, **TeX Live**, or **MiKTeX**) with:
  - `pdflatex`
  - The **moderncv** class (usually installed with the distribution)

## Generate the PDF

From this folder (where `Venkateswara_Reddy_M_moderncv.tex` lives):

```bash
pdflatex Venkateswara_Reddy_M_moderncv.tex
```

Run **twice** if you change cross-references or want a stable PDF (TOC/outline):

```bash
pdflatex Venkateswara_Reddy_M_moderncv.tex
pdflatex Venkateswara_Reddy_M_moderncv.tex
```

Output: **`Venkateswara_Reddy_M_moderncv.pdf`**

### Alternative layout (article / UX-focused)

```bash
pdflatex Venkateswara_Reddy_M_article.tex
```

Output: **`Venkateswara_Reddy_M_article.pdf`** (2 pages with the current content).

## Clean auxiliary files (optional)

```bash
rm -f Venkateswara_Reddy_M_moderncv.aux Venkateswara_Reddy_M_moderncv.log Venkateswara_Reddy_M_moderncv.out
rm -f Venkateswara_Reddy_M_article.aux Venkateswara_Reddy_M_article.log Venkateswara_Reddy_M_article.out
```

## Troubleshooting

- **`moderncv` not found:** Install/update your TeX distribution or install the `moderncv` package via the package manager (`tlmgr` on TeX Live).
- **Header overlap:** The `.tex` file avoids setting `\makecvheadnamewidth` manually; do not re-enable it unless you adjust the classic layout.
