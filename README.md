# Wiley Design LaTeX Template

Mirror of the official Wiley journal LaTeX template (USG.cls v6.0, May 2024) from [Wiley Author Services](https://authorservices.wiley.com/).

## Bug Fixes

The original template has bugs in `wileyNJD-Chicago.bst` that cause BibTeX errors. See the [`fixes`](https://github.com/cameronbracken/WileyDesign/tree/fixes) branch for corrections.

## Usage

```bash
# Full build
latexmk -pdf Optimal-Design-layout.tex

# Or manually
pdflatex Optimal-Design-layout.tex
bibtex Optimal-Design-layout
pdflatex Optimal-Design-layout.tex
pdflatex Optimal-Design-layout.tex
```

## Document Class Options

Set in `\documentclass[OPTIONS]{USG}`:

| Option | Description |
|--------|-------------|
| `ASNA` | AMS-style numbered references |
| `APA` | APA author-year style |
| `CHICAGO` | Chicago author-year style |
| `HARVARD` | Harvard style |
| `VANCOUVER` | Vancouver numbered style |
| `twocolumn` | Two-column layout |
| `doublespace` | Double-spaced text |

## Key Files

- `USG.cls` - Wiley document class
- `wileyNJD-Chicago.bst` - Chicago bibliography style
- `Optimal-Design-layout.tex` - Sample document

## License

Template provided by Wiley for use with Wiley journal submissions.
