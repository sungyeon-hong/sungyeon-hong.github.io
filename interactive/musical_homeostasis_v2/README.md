# Musical Homeostasis v.2: Distributed Tuning

This folder contains a standalone browser app for demonstrating self-organisation through a triangular lattice of musical agents.

## Concept

Each triangular cell has:

- a preferred note, shown as a small dot,
- a current note, shown as the cell colour,
- local neighbours, which it listens to while updating,
- a stability value, which increases when it keeps the same note.

The grid evolves through a rule of **distributed tuning**: each cell balances local harmonic compatibility, memory of its own preferred note, inertia, and noise. The whole grid becomes a collective instrument because the app aggregates pitch counts into a sustained chord field.

This is related to cellular automata such as Conway's Game of Life, but the cells are adaptive musical agents rather than simply alive/dead states.

## Files

- `musical_homeostasis_v2_app.html`: the standalone interactive app.
- `index.qmd`: optional Quarto wrapper page that embeds the app in an iframe.
- `README.md`: this file.

## Suggested placement in your Quarto site

Place this folder in your Quarto project root:

```text
interactive_musical_homeostasis_v2/
├── index.qmd
├── musical_homeostasis_v2_app.html
└── README.md
```

In `_quarto.yml`, make sure Quarto copies the raw HTML app:

```yaml
project:
  type: website
  output-dir: docs
  resources:
    - interactive_musical_homeostasis_v2/musical_homeostasis_v2_app.html
```

Then link to the standalone page from a root-level page:

```markdown
[Launch Musical Homeostasis v.2](interactive_musical_homeostasis_v2/){.btn .btn-primary}
```

or from a subpage:

```markdown
[Launch Musical Homeostasis v.2](../interactive_musical_homeostasis_v2/){.btn .btn-primary}
```

## Audio note

Browsers require user interaction before audio can start, so press **Start audio** inside the app to hear the aggregate chord.
