# Trial Design Course Notes

This is a Quarto book project containing course notes on trial design for experimental research in public policy and business applications. The book covers experimental foundations, trial design, execution, and interpretation of results.

## Migration Status: ✅ COMPLETE

All content has been successfully migrated from Canvas LMS export to Quarto format. The `canvas-export/` directory contains the original source HTML files and images for reference.

**Note:** Module 0 (Statistical Concepts and Hypothesis Testing) from Canvas is intentionally excluded - it has been moved to a separate math site.

## Build and Development Commands

### Building the Book

```bash
# Render the entire book (outputs to _book/ directory)
quarto render

# Preview the book with live reload
quarto preview

# Render a single chapter (useful for testing changes)
quarto render experimental-foundations/randomised-trials.qmd
```

### Key Build Outputs

- **HTML output**: `_book/` directory (gitignored via `.quarto/`)
- **Frozen computations**: `_freeze/` directory (stores R execution results)
- The build process uses `freeze: auto` in `_quarto.yml`, meaning R code chunks are only re-executed when their source changes

## Project Structure

### Content Organization

The book is organized into 5 modules as defined in `_quarto.yml`:

1. **experimental-foundations/** - Module 1: Theory of experimental research
2. **before-the-trial/** - Module 2: Pre-trial preparation
3. **running-a-trial/** - Module 3: Trial execution
4. **statistical-power/** - Module 4: Statistical power, error control, and effect sizes
5. **interpreting-trial-results/** - Module 5: Results interpretation

Each module contains multiple chapters stored as `.md` or `.qmd` files, with images in `img/` subdirectories.

### File Types

- **`.qmd` files**: Quarto markdown with embedded R code (interactive elements, calculations)
- **`.md` files**: Plain markdown (static content only)
- **`canvas-export/`**: Images and assets (exported from Canvas LMS)
- **`include/webex.js` and `include/webex.css`**: Interactive quiz/exercise functionality

### Key Configuration Files

- **`_quarto.yml`**: Main configuration (book structure, theme, bibliography, rendering options)
- **`trialdesign.Rproj`**: RStudio project configuration
- **`references.bib`**: Bibliography database
- **`apa-no-ampersand.csl`**: Citation style file
- **`styles.css`**: Custom CSS (primarily KaTeX math font sizing)

## Editing Content

### Adding or Modifying Chapters

1. **New chapters**: Add to appropriate section directory, then update `_quarto.yml` chapters list
2. **Math notation**: Uses KaTeX (configured in `_quarto.yml`). Font size controlled by `styles.css`
3. **Images**: Store in subdirectory `img/` within each section, or use `canvas-export/` for shared assets
4. **Citations**: Add to `references.bib`, reference using `[@key]` syntax

### Quarto-Specific Features

- **Code folding**: Enabled by default (`code-fold: true`)
- **Lightbox**: Auto-enabled for images
- **Figure captions**: Positioned at top (`fig-cap-location: top`)
- **TOC expansion**: Set to level 1 (`toc-expand: 1`)
- **External links**: Open in new window (`link-external-newwindow: true`)

## R Environment

- **RStudio project**: Use `trialdesign.Rproj` to open in RStudio
- **Settings**: 2 spaces for tabs, UTF-8 encoding
- **R profile**: Custom `.Rprofile` exists (check for package loading or options)

## Publishing

- **Site URL**: https://trialdesign.jasoncollins.blog
- **Repository**: https://github.com/jasonacollins/trialdesign
- **License**: CC-BY (Creative Commons Attribution)
- **Author**: Jason Collins

## Common Issues

### Build Failures

- If R code chunks fail: Check `_freeze/` directory and consider deleting to force re-execution
- If math rendering issues: Verify KaTeX syntax (LaTeX-compatible)
- Missing bibliography: Ensure `references.bib` contains all cited keys

### File Modifications

- **Do not edit** files in `_book/` or `.quarto/` (generated content)
- **webex.css has been customized** - preserve the custom color scheme and styling when making changes
