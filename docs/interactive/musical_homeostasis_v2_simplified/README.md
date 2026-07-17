# Musical Homeostasis v.2: Distributed Tuning (simplified)

This is a simplified version of the musical homeostasis demo.

## Main simplifications

- preferred notes were removed, so each cell now has only one visible/current note;
- the lattice is a true equilateral triangular tiling;
- the default scale is a simple C major triad for clearer audio and visual patterns;
- the rule is simplified to local harmonic retuning with a little noise;
- the collective sound is directly tied to the pitch distribution shown in the bars.

## Files

- `musical_homeostasis_v2_simplified_app.html` — standalone interactive app.
- `index.qmd` — Quarto wrapper page embedding the app.
- `README.md` — this file.

## Quarto integration

Place the folder in your Quarto project root:

```text
interactive_musical_homeostasis_v2_simplified/
├── index.qmd
├── musical_homeostasis_v2_simplified_app.html
└── README.md
```

Add the raw HTML app to `_quarto.yml` so it is copied to `docs/`:

```yaml
project:
  type: website
  output-dir: docs
  resources:
    - interactive_musical_homeostasis_v2_simplified/musical_homeostasis_v2_simplified_app.html
```

Link from a root-level page:

```markdown
[Launch Musical Homeostasis v.2](interactive_musical_homeostasis_v2_simplified/){.btn .btn-primary}
```

Or from a subpage:

```markdown
[Launch Musical Homeostasis v.2](../interactive_musical_homeostasis_v2_simplified/){.btn .btn-primary}
```

## Audio note

Browsers require a user interaction before sound can play, so click **Start audio** inside the app.
