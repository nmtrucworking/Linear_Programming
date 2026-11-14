<p align="center"><img src=".github/assets/linear-programming-banner.svg" width="100%" alt="Linear programming LaTeX notes banner" /></p>

<h1 align="center">Linear Programming</h1>
<p align="center"><strong>Reproducible mathematical lecture notes, worked methods and exercises</strong></p>
<p align="center">
  <a href=".github/workflows/latex-build.yml"><img src="https://github.com/nmtrucworking/Linear_Programming/actions/workflows/latex-build.yml/badge.svg" alt="LaTeX workflow status (live GitHub badge)" /></a>
  <img src="https://img.shields.io/badge/LaTeX-source-6C4A80" alt="LaTeX source" />
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-3D6A59" alt="MIT license" /></a>
</p>
<p align="center">
  <a href="#topics-covered">Topics</a> · <a href="#manuscript-build-flow">Document pipeline</a> ·
  <a href="#requirements">Build</a> · <a href="#project-structure">Structure</a> · <a href="CONTRIBUTING.md">Contributing</a>
</p>

## Topics covered

| | Area | Contents |
| :--: | --- | --- |
| <img src=".github/assets/icons/geometry.svg" width="34" height="34" alt="Graphical optimization icon" /> | **Foundations** | LP formulation and graphical method |
| <img src=".github/assets/icons/simplex.svg" width="34" height="34" alt="Simplex tableau icon" /> | **Algorithms** | Simplex method, exercises and tables |
| <img src=".github/assets/icons/duality.svg" width="34" height="34" alt="Duality icon" /> | **Extensions** | Duality and transportation models |

## Manuscript build flow

```mermaid
flowchart LR
  MAIN[main.tex] --> PRE[preamble.tex and appendix settings]
  MAIN --> CH[Chapter source files]
  MAIN --> AP[Appendices and exercises]
  PRE --> TEX[LaTeX compiler]
  CH --> TEX
  AP --> TEX
  TEX --> PDF[main.pdf]
```

```mermaid
flowchart LR
  MODEL[LP formulation] --> GEO[Graphical intuition]
  GEO --> SIMPLEX[Simplex method]
  SIMPLEX --> DUAL[Duality]
  DUAL --> TRANS[Transportation applications]
  TRANS --> PRACTICE[Exercises and sample test]
```

The second diagram is a **pedagogical reading path**, not a claim that every mathematical method derives from the preceding one.

---

## Source and build guide

LaTeX source for lecture notes and exercises on linear programming topics, including simplex method, duality, and transportation models.

## Project Structure

- `main.tex`: main entry file
- `preamble.tex`: shared preamble packages and settings
- `chapters/`: core chapters and topic sections
- `appendix/`: appendix formulas, symbols, and simplex tables
- `exercise_1/`: chapter exercises
- `figures/`: figure sources (TikZ/LaTeX)
- `images/`: image assets
- `sample-test/`: sample test and answer key

## Requirements

- A TeX distribution (TeX Live or MiKTeX)
- `pdflatex` available in terminal

## Build

### Windows PowerShell

```powershell
pdflatex -interaction=nonstopmode -halt-on-error main.tex
pdflatex -interaction=nonstopmode -halt-on-error main.tex
```

Run twice to resolve references and table of contents.

## Clean Generated Files

Generated files are ignored by `.gitignore`. If needed, remove local build artifacts manually.

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) before opening pull requests.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE).
