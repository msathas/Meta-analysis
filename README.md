# Conserved Mechanisms of Plant Lipidome Remodeling under Heat and Cold Stresses Revealed through a Meta-Analysis

This repository contains R code for performing a comprehensive meta-analysis of plant lipidomic responses to temperature stress (heat and cold). The focus is on heterogeneity and sensitivity analysis, lipid class–specific and molecular species–level modeling. Very-long-chain fatty acids (VLCFAs) are also given special consideration.


##Repository Structure

##Main Features

### Effect size calculation
- Loads data, followed by data cleaning
- Label the "heat" and "cold" treatments properly
- Calculates effect size for each observation
 
### Heterogeneity Analysis
- Estimates of heterogeneity (τ²) and inconsistency (I²)
- Forest plots per lipid class/species using `metafor`

### Sensitivity Analysis
- Leave-one-out influence diagnostics
- Cumulative effect size trajectory plots

### Bayesian Hierarchical Modeling (Lipid class response and molecular species response)
- Conducted separately at each lipid class for "cold" and "heat" treatments
- Models include nested structure by study and lipid group
- Priors and diagnostics implemented using `brms`
- Split-platform analysis with platform being removed from the pooled model and fit per platform data (per stress)

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


## AI has been used only to help with codes
