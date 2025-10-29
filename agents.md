# Agent Instructions

This file provides additional guidance for AI agents working with this repository.

## R Code Conventions

### Interactive Elements

The book uses R packages for interactive learning elements:

- `longmcq()`: Multiple choice questions
- `hide()` / `unhide()`: Collapsible content sections
- Webex framework: Client-side interactive exercises

Example pattern from `randomised-trials.qmd`:
```r
opts_counterfactual <- c(
  "Option 1",
  "Option 2",
  answer = "Correct option"
)

longmcq(opts_counterfactual)

hide("Click here to see an explanation")
# Explanation content
unhide()
```

### Code Execution Control

When R code examples require external data or packages that may not be available:
- Use `#| eval: false` to display code without execution
- Replace inline R code (`` `r variable` ``) with actual values in tables/text
- Add notes to users explaining how to run the code themselves

Example:
```r
```{r}
#| eval: false
# Code that requires external data
data <- read.csv("external-file.csv")
```
```

## Canvas Export Reference

The `canvas-export/` directory contains the original Canvas LMS HTML files and images. When converting content from Canvas:

1. **File format choice**: Use `.qmd` if the content needs R code/interactive elements, otherwise use `.md`
2. **HTML to Markdown**: Convert Canvas HTML to clean Markdown/Quarto format
3. **Images**: Canvas images are in `canvas-export/Uploaded Media/` or `canvas-export/*.{jpg,png}` - copy to appropriate `img/` subdirectory
4. **Interactive elements**: Canvas may have embedded videos/iframes - replace with appropriate Quarto equivalents
5. **Update `_quarto.yml`**: Add new files to the appropriate section's chapters list in the correct order
6. **Check references**: Canvas content may reference papers - ensure they're in `references.bib`

**Canvas file naming convention in `canvas-export/wiki_content/`:**
- Main sections: `{number}-{title}.html` (e.g., `7-steps-in-a-randomised-trial.html`)
- Sub-sections: `{number}-dot-{sub}-{title}.html` (e.g., `7-dot-2-random-assignment.html`)
- Sub-sub-sections: `{number}-dot-{sub}-{subsub}-{title}.html` (e.g., `7-dot-2-1-random-sample-versus-random-assignment.html`)

## Agent-Specific Editing Guidelines

### Converting HTML Tabs to Quarto Panel Tabsets

Canvas HTML tabs should be converted to Quarto panel-tabsets:

```markdown
::: {.panel-tabset}
## Tab 1 Title
Content for tab 1

## Tab 2 Title
Content for tab 2
:::
```

### Handling Images

- Copy images from `canvas-export/` to the appropriate module's `img/` subdirectory
- Use relative paths in markdown: `![Description](img/filename.png)`
- Decorative Canvas banners/filler images can be omitted

### Preserving Custom Styling

- **webex.css**: Contains custom color scheme - do not modify the existing styles
- **styles.css**: Contains KaTeX math font sizing - preserve existing rules when adding new styles

## Build Process Considerations

### Frozen Computations

The project uses `freeze: auto` in `_quarto.yml`:
- R code chunks are cached in `_freeze/` directory
- Only re-executed when source changes
- Delete `_freeze/` to force re-execution if needed

### Full Book Rebuild

When making structural changes (deleting files, reorganizing):
- Run full `quarto render` to clean up stale artifacts in `_book/`
- Check for leftover HTML files that should have been removed

## Common Agent Tasks

### Adding a New Chapter

1. Create `.md` or `.qmd` file in appropriate module directory
2. Add images to `img/` subdirectory if needed
3. Update `_quarto.yml` chapters list in correct order
4. Test render: `quarto render path/to/new-file.qmd`

### Restructuring Content

1. Create new file structure
2. Migrate content from old files
3. Update `_quarto.yml`
4. Delete old files
5. Run full `quarto render` to clean up
6. Verify no stale HTML files remain in `_book/`

### Troubleshooting Build Errors

1. **R package errors**: Add `#| eval: false` to problematic chunks
2. **Missing data errors**: Replace inline R code with static values
3. **Math rendering errors**: Check KaTeX syntax compatibility
4. **Bibliography errors**: Verify all citation keys exist in `references.bib`
