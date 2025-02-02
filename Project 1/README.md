## Project 1 : Regenerative Organizing Cell in the Frog tail

[Project Report](https://github.com/optimizedLP/STAT_5243/blob/main/Project%201/report/STAT5243_Project_1.pdf)
### Overview
This repository contains the analysis and findings from Project 1 of STAT5243, which investigates the Regenerative Organizing Cell (ROC) in Xenopus laevis tadpole tails through single-cell RNA sequencing (scRNA-seq) data. The study identifies distinct cell populations and highlights key genes associated with tissue regeneration.


### Abstract
We utilized clustering methods such as PCA + Louvain and PCA + Leiden to analyze scRNA-seq data. Our results identified the ROC, a crucial cell type responsible for the regenerative capacity in tadpoles, alongside specific genes linked to regenerative pathways.
Methodology


### Data Preprocessing:
Raw scRNA-seq data was log-normalized and filtered for highly variable genes (HVGs).
The top 2,000 HVGs were selected for further analysis.

### Clustering Analysis:
PCA was performed for dimensionality reduction.
Clustering was executed using PCA + Louvain and PCA + Leiden methods, with metrics like Adjusted Rand Index (ARI) used for quality assessment.

### Marker Gene Identification:
Logistic regression-based marker selection was applied to distinguish ROC from other cell types.

### Visualization:
UMAP visualizations were created to illustrate cell clusters and gene expression patterns.

### Results
Plots and figures demonstrate the clustering of cells and highlight significant gene expression differences across identified clusters.
Key genes, such as mmp3.1, vcan.1, and krb8.S, were identified as pivotal in distinguishing the ROC from other cell types.

##### Figure 1: PCA Analysis
![PCA Analysis](https://github.com/optimizedLP/STAT_5243/blob/main/Project%201/plots//pca-analysis.png)

##### Figure 2: Clustering Results
![Clustering Results](https://github.com/optimizedLP/STAT_5243/blob/main/Project%201/plots/leiden-clustering.png)

##### Figure 3: Marker Gene Expression
![Marker Gene Expression](https://github.com/optimizedLP/STAT_5243/blob/main/Project%201/plots/marker-gene-selection.png)


### Conclusion
The analysis successfully pinpointed gene markers specific to the ROC, providing insights into their role in regeneration. Future work includes further validation of marker genes and performing Gene Ontology (GO) analysis for deeper biological context.
