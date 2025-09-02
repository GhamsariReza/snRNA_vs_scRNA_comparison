![Python](https://img.shields.io/badge/python-3.9%2B-blue)
![R](https://img.shields.io/badge/R-4.0%2B-green)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

# Utilities and Custom Scripts

This repository contains a collection of **personalised scripts and utilities** I developed for my reseach projects as a bioinformatician.  
Most scripts are tailored for **single-cell RNA-seq (scRNA-seq) analysis**, but some are general-purpose for data visualisation and file conversion.

## Features
- 🧬 **scRNA-seq analysis**: custom QC, clustering, mutation burden analysis, and integration with Seurat/Scanpy  
- 📊 **Visualisation**: helper scripts for UMAP/TSNE plots, violin plots, and publication-ready figures  
- 🔄 **File conversion**: BAM ↔ VCF, count matrix formatting, metadata restructuring  
- 🛠️ **General utilities**: data wrangling, parsing, and automation helpers  

## Example Usage
```bash
# Clone the repository
git clone https://github.com/<GhamsariReza>/<customized-scripts>.git
cd <customized-scripts>

# Example: mutation-expression association
python scRNAseq/mutation_expression.py --input data/matrix.mtx --meta metadata.csv --output results.csv

