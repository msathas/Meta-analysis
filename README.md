# Conserved Mechanisms of Plant Lipidome Remodeling under Heat and Cold Stresses Revealed through a Meta-Analysis

This repository contains R code for performing a comprehensive meta-analysis of plant lipidomic responses to temperature stress (heat and cold). The focus is on heterogeneity and sensitivity analysis, lipid class–specific and molecular species–level modeling. Very-long-chain fatty acids (VLCFAs) are also given special consideration.


##Repository Structure

##Main Features

### Heterogeneity Analysis
- Estimates of heterogeneity (τ²) and inconsistency (I²)
- Forest plots per lipid class/species using `metafor`

### Sensitivity Analysis
- Leave-one-out influence diagnostics
- Cumulative effect size trajectory plots

### Bayesian Hierarchical Modeling (Lipid class response)
- Conducted separately at each lipid class for "cold" and "heat" treatments
- Models include nested structure by study and lipid group
- Priors and diagnostics implemented using `brms`

### Normality & Non-parametric Testing (Molecular species-wise response)
- Shapiro-Wilk test for distributional assumptions
- Wilcoxon rank-sum tests comparing heat vs. cold treatment
- Models were fit for "heat" and "cold" treatments separately and combined for the comparison tests

### VLCFA Analysis
- Special module to explore the role of "very-long-chain fatty acids (≥C22)"
- Distribution trends and treatment effects highlighted

---

## Libraries

Install these R packages before running the scripts:

```r
install.packages(c(
  "tidyverse", "brms", "metafor", "dplyr", "tibble", "readr", "ggplot2", "tidyr", "purrr", "stringr", "posterior"
))
