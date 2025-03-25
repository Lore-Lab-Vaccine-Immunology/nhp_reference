## Biochemical and hematological reference intervals in rhesus and cynomolgus macaques and implications for vaccine and drug development

Xianglei Yan1,2, Rodrigo Arcoverde Cerveira1,2, Sebastian Ols1,2,4, Klara Lenart1,2, Fredrika Hellgren1,2, Marcos Miranda1,2, Olivia Engstrand1,2, Annika Reinhardt1,2, Bengt Eriksson3 and Karin Loré1,2*

1Division of Immunology and Respiratory Medicine, Department of Medicine Solna, Karolinska Institutet and Karolinska University Hospital, Stockholm, Sweden. 
2Center of Molecular Medicine, Stockholm, Sweden. 
3Astrid Fagraeus laboratory, Comparative Medicine, Karolinska Institutet, Stockholm, Sweden. 
4Current affiliation: Institute for Protein Design, University of Washington, Seattle, WA, USA.

*e-mail: karin.lore@ki.se 


## Table of contents
* [Summary](#summary)
* [General information](#general-information)
* [Preprocessing dataset](#preprocessing-dataset)
* [Repository structure](#repository-structure)
* [Plots and rendered results](#plots-and-rendered-results)
* [Reproducibility](#reproducibility)
* [License](#license)

## Summary

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
- [Blood cell ratio analysis](https://lore-lab-vaccine-immunology.github.io/nhp_reference/results/lab_book/nhp_ratio_references_2025-03-25.html)
- [RNA-seq analysis](https://lore-lab-vaccine-immunology.github.io/nhp_reference/results/lab_book/rna-seq_analysis_2025-03-25.html)

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
git clone https://github.com/Lore-Lab-Vaccine-Immunology/nhp_reference_project

# Install required R packages
Rscript -e "renv::restore()"

# Run the analyses (from within RStudio)
# Open nhp_ratio_references.Rmd and knit
# Open rna-seq_analysis.Rmd and knit
```

## Plots and rendered results

All plots will be generated under the results folder with date-based subfolders. Key outputs include:

* Blood cell ratio distributions by age group and species

* RNA-seq quality control plots

* Differential expression results (volcano plots)

* Pathway enrichment analysis

* Correlation plots between gene expression and biochemical markers