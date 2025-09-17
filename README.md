![Python](https://img.shields.io/badge/python-3.9%2B-blue)
![R](https://img.shields.io/badge/R-4.0%2B-green)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)


## **Manuscript Title**
Comparative Analysis of Single-Nucleus and Single-Cell RNA Sequencing in Human Bone Marrow Mononuclear Cells: Methodological Insights and Trade-offs

## Table of Contents
- [**Manuscript Title**](#manuscript-title)
- [Table of Contents](#table-of-contents)
- [**Overview**](#overview)
- [**Key Findings**](#key-findings)
- [**Significance**](#significance)
- [**Dataset**](#dataset)
- [**Analysis Workflow**](#analysis-workflow)
- [**Conclusion**](#conclusion)
- [**Repository Structure**](#repository-structure)
- [**Citation**](#citation)
- [📜 **License**](#-license)

## **Overview**  
Bone marrow mononuclear cells (BMMCs) are a diverse population of hematopoietic progenitors and mature immune cells that sustain hematopoiesis and coordinate immune responses. The bone marrow is not only the primary site of blood cell production but also a key niche for various disorders, including blood cancers.
Recent advances in scRNA-seq and snRNA-seq have significantly improved our understanding of cellular composition and molecular dynamics within this complex microenvironment.
However, the choice between these two approaches is influenced by study design, sample type, and preservation conditions. Differences in library preparation and transcript capture efficiency can introduce systematic biases, making it important to account for method-specific features during analysis.
In this work, we performed a comparative analysis of matched scRNA-seq and snRNA-seq datasets from 11 healthy donor BMMC samples, all generated using the 10x Genomics platform. We evaluated:

- Method-specific biases across multiple quality metrics

- Differences in cell type proportions and transcriptomic signatures

- The feasibility and limitations of integrative analysis

![Dataset](Study_Design.png)

## **Key Findings**

- Both scRNA-seq and snRNA-seq reliably captured all major BMMC cell types, despite differences in library complexity.

- Systematic gene length biases exist between the two methods, which can complicate direct integration of datasets.

- Understanding method-specific advantages and limitations is crucial for selecting the optimal approach for specific biological questions.

## **Significance**

- This study provides a resource for researchers aiming to:

- Choose the appropriate single-cell sequencing method based on sample type and research objectives

- Perform method-aware analyses and interpretation of scRNA-seq and snRNA-seq data

## **Dataset**  
For this study, we re-used a publicly available dataset of bone marrow mononuclear cells (BMMCs), originally generated for a multi-modal single-cell benchmarking study. In this dataset, biological samples from multiple healthy donors (aged 22–40) were processed across four different laboratories, where each sample was split into two parts, with one part subjected to transcriptomic profiling using 10x Multiome and the other using 10x CITE-seq. 
For the both scRNA and snRNA, 3' gene expression libraries were sequenced on an Illumina NextSeq 2000 platform using paired-end reads with the following parameters: Read 1 (28 cycles), Index 1 (10 cycles), Index 2 (10 cycles), and Read 2 (90 cycles). 
The targeted sequencing depth was approximately 20,000 reads per cell or nucleus.

**Data Availability** 
Publicly available multiome datasets of healthy donors with GEO accession numbers: [GSE194122](https://www.ncbi.nlm.nih.gov/bioproject/PRJNA799242). For further information, please read and cite [A sandbox for prediction and integration of DNA, RNA, and proteins in single cells](https://datasets-benchmarks-proceedings.neurips.cc/paper/2021/hash/158f3069a435b314a80bdcb024f8e422-Abstract-round2.html).


## **Analysis Workflow**  
The analysis workflow, including the execution order of R and UNIX scripts for data download, preprocessing, and downstream analysis in this project, is schematically illustrated in the following diagram:
 ![Dataset](Script_Overview.png)

## **Conclusion**  
In this study, we did not assume complete agreement between the results, nor was our aim to determine which method is superior. Instead, we conducted a series of analyses and visualisations to compare the outputs from two widely used single-cell RNA sequencing approaches on BMMCs. 
Although our batch correction and cell type annotations demonstrate that integrating datasets from these methods is technically feasible, we do not recommend directly comparing gene expression between the two methodologies. This caution is based on observed methodological biases—such as differences in library size, number of detected genes, and gene length—that may obscure biologically meaningful signals. Furthermore, this study offers practical guidance to researchers specifically bioinformaticians by highlighting key considerations related to the inherent characteristics of 
data generated by each methodology, helping inform decisions during preprocessing and downstream analysis.
Finally, while both methods provide valuable information and have their own advantages and trade‑offs, the choice between them should be guided by a well‑defined study design that considers factors such as sample preservation method (fresh versus frozen), logistical constraints (e.g., timing), and study objectives (e.g., multimodal data). 

## **Repository Structure**

```

snRNA_vs_scRNA_comparison-main/
├── Main_Figures/                                    # Main figures in the Manuscript
├── Supplementary_Figures/                           # Supplementary figures in the Manuscript
└── Scripts/                                         # Analysis scripts and outputs
    ├── Figure_Table_Outputs/                        # Figures and tables generated from scripts
    └── Sessions_Info/                               # R sessions' information
└── README.md                                        #Project overview & instructions
```

- [Main_Figures](Main_Figures/)
- [Supplementary_Figures](Supplementary_Figures/)
- [Scripts](Scripts/)
  - [Figure_Table_Outputs](Scripts/Figure_Table_Outputs)
  - [Sessions_Info](Scripts/Sessions_Info)
- README.md

## **Citation**  
Please cite our paper:
Ghamsari, Reza, et al.  
*"Comparative Analysis of Single-Nucleus and Single-Cell RNA Sequencing in Human Bone Marrow Mononuclear Cells: Methodological Insights and Trade-offs."*  
bioRxiv (2025): 2025-09.  
[https://www.biorxiv.org/content/10.1101/2025.09.08.675012v1](https://www.biorxiv.org/content/10.1101/2025.09.08.675012v1)

## 📜 **License**  
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
