# Distal Outcome Reporting in Mixture Models

Reproducible Quarto/R workflow accompanying:

**Carter, D. B. (2026). _Distal Outcomes in Mixture Modeling: A Guide for Pairwise Comparisons, Multiplicity Control, and Effect Size Reporting._ Behavior Research Methods.**

**Article DOI:** https://doi.org/10.3758/s13428-026-03144-4

## Supplement D

This repository contains the reproducible post-estimation workflow provided as Supplement D to the article.

**[View the rendered Supplement D workflow](https://delwincarter.github.io/distal-outcomes-mixture-reporting/)**

The workflow is designed for researchers who have already estimated a latent class or latent profile model and obtained distal outcome results from their preferred mixture-modeling software.

It provides a reproducible reporting layer for computing and organizing:

- class-specific standard deviations
- weighted grand means
- LTB-ω global effect sizes
- pairwise mean differences
- pooled standard deviations
- pairwise Cohen's *d*
- standard errors and 95% confidence intervals for Cohen's *d*
- Bonferroni-adjusted *p*-values
- Holm-adjusted *p*-values
- Benjamini–Hochberg/FDR-adjusted *p*-values

## Scope

The workflow is software-agnostic and operates on post-estimation quantities obtained from mixture-modeling software.

It does **not**:

- estimate the mixture model
- determine the number of latent classes or profiles
- conduct the omnibus Wald test
- automatically extract values from Mplus or other software

The same workflow can be used with results obtained from Mplus, Latent GOLD, SAS-based LCA workflows, StepMix/StepMixR, R-based mixture-modeling packages, or other software when the required post-estimation quantities are available.

## Required Inputs

The workflow requires six inputs:

- `class_label` — class or profile labels
- `class_prob` — estimated class membership probabilities
- `class_mean` — class-specific distal outcome means
- `class_variance` — class-specific within-class distal outcome variances
- `class_n` — class-specific sample sizes or estimated class counts
- `pairwise_p` — pairwise comparison *p*-values

The included BMLSS example demonstrates the complete workflow using a four-class solution. The pairwise *p*-values in the example are instructional values selected to illustrate differences among multiplicity-adjustment procedures.

## Repository Files

| File | Description |
|---|---|
| `supplement-d-distal-reporting-workflow.qmd` | Quarto/R source for Supplement D |
| `index.html` | Rendered Supplement D workflow published through GitHub Pages |
| `distal-outcomes-mixture-reporting.Rproj` | RStudio project file |

## Requirements

The workflow requires:

- R
- Quarto
- the R package `gt`

If needed, install `gt` in R with:

```r
install.packages("gt")
