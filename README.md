# MGP-manuscript-R-scripts
This repository contains the R scripts used for data analysis and figure generation in the manuscript

The repository includes two analysis workflows:

1. Human atrial single-nucleus RNA sequencing (snRNA-seq) analysis of MGP expression.
2. Bulk RNA-seq analysis of primary mouse atrial cardiac fibroblasts (ACFs) treated with recombinant MGP (rMGP).

The scripts have been streamlined to retain the analyses used to generate the relevant manuscript figures.

Files

human_AF_snRNA-seq.Rmd

Analysis of publicly available human atrial snRNA-seq data.

The script includes: Seurat object generation and quality-control filtering; SCTransform normalization; PCA and Harmony integration; UMAP dimensional reduction and cell-type annotation; MGP expression visualization using FeaturePlot; Comparison of MGP expression in atrial fibroblasts between control and atrial fibrillation (AF) samples

Human snRNA-seq samples

Five samples from the public human atrial snRNA-seq dataset were used for the analysis:

| Analysis label | Group |
| --- | --- |
| `ctrl_10` | Control |
| `ctrl_11` | Control |
| `ctrl_12` | Control |
| `AF_13` | Atrial fibrillation |
| `AF_14` | Atrial fibrillation |

The raw public snRNA-seq data are not included in this repository. Users should obtain the data from the original public data source (GSE224959).


rMGP_bulk_RNAseq.Rmd

DESeq2 and clusterProfiler analysis of bulk RNA-seq data from primary mouse ACFs.

Experimental groups: 

- Vehicle (`Veh`)
- TGFβ (`TGFb`)
- Recombinant MGP (`rMGP`)
- Recombinant MGP + TGFβ (`rMGPTGFb`)

The script includes: DESeq2 dataset construction and gene filtering; PCA and Differential gene expression analysis; Fibrosis-associated gene heatmap; DEG Volcano plots; Gene Ontology enrichment analysis

Differentially expressed genes are defined using: adjusted P value < 0.05 and |log2 fold change| > 1

The comparisons used in the manuscript are:

- `TGFb vs Veh`
- `rMGPTGFb vs TGFb`
- `rMGP vs Veh`

Users can access to raw  processed data from the original public data source (GSE342294).
