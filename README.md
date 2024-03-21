# Quarto: Reproducible Publishing

Slides

## Abstract

[Quarto](https://quarto.org) is a system for weaving together code and narrative to create fully reproducible documents, presentations, websites, and more. You can combine R, Python, Julia, or any language with a Jupyter kernel, with advanced authoring features such as cross-references, callouts, citations, and equations. You can write your content in a Jupyter notebook or Quarto's own plain text format in your favorite editor, or use VS Code or RStudio for a richer editing experience.

In this talk, I'll give you a tour of Quarto's capabilities, touch on ways Quarto extends and unifies RMarkdown, and demo working with Quarto documents in RStudio and VS Code.

## Bio

Dr. Charlotte Wickham (she/her) is a Developer Educator on the Developer Relations team at Posit with a focus on Quarto. As part of her job at Posit, Charlotte helps to keep quarto.org—a website about, and also built with, Quarto—up to date. Prior to Posit, she taught Statistics and Data Science at Oregon State University where she received awards for her in-person and online teaching.

## Acknowledgments

This talk is heavily based on:

-   Mine Çetinkaya-Rundel's talk: <https://github.com/mine-cetinkaya-rundel/quarto-rladies-cologne>

-   Isabella Velásquez's workshop: <https://github.com/ivelasq/2022-10-27_intro-to-quarto/tree/main>

## Demo

### Setup

-   Quarto 1.4.551

-   RStudio 2023.12.1+402 (currently bundles Quarto 1.3)

-   R 4.3.3 +  `install.packages(c("tidyverse", "ggthemes", "palmerpenguins"))`
-   Visual Studio Code + Quarto Extension 

-   JupyterLab + Quarto Extension

### Documents

-   Open `index.qmd` in RStudio

-   Point out components: YAML header, R code cells (could by Python), markdown everywhere else.

-   Render: button, command palette, shortcut.

-   Change `format: pdf`. Render. Back to `format: html`

-   Switch to Visual Editor

-   Add bold and link:

    -   <https://allisonhorst.github.io/palmerpenguins/>

-   Add code chunk options:

    - Try `message: true`  
    
    - Set `echo: false`

    - Set `echo: false` in `execute` in the YAML header
    
    - Add `fig-cap`: 
    
        ```
        #| fig-cap: "A scatterplot of three species of penguins showing the relationship between bill depth and bill length."
       ```

-   Cross-reference the figure and the table:

    -   Add `fig-` to `label`, "Insert Anything"

-   Add a citation: DOI 10.1371/journal.pone.0090081

-   Switch to Source Editor

-   Output to PDF, output to Word.

### VS Code

-   Same file

-   Show Visual Editor

-   Buttons + Command Palette

## Optional Extras

-   `layout`
-   Callouts
-   Equations
-   HTML: `code-fold: true`, tabsets, `theme: darkly`

### JupyterLab

`python3 -m jupyter lab python.ipynb`

-   Similar file starting, but now in Python

-   Add YAML header

-   Preview from Terminal

-   Add code cell options

### Websites

- Add `quarto.yml` 

```
project:
  type: website

website:
  title: "Hello Quarto"
  navbar:
    left:
      - index.qmd
      - talk.qmd
```

- Render
- Add other formats to index.qmd:

```
format:
  html: default
  pdf: default
```

- Navigation
- Add one more document with R chunk
- Freeze
- Themes and dark theme toggle
- `publish quarto`



