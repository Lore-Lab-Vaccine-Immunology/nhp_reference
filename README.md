## NHP reference values project


## Table of contents
* [Abstract](#abstract)
* [General information](#general-information)
* [Preprocessing dataset](#preprocessing-dataset)
* [Repository structure](#repository-structure)
* [Plots and rendered results](#plots-and-rendered-results)
* [Reproducibility](#reproducibility)
* [License](#license)

## Abstract

This repository contains code for analyzing NHP (Non-Human Primate) blood cell ratio reference values and RNA-seq data from vaccination studies. The analysis includes:

1. Calculation of key hematological ratios (NLR, MLR, PLR, NMR) from blood cell counts
2. RNA-seq analysis pipeline including quality control, differential expression, and pathway enrichment
3. Correlation analysis between gene expression changes and biochemical markers

## General information

This repository contains all the code used for:
- Blood cell ratio calculations and visualization (`nhp_ratio_references.Rmd`)
- RNA-seq data processing and analysis (`rna-seq_analysis.Rmd`)
- Statistical analysis and visualization of results

If you want to check the code and plots without rerunning the analysis, see our rendered results:
- [Blood cell ratio analysis](link_to_rendered_ratio_analysis)
- [RNA-seq analysis](link_to_rendered_rnaseq_analysis)

## Preprocessing dataset

The preprocessing steps include:
1. Blood cell count data:
   - Loaded from Excel files
   - Calculated key ratios (NLR, MLR, PLR, NMR)
   - Filtered and cleaned data

2. RNA-seq data:
   - Raw counts processed using nf-core RNA-seq pipeline
   - Counts normalized using DESeq2
   - Quality control and filtering of low-count genes
   - Differential expression analysis

## Repository structure
- `src` folder: contains all the source code used for the analysis
- `data` folder: contains input data files (blood counts, RNA-seq counts)
- `results` folder: contains output files and figures
- `renv` folder: contains files for reproducible environment
- `renv.lock` file: contains package versions and dependencies

## Reproducibility

To rerun the analysis and generate plots, you need:
- R (version 4.2.2 or higher)
- RStudio (2022.12.0+353 recommended)
- renv (0.16.0)

Reproduction steps:
```bash
# Clone this repository
git clone https://github.com/yourusername/nhp_reference_project

# Install required R packages
Rscript -e "renv::restore()"

# Run the analyses (from within RStudio)
# Open nhp_ratio_references.Rmd and knit
# Open rna-seq_analysis.Rmd and knit

## Plots and rendered results

All plots will be generated under the results folder with date-based subfolders. Key outputs include:

* Blood cell ratio distributions by age group and species

* RNA-seq quality control plots

* Differential expression results (volcano plots)

* Pathway enrichment analysis

Correlation plots between gene expression and biochemical markers