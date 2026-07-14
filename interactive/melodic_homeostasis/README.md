# Melodic Homeostasis: Regulated Variation from a Motif

This folder contains a standalone browser app for generating short melodies from a seed motif using transparent, rule-based procedures.

## Concept

The demo treats a melody as a trajectory through pitch space. A user enters an initial motif, such as:

```text
E4 G4 A4 Bb4 E4
```

The app extracts motif features:

- anchor note
- interval pattern
- contour
- range
- pitch-class material

It then generates four different variations from the same motif using explicit rule parameters:

- motif loyalty
- exploration
- tension
- resolution strength
- rhythm mode
- phrase length

This is not an AI music generator trained on large datasets. It is a small, inspectable, rule-based system for exploring how musical coherence can emerge through regulated variation.

## Files

- `melodic_homeostasis_app.html`: standalone interactive app.
- `index.qmd`: optional Quarto wrapper page.
- `README.md`: this file.

## Features

- Motif input using note names, including accidentals such as `Bb4`, `B♭4`, and `F#4`.
- Clickable C4–B5 piano keyboard for building and auditioning an initial motif.
- Play motif, clear motif, and remove-last-note controls before generating variations.
- Four-output variation gallery for comparing different trajectories from the same input.
- Piano-roll visualisation.
- Playback using Web Audio.
- MIDI export for the selected variation.
- Motif analysis panel.
- Hover/click explanation for generated notes.

## Suggested placement in your Quarto site

Place this folder in your Quarto project root:

```text
interactive_melodic_homeostasis/
├── index.qmd
├── melodic_homeostasis_app.html
└── README.md
```

In `_quarto.yml`, make sure Quarto copies the raw HTML app:

```yaml
project:
  type: website
  output-dir: docs
  resources:
    - interactive_melodic_homeostasis/melodic_homeostasis_app.html
```

Then link to the standalone page from a root-level page:

```markdown
[Launch Melodic Homeostasis](interactive_melodic_homeostasis/){.btn .btn-primary}
```

or from a subpage:

```markdown
[Launch Melodic Homeostasis](../interactive_melodic_homeostasis/){.btn .btn-primary}
```

## MIDI export

Because the app generates symbolic notes directly, MIDI export is more appropriate than recording audio. MIDI keeps pitch, timing, and tempo editable in notation software or a digital audio workstation.
