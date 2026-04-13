# Beamer Presentation: Brokers and Atypical Technology

## Overview

This folder contains a complete beamer presentation based on the paper "Brokers and Atypical Technology: Network Position, Bridging, and Innovation in Patent Teams."

The presentation reuses the structure and styling from the TDK presentation template while adapting all content to match the current research paper.

## Folder Structure

```
presentation/
├── main.tex                    # Main presentation file
├── main.pdf                    # Compiled presentation (output)
├── frames/                     # All slide content by section
│   ├── 01_intro/
│   │   └── intro.tex          # Introduction and research question
│   ├── 02_data/
│   │   ├── data_sources.tex   # Data sources and sample
│   │   └── variables.tex      # Key variables and measures
│   ├── 03_methods/
│   │   ├── method1.tex        # Network construction
│   │   ├── method2.tex        # Atypicality and econometric model
│   │   └── method3.tex        # Moderating factors
│   ├── 04_results/
│   │   ├── main_results.tex   # Main brokerage effect
│   │   ├── comparison.tex     # Comparison and alternative specifications
│   │   └── robustness.tex     # Robustness checks
│   ├── 05_conclusion/
│   │   └── conclusion.tex     # Conclusion and thank you
│   ├── 06_discussion/
│   │   ├── findings.tex       # Key findings and implications
│   │   └── implications.tex   # Policy recommendations
│   └── 07_backup/
│       └── backup.tex         # Backup slides
├── imgs/                       # Image folder (for figures and logos)
└── README.md                   # This file
```

## How to Use

### Compiling the Presentation

To compile the presentation to PDF:

```bash
cd presentation
pdflatex main.tex
```

Or use your LaTeX editor (Overleaf, TeXshop, VSCode with LaTeX workshop, etc.)

### Editing Slides

Each section is organized in a separate `.tex` file:

1. **To modify content:** Edit the `.tex` files in the `frames/` folder
2. **To reorder slides:** Modify the `\input{}` statements in `main.tex`
3. **To add figures:** Place images in the `imgs/` folder and reference them in the slide files

### Key Placeholders to Fill In

The presentation contains several placeholders marked with `[INSERT ...]` that you should fill in with actual values from your analysis:

- **In `04_results/main_results.tex`:**
  - Brokerage coefficient and significance
  - Effect magnitude and interpretation
  
- **In `04_results/comparison.tex`:**
  - Results for alternative network measures
  
- **In `04_results/robustness.tex`:**
  - Thresholds results (Z < 0, Z < -1, Z < -2)
  
- **In `05_conclusion/conclusion.tex`:**
  - Contact information / affiliations

### Adding Figures and Tables

To add figures:

1. Place your image files in the `imgs/` folder
2. Reference them in the slide files using:
   ```latex
   \includegraphics[width=0.8\textwidth]{../imgs/your_figure_name.pdf}
   ```

### Styling

The presentation uses:

- **Theme:** Berlin
- **Colors:** Navy blue (#0E213B) and Berlin Light (RGB 200,220,240)
- **Custom boxes:**
  - `\begin{pill}...\end{pill}` for highlighted text
  - `\begin{eqbox}...\end{eqbox}` for important statements

## Slides Overview

| Section | # Slides | Content |
|---------|----------|---------|
| Introduction | 3 | Research question, motivation, theoretical foundation |
| Data | 3 | Data sources, sample distribution, key variables |
| Methodology | 4 | Network construction, atypicality measurement, econometric model |
| Results | 5 | Main effects, heterogeneous effects, robustness checks |
| Discussion & Conclusion | 5 | Key findings, implications, limitations, recommendations |
| Backup | 3 | Additional results and appendix materials |
| **Total** | **~23** | Excluding title/ToC |

## Customization

### Change Author/Date

Edit the metadata section in `main.tex`:

```latex
\title{Brokers and Atypical Technology}
\subtitle{...}
\author[Bruinsma, Virág]{...}
\date[\today]{\today}
```

### Add University Logo

Add to `main.tex` after `\begin{document}`:

```latex
\logo{\includegraphics[scale=0.1]{../imgs/corvinus_logo.eps}}
```

(Place your logo in the `imgs/` folder)

## Compilation Notes

- The presentation is built on the **Berlin** beamer theme
- Uses **English** language (\usepackage[english]{babel})
- Includes **mathematics** support and **TikZ** for diagrams
- Supports **PDF and PostScript graphics**

## Next Steps

1. **Fill in the placeholders** with actual results and values
2. **Add figures** from your paper to the `imgs/` folder and reference them
3. **Customize colors** if desired (edit `\definecolor` commands in `main.tex`)
4. **Add appendix content** to the backup slides
5. **Compile and review** the PDF output
6. **Share** the presentation!

## Template Credit

This presentation template was adapted from the TDK presentation structure (frames organization and beamer styling) and customized for the brokerage-atypicality research project.

---

**Questions or improvements?** Feel free to edit the .tex files or contact the research team.
