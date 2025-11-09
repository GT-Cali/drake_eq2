\# Drake Equation 2.0: Bayesian Inference on the Prevalence of Observable Extraterrestrial Civilizations



\*\*Author:\*\* J.R. Noble  

\*\*Affiliation:\*\* Independent Researcher / Astrophysics \& Bayesian Modelling  

\*\*Year:\*\* 2025  

\*\*Version:\*\* 1.0  

\*\*License:\*\* MIT  



---



\## 📘 Description

This repository contains the complete reproducibility package for the paper:



> \*Drake Equation 2.0: Bayesian Inference on the Prevalence of Observable Extraterrestrial Civilizations\*  

> J.R. Noble (2025). Submitted to \*Astrobiology / ApJ.\*



This work reformulates the classical Drake Equation within a Bayesian framework to derive posterior distributions for the prevalence of detectable extraterrestrial civilizations. The model incorporates astrophysical priors, detection thresholds, and civilization survival distributions.



All data, scripts, and figures in this repository support the analysis and visualizations presented in the paper.



---



\## 📂 Contents

\- `manuscript\_clean.tex` — AASTeX 6.31 LaTeX source  

\- `manuscript\_clean.pdf` — Publication-ready typeset version  

\- `data/` — All numerical outputs, stress test results, and posterior samples  

\- `figures/` — All generated publication figures  

\- `environment.yml` — Conda environment for exact reproducibility  

\- `references.bib` — Bibliography file  

\- `LICENSE` — MIT License  

\- `README.md`, `CITATION.cff`, `CHANGELOG.md` — Documentation and metadata



---



\## ⚗️ Reproducibility

All analysis is reproducible using the included YAML configuration and Conda environment:



```bash

conda env create -f environment.yml

conda activate drake\_eq2

pdflatex manuscript\_clean.tex



