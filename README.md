# Wiley Design LaTeX Template

Mirror of the official Wiley journal LaTeX template (USG.cls v6.0, May 2024) from [Wiley Author Services](https://authorservices.wiley.com/).

## Bug Fixes (this branch)

This branch contains fixes for bugs in `wileyNJD-Chicago.bst` that cause BibTeX errors in the original Wiley template.

### Fixed Issues

- **Undefined variable**: `Volume` (uppercase) changed to `volume` (the actual BibTeX field) on lines 757 and 790
- **Stack corruption**: Removed erroneous double `* *` concatenation operators on lines 765 and 797
- **Orphaned stack item**: Fixed `format.editors.byfml` call in the `book` function that pushed a value without consuming it

### Known Limitations

The original `.bst` file has deeper structural issues with BibTeX stack management that cause warnings (but not errors) during compilation. The bibliography output is still correct despite these warnings.

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
