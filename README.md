# Loneliness, Thinness, and Sex Differences: Mediation Analysis Code

This repository contains the R code used to estimate interventional direct and indirect effects in the study:

Narita et al., “Loneliness and desire for thinness explain sex differences in adolescent internalizing problems.”

The code implements the parametric mediational g-formula and reproduces the quantitative analyses reported in the manuscript.

## File organization

This repository is organized as follows:

* `run_analysis.R`: main analysis script to reproduce the manuscript results
* `helper_functions.R`: supporting functions used by the main script
* `demo/demo_gformula.R`: demo script using synthetic simulated data
* `example_data/example_simulated_data.rds`: example dataset for the demo
* `output/`: directory where analysis results are saved, created automatically if not present

## System requirements

Software:

* R version 4.5.1 or higher
* Required R packages: `tidyverse`, `mice`, `boot`, `data.table`, and `MASS`

Operating systems tested:

* macOS Sonoma
* Windows 10/11
* Ubuntu Linux 22.04 LTS

Hardware requirements:

* No non-standard hardware is required. The code runs on a standard desktop or laptop computer.

## Installation guide

Install R version 4.5.1 or higher.

Install the required R packages:

```r
install.packages(c("tidyverse", "mice", "boot", "data.table", "MASS"))
```

Download or clone this repository:

```bash
git clone https://github.com/ZuiCNarita/Loneliness-thinness-sex-differences-mediation.git
```

Ensure that all `.R` files remain in the same directory structure. Typical installation time is less than 2 minutes on a standard desktop computer.

## Demo instructions

A simple demonstration using synthetic data is included in `demo/demo_gformula.R` and `example_data/example_simulated_data.rds`.

To run the demo, start R in the repository directory and execute:

```r
source("demo/demo_gformula.R")
```

Expected output includes estimated interventional direct and indirect effects, bootstrap-based confidence intervals, and diagnostic summaries printed to the console. The expected run time for the demo is approximately 30–60 seconds on a standard desktop computer.

## Instructions for use with real data

To run the mediational g-formula on real data, provide an analytical dataset containing the variables listed in the Methods section of the manuscript, formatted in the same structure as the demo data. Modify file paths and dataset names in `run_analysis.R` as appropriate for your environment.

Outputs include the total effect, overall effect, interventional direct effect, interventional indirect effect, difference term, effect ratio, and bootstrap confidence intervals.

## Reproducing the manuscript analyses

The Tokyo Teen Cohort data are not publicly available due to ethical restrictions and data-use agreements. Researchers with authorized access to the required analytical dataset can reproduce the manuscript analyses by preparing the dataset in the same structure as the demo data, updating the file paths in `run_analysis.R`, and running:

```r
source("run_analysis.R")
```

This script runs the mediational g-formula analysis and writes effect estimates to the `output/` directory.

## License

This code is released under the MIT License, an Open Source Initiative-approved license. Users may freely use, modify, and distribute the code with appropriate attribution.

## Contact

For questions related to this software, please contact:

Zui C. Narita
Email: [zuinarita@ncnp.go.jp](mailto:zuinarita@ncnp.go.jp)
GitHub: https://github.com/ZuiCNarita
