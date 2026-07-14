# Musical Homeostasis v.1

This folder contains a standalone browser app for a participatory sound activity exploring self-organisation through music.

## Files

- `musical_homeostasis_app.html`: the standalone interactive app.
- `index.qmd`: optional Quarto wrapper page that embeds the app in an iframe.
- `README.md`: this file.

## Suggested placement in your Quarto site

Place this folder in your Quarto project root:

```text
interactive_musical_homeostasis/
├── index.qmd
├── musical_homeostasis_app.html
└── README.md
```

In `_quarto.yml`, make sure Quarto copies the raw HTML app:

```yaml
project:
  type: website
  output-dir: docs
  resources:
    - interactive_musical_homeostasis/musical_homeostasis_app.html
```

Then link to the standalone page from a research, education, or activity page:

```markdown
[Launch Musical Homeostasis v.1](../interactive_musical_homeostasis/){.btn .btn-primary}
```

If linking from a root-level page, use:

```markdown
[Launch Musical Homeostasis v.1](interactive_musical_homeostasis/){.btn .btn-primary}
```

## Facilitation notes

This v.1 app is intentionally static and serverless, so it can run on GitHub Pages. Each participant opens the same page on their own device and produces one sustained tone locally. The group-level sound emerges through the shared room or audio call.

For remote-first use with shared state, a future v.2 would need WebRTC, WebSockets, or another real-time backend.
