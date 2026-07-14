# Interactive Conway's Game of Life demo

This folder contains a standalone browser app for exploring Conway's Game of Life as a simple model of emergence and complexity.

## Files

- `game_of_life_demo_app.html`: the standalone interactive app.
- `index.qmd`: optional Quarto wrapper page that embeds the app in an iframe.
- `README.md`: this file.

## Suggested placement in your Quarto site

Place this folder in your Quarto project root:

```text
interactive_life/
├── index.qmd
├── game_of_life_demo_app.html
└── README.md
```

In `_quarto.yml`, make sure Quarto copies the raw HTML app:

```yaml
project:
  type: website
  output-dir: docs
  resources:
    - interactive_life/game_of_life_demo_app.html
```

Then link to the standalone page from a research or education page:

```markdown
[Launch Game of Life demo](../interactive_life/){.btn .btn-primary}
```

If linking from a root-level page, use:

```markdown
[Launch Game of Life demo](interactive_life/){.btn .btn-primary}
```

## Features

- Two editable grids for side-by-side comparison.
- Click and drag to set initial conditions.
- Run, step, initialise, randomise, and copy-plus-perturb controls.
- Boundary mode: bounded edges or wrapped torus.
- Speed and density sliders.
- Difference counter for comparing the two grids.
