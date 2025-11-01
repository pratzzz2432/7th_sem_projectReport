# EcoSenseNet - Smart Environment Prediction and Alert System

This project is a smart environment prediction and alert system designed for localized areas like a college campus. It integrates IoT sensors, machine learning, and offline communication to deliver real-time environmental predictions and alerts, especially when the internet is unavailable.

## Project Report

The full project report is available in the root directory of this project. The main file is `report.tex`, and the chapters are in the `chapters` directory.

## Presentation

A 5-slide presentation summarizing the project is available in the `presentation` directory.

### Compiling the Presentation

To compile the presentation, you will need a LaTeX distribution with the following packages installed:

*   `beamer`
*   `tikz`

On a Debian-based system (like Ubuntu), you can install these packages with the following command:

```bash
sudo apt-get install texlive-latex-base texlive-latex-recommended texlive-pictures
```

Once you have the necessary packages installed, you can compile the presentation by running the following command in the `presentation` directory:

```bash
pdflatex presentation.tex
```

You may need to run the command twice to ensure all references are correctly generated.
