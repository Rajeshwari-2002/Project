# 🧬 Integrative Microbiome-Immune-Gene Network Signature for Immune Evasion & Survival prediction in Lung Adenocarcinoma

## Overview

Lung adenocarcinoma (LUAD) is the most common subtype of non-small cell lung cancer and exhibits substantial heterogeneity in its tumor microenvironment. Increasing evidence suggests that the lung microbiome influences tumor progression and immune responses. This project integrates microbiome profiling, transcriptomic analysis, immune infiltration estimation, network biology, and machine learning to identify microbiome-associated molecular signatures involved in immune evasion.

The workflow combines microbial diversity analysis with host gene expression to discover potential biomarkers and predictive models for tumor immune status.

## Objectives

* Analyze lung microbiome composition in LUAD samples.
* Perform differential gene expression analysis using TCGA-LUAD RNA-Seq data.
* Estimate immune cell infiltration across tumor samples.
* Correlate microbial abundance with host gene expression.
* Construct gene regulatory and interaction networks.
* Identify microbiome-driven biomarkers associated with immune evasion.
* Develop machine learning models for biomarker prediction.


## Dataset

### Transcriptomic Data

* Source: The Cancer Genome Atlas (TCGA-LUAD)
* Data Type: RNA-Seq Gene Expression

### Microbiome Data

* Source: 16S rRNA sequencing data
* Processed using the QIIME2 pipeline


## Workflow

Raw 16S Reads
        │
        ▼
Quality Control (FastQC)
        │
        ▼
QIIME2 Processing
(DADA2 → Feature Table → Taxonomic Assignment)
        │
        ▼
Alpha & Beta Diversity Analysis
        │
        ▼
──────────────────────────────────────────────

TCGA LUAD RNA-Seq
        │
        ▼
Data Preprocessing
        │
        ▼
Differential Gene Expression (DESeq2)
        │
        ▼
Immune Cell Infiltration Estimation
(TIMER2 / immunedeconv)
        │
        ▼
Immune Phenotype Classification
(Hot vs Cold Tumors)
        │
        ▼
Microbiome–Gene Correlation Analysis
        │
        ▼
Network Construction
(Cytoscape)
        │
        ▼
Survival Analysis
        │
        ▼
Machine Learning
(Random Forest & Cox Regression)
        │
        ▼
Candidate Biomarker Identification


## Tools and Software

| Tool          | Purpose                              |
| ------------- | ------------------------------------ |
| QIIME2        | Microbiome sequence processing       |
| FastQC        | Quality assessment                   |
| DADA2         | Denoising and ASV generation         |
| R             | Statistical analysis                 |
| DESeq2        | Differential expression analysis     |
| TCGAbiolinks  | Download TCGA data                   |
| immunedeconv  | Immune cell estimation               |
| TIMER2        | Immune infiltration analysis         |
| Cytoscape     | Gene regulatory network construction |
| Random Forest | Machine learning classification      |
| Cox regression   | Predictive modeling                  |
| Python        | Data preprocessing and visualization |

## Analysis Pipeline

### 1. Microbiome Analysis

* Quality assessment of raw reads
* DADA2 denoising
* Taxonomic classification
* Alpha diversity analysis
* Beta diversity analysis
* Relative abundance profiling

### 2. Transcriptomic Analysis

* Download TCGA-LUAD RNA-Seq data
* Data normalization
* Differential gene expression analysis
* Functional annotation

### 3. Immune Profiling

* Estimate immune cell infiltration
* Compare immune landscapes
* Classify tumors into immune phenotypes

### 4. Correlation Analysis

* Microbial abundance vs gene expression
* Correlation with immune infiltration scores

### 5. Network Analysis

* Construct regulatory networks
* Identify hub genes
* Infer microbiome-driven immune interactions
* Infer gene-driven immune interactions

### 6. Survival Analysis

* Evaluate prognostic significance
* Kaplan–Meier survival analysis
* Hazard ratio estimation

### 7. Machine Learning

* Feature selection - LASSO
* Random Forest classification
* Cox regression prediction
* Model evaluation

---

## Outputs

* Differentially expressed genes
* Microbial diversity metrics
* Immune infiltration scores
* Correlation matrices
* Regulatory networks
* Survival plots
* Machine learning performance metrics
* Candidate microbiome-Gene associated biomarkers


## Technologies Used

* Python
* R
* QIIME2
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Cos regression
* LASSO
* DESeq2
* Cytoscape


## Future Improvements

* Validation using independent LUAD cohorts.
* Multi-omics integration with mutation and methylation data.
* Deep learning models for biomarker prediction.
* Development of an interactive biomarker visualization dashboard.


## Author

**Rajeshwari N G**


## Acknowledgements

This project was completed as part of a bioinformatics research internship at NIT Calicut focused on integrating microbiome and transcriptomic data to investigate immune evasion mechanisms in lung adenocarcinoma. The work provided practical experience in multi-omics data integration, computational biology, and machine learning for cancer research.


## License

This project is intended for academic and research purposes.

