# MDPI *Computers* submission — Overleaf project

This folder is a self-contained Overleaf/LaTeX project for the manuscript
**"Occlusion-Robust Single-View 3D Reconstruction of Pigs via Discrete Latent
Keypoint Completion and Skeleton Joint-Angle Constraints"**, formatted for the
MDPI journal *Computers* (E-ISSN 2073-431X).

## Structure

```
MDPI_Computers_Submission/
├── main.tex            # Manuscript (uses the official MDPI class)
├── Definitions/        # MDPI class + support files (do not edit)
│   ├── mdpi.cls
│   ├── journalnames.tex
│   ├── mdpi.bst, mdpi_apacite.{bst,sty}, mdpi_chicago.bst
│   ├── logo-mdpi.eps, logo-orcid.pdf, logo-updates.eps
├── fig/                # Figures referenced by main.tex
│   ├── KeyPoint.pdf, fig2.pdf, fig3.pdf
│   ├── DLPCM.pdf, sc.pdf, DLCPM_SC.pdf
└── README.md
```

## How to compile

### On Overleaf
1. Create a new project and upload **all** files in this folder, preserving the
   `Definitions/` and `fig/` sub-folders.
2. Set the compiler to **pdfLaTeX** and the main document to `main.tex`
   (Menu → Settings).
3. Compile. Overleaf converts the `.eps` logo automatically.

### Locally
```bash
latexmk -pdf main.tex      # epstopdf must be available for the .eps logo
```

## Notes

- The journal is selected via the class option `computers` in
  `\documentclass[computers,article,submit,pdftex,moreauthors]{Definitions/mdpi}`,
  which automatically sets the *Computers* E-ISSN (2073-431X); no manual `\ISSN`
  command is needed.
- References are kept inline in a `thebibliography` block, so no external `.bib`
  file is required.
- The manuscript is in `submit` mode (single-column draft layout with line
  numbers), which is what MDPI requests for initial submission.
