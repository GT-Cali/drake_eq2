[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.17565867.svg)](https://doi.org/10.5281/zenodo.17565867)


# Drake Equation 2.0: A Bayesian, Time-Dependent, and Observability-Centered Framework

**Author**: Jason Richard Noble  
**Contact**: jayrnoble@gmail.com  
**Publication**: Submitted to The Astrophysical Journal (2025)

## Overview

This repository contains the manuscript, data, and supplementary materials for "Drake Equation 2.0: A Bayesian, Time-Dependent, and Observability-Centered Framework."

The Drake Equation 2.0 is a revised probabilistic framework for estimating the number of currently observable extraterrestrial civilizations (N_obs). This framework improves upon the classical Drake Equation by:

- Employing **Monte Carlo Bayesian integration** with full marginalization over all parameters
- Integrating **time-dependent astrophysical parameters**
- Accounting for **signal survival** over cosmic time through an exponential decay kernel
- Incorporating **detectability** based on real instrument capabilities (MeerKAT, FAST)

## Key Results

- **Median N_obs ≈ 0.26** (log₁₀(N_obs) = -0.58)
- **68% Credible Interval**: [0.05, 1.95]
- **Dominant uncertainties**: Detectability (D, 45%) and abiogenesis rate (λ_L, 30%)
- **Fermi Paradox resolution**: P(k=0 detections) = 73.2% → null result is expected

## Repository Structure

```
drake_eq2_publication/
│
├── manuscript_clean.tex       # Main manuscript LaTeX source
├── references.bib             # Bibliography
├── manuscript_clean.pdf       # Compiled manuscript
│
├── figures/                   # Publication-quality figures (300 DPI)
│   ├── figure1_posterior.png
│   ├── figure2_convergence.png
│   ├── figure3_sobol_indices.png
│   └── figure4_detectability.png
│
├── data/                      # Simulation data and configuration
│   ├── posterior_samples.csv
│   ├── stress_test_results.csv
│   ├── sobol_indices.csv
│   └── montecarlo_config.yaml
│
├── environment.yml            # Conda environment specification
├── README.md                  # This file
└── LICENSE                    # MIT License
```

## Data Files

### `data/posterior_samples.csv`
Representative sample of posterior distribution (5 samples shown; full dataset of 1M samples available upon request).

**Columns**:
- `sample_id`: Sample number
- `log10_Nobs`: Log₁₀ of number of observable civilizations
- `lambda_L`: Abiogenesis rate (Gyr⁻¹)
- `D`: Detectability fraction
- `tau_s`: Signal lifetime (Gyr)
- `f_p`, `f_HZ`, `f_GHZ`, `f_i`, `f_c`: Drake Equation parameters

### `data/stress_test_results.csv`
Results from 9 robustness tests including prior variance sweeps, alternate survival kernels, and Gaussian copula correlations.

### `data/sobol_indices.csv`
Global sensitivity analysis results showing first-order and total-order Sobol indices with 95% confidence intervals.

### `data/montecarlo_config.yaml`
Complete configuration file for Monte Carlo simulation including all prior distributions, integration parameters, and stress test specifications.

## Figures

All figures are publication-quality PNG files at 300 DPI:

- **Figure 1**: Posterior distribution of log₁₀(N_obs) showing KDE, CDF, and histogram
- **Figure 2**: Convergence diagnostics including running median, variance, and seed sensitivity
- **Figure 3**: Tornado diagram showing Sobol sensitivity indices
- **Figure 4**: Detectability contours for MeerKAT and FAST telescopes

## Software Requirements

The analysis was performed using:
- **Python**: 3.10+
- **NumPy**: 1.23+
- **SciPy**: 1.9+
- **Matplotlib**: 3.6+
- **Pandas**: 1.5+ (for data handling)

See `environment.yml` for complete environment specification.

## Reproducibility

All results in the manuscript are reproducible using the configuration in `data/montecarlo_config.yaml`. The random number generator was seeded with value 42 for the production run.

To reproduce the analysis:

1. Set up the environment: `conda env create -f environment.yml`
2. Activate the environment: `conda activate drake_eq2`
3. Run the simulation using the configuration in `data/montecarlo_config.yaml`

**Note**: Full simulation code will be made available on GitHub upon manuscript acceptance.

## Citation

If you use this framework or data in your research, please cite:

```bibtex
@article{Noble2025DrakeEq2,
  author = {Noble, Jason Richard},
  title = {Drake Equation 2.0: A Bayesian, Time-Dependent, and Observability-Centered Framework},
  journal = {The Astrophysical Journal},
  year = {2025},
  note = {Submitted}
}
```

## License

This work is licensed under the MIT License - see the LICENSE file for details.

## Contact

For questions or requests for the full dataset (1M posterior samples), please contact:

**Jason Richard Noble**  
Email: jayrnoble@gmail.com  
GitHub: https://github.com/jason-noble/drake-equation-2.0

## Acknowledgments

This work builds upon decades of research in SETI and astrobiology. We acknowledge the contributions of Frank Drake, Carl Sagan, and the many researchers who have refined the Drake Equation framework over the years.

## Version History

- **v1.0** (2025-11-09): Initial submission to The Astrophysical Journal
- ---

## 📄 Citation

If you use this repository, please cite it as:

**Noble, J. R. (2025). _Drake Equation 2.0: A Bayesian, Time-Dependent, and Observability-Centered Framework._ Zenodo.**  
[https://doi.org/10.5281/zenodo.17565867](https://doi.org/10.5281/zenodo.17565867)

### BibTeX
```bibtex
@misc{Noble2025_DrakeEquation2,
  author       = {Noble, Jason Richard},
  title        = {Drake Equation 2.0: A Bayesian, Time-Dependent, and Observability-Centered Framework},
  year         = {2025},
  publisher    = {Zenodo},
  doi          = {10.5281/zenodo.17565867},
  url          = {https://doi.org/10.5281/zenodo.17565867}
}

