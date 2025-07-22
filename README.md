# Lipidomics Meta-Analysis under Temperature Stress

This repository contains R code for performing a comprehensive meta-analysis of plant lipidomic responses to temperature stress (heat and cold). The focus is on heterogeneity and sensitivity analysis, lipid class–specific and molecular species–level modeling. Very-long-chain fatty acids (VLCFAs) are also given special consideration.


##Repository Structure

##Main Features

### Bayesian Hierarchical Modeling
- Conducted separately at the lipid for **cold** and **heat** treatments
- Models include nested structure by study and lipid group
- Priors and diagnostics implemented using `brms`

### Heterogeneity Analysis
- Estimates of heterogeneity (τ²) and inconsistency (I²)
- Forest plots per lipid class/species using `metafor`

### ✅ 3. Sensitivity Analysis
- Leave-one-out influence diagnostics
- Cumulative effect size trajectory plots
- Stratified analysis by tissue and plant species when sufficient studies are available

### ✅ 4. Normality & Non-parametric Testing
- Shapiro-Wilk test for distributional assumptions
- Wilcoxon rank-sum tests comparing heat vs. cold treatment
- Performed per plant species, lipid class, and molecular species

### ✅ 5. VLCFA Analysis
- Special module to explore the role of **very-long-chain fatty acids (≥ C20:0)**
- Distribution trends and treatment effects highlighted

---

## 📦 Dependencies

Install these R packages before running the scripts:

```r
install.packages(c(
  "tidyverse", "brms", "metafor", "bayesplot", "ggpubr", "readr", "patchwork"
))
