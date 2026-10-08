# rd2-etf-cvar-backtest

LaTeX source for **CVaR-Based Portfolio Optimisation for a Malta-Accessible UCITS ETF Basket**, prepared for Research Design 2 at MCAST.

Read the paper: [main.pdf](main.pdf).

## Project files

- `main.tex` — main document and formatting.
- `includes/` — paper sections and figures.
- `sources.bib` — bibliography.
- `main.pdf` — compiled paper.

## Build locally

Install [TeX Live](https://tug.org/texlive/quickinstall.html) or [MiKTeX](https://miktex.org/howto/install-miktex) with PDFLaTeX, BibTeX, the `IEEEtran` class and bibliography style, and the packages used in `main.tex`. Install `latexmk` for automated compilation; it requires Perl.

```sh
git clone https://github.com/ZamirLucky/rd2-etf-cvar-backtest.git
cd rd2-etf-cvar-backtest
latexmk -pdf -outdir=build -interaction=nonstopmode -halt-on-error main.tex
```

Open `build/main.pdf`. To update the root `main.pdf`, omit `-outdir=build`.

If `latexmk` is unavailable, run these commands from the repository root:

```sh
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

## Build on Overleaf

1. Upload a ZIP containing `main.tex`, `sources.bib`, and the complete `includes/` directory, preserving their paths.
2. Set `main.tex` as the main document and **PDFLaTeX** as the compiler.
3. Recompile and download the PDF.
