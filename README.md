# sudodoc — A clean, modern LaTeX document template

A LuaLaTeX template inspired by the Typst Thesis Starter aesthetic. Dark title pages, styled TOC, chapter dividers, and consistent typography.

## Quick Start

```latex
\documentclass[12pt]{article}
\usepackage{sudodoc}

\sudodocsetup{
  title={Your Document Title},
  subtitle={A Subtitle or Tagline},
  author={Author Name},
  institution={University Name},
  date={May 2026},
}

\begin{document}
  \maketitlepage        % dark full-bleed title page
  \maketoc              % styled TOC page
  \chapterpage{1}{Introduction}  % chapter divider
  \section{Background}
  Your content here.
\end{document}
```

Compile: `lualatex sample.tex` (run **twice** for TOC + overlays)

## Features

- **Title page**: Dark full-bleed design with accent stripe
- **TOC**: Styled with TikZ leader lines and accent colors
- **Chapter dividers**: Dark pages with large watermark numbers
- **Section headings**: Three levels (section, subsection, subsubsection) with TikZ decorations
- **Tables**: `\rowcolorhead` / `\rowcoloralt` helpers for booktabs tables
- **Lists**: Styled bullets (triangles, squares), colored enumerate badges, description lists
- **Code listings**: Syntax highlighting with left accent bar
- **Blockquotes**: tcolorbox with left accent bar and warm background
- **Headers/footers**: Subtle section name + page numbers

## Requirements

- LuaLaTeX (TeXLive 2024+)
- Standard packages: booktabs, enumitem, titlesec, titletoc, tcolorbox, listings, etc.
- See `install-texlive.sh` for a portable installation script

## Known Issues

- `\insertsection` produces a non-fatal warning in LuaLaTeX (titlesec fallback handles it correctly)
- Compilation takes 2-4 minutes on first run due to font loading
- Always compile **twice** for correct TOC and TikZ overlays

## Files

- `sudodoc.sty` — the style package
- `sample.tex` — full demonstration document
- `sample.pdf` — compiled output
- `install-texlive.sh` — portable TeXLive installer
- `.gitignore` — keeps the repo clean

## License

MIT
