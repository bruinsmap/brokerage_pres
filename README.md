# Conference beamer manual

This folder now contains the repo-visible conference deck for the paper
**"The Micro-Foundations of Innovation: Individual Inventor Brokerage and Atypical Recombination in Europe"**.

It is intentionally built from the original TDK beamer presentation's visual logic:

- Berlin theme
- navy / light-blue palette
- rounded callout boxes
- TikZ-based explanatory slides
- large figure-driven empirical slides
- branded closing slide

## What matters most

If Overleaf is synced to this repository, point the project to compile:

- `presentation/main.tex`

The deck only references assets that now live inside the repository.

## Folder map

```text
presentation/
├── main.tex                  # talk entry point
├── style.tex                 # reusable theme/colors/box definitions
├── frames/                   # slide content by section
├── imgs/
│   ├── branding/             # logo assets
│   └── results/              # copied paper figures used in the slides
└── README.md                 # this manual
```

## How to edit the talk

### Change editorial metadata

Edit `presentation/main.tex`:

- `\title{...}`
- `\subtitle{...}`
- `\author{...}`
- `\institute{...}`
- `\date{...}`

### Change slide order

Edit the `\input{...}` lines in `presentation/main.tex`.

### Change colors later

Edit only `presentation/style.tex`.

The main color controls are centralized here:

- `BerlinLight`
- `navy`
- `accent`
- `softbg`
- `softline`

This means a later palette refresh does **not** require rewriting every frame.

### Change box styles later

Also in `presentation/style.tex`:

- `pill`
- `eqbox`
- `softbox`
- `accentbox`
- `\takeaway{...}`

## How to swap figures

1. Replace the file inside `presentation/imgs/results/`
2. Keep the same filename if you want zero LaTeX edits
3. Or update the `\includegraphics{...}` path in the relevant frame

Current main-talk figures:

- `figure1_marginal_effects.pdf`
- `figure2_temporal_trends.pdf`
- `figure4_network_variants.pdf`

Current backup figures:

- `figure3_country_heterogeneity.pdf`
- `figure6_experience_heterogeneity.pdf`

## Suggested workflow for future talks

1. Duplicate this `presentation/` folder or branch from it
2. Update metadata in `main.tex`
3. Keep `style.tex` as the reusable template layer
4. Replace figures first
5. Only then rewrite slide text
6. Compile twice so navigation and references settle

## How to compile locally

Optional local compile:

```text
cd presentation
pdflatex main.tex
pdflatex main.tex
```

## Design rules used in this deck

- avoid dense bullet lists
- prefer one visual idea per slide
- use figures whenever a plot explains more than text
- keep tables compact and only show coefficients that matter for the spoken narrative
- push secondary heterogeneity and robustness material to backup slides

## If Overleaf still does not update

Then the likely issue is not the GitHub branch but the Overleaf compile target.
Check that the Overleaf project is compiling `presentation/main.tex` rather than a different `main.tex` elsewhere in the repository.
