# PangenomeMatrix Pipeline
An automated **Snakemake** pipeline for comparative analysis of bacterial accessory pangenomes. [cite_start]Developed to replace manual workflows involving Geneious and Spreadsheet software [cite: 1, 4, 18][cite_start], this tool extracts ORFs, performs BLASTn alignments, calculates Welch's T-Test and Fold-Change[cite: 57, 64, 65, 70], and generates publication-ready PCA and Volcano Plots.

## 🚀 Features

- [cite_start]**Automated ORF Extraction:** Uses Prokka to annotate and extract CDS from a reference genome[cite: 6].
- [cite_start]**Database Construction:** Automatically concatenates and indexes target genomes[cite: 1, 14, 15].
- [cite_start]**Statistical Analysis:** Generates a binary presence/absence matrix based on >90% coverage and identity thresholds[cite: 21, 48, 49, 50].
- [cite_start]**Dynamic Visualization:** Automatically produces PCA and Volcano Plots using $log_{10}(p\text{-value})$ and $log_{2}(\text{Fold-Change})$[cite: 79, 80, 82, 83, 86].
- **GWAS Ready:** Outputs a formatted matrix compatible with Scoary.

## 🛠️ Installation

We recommend using `mamba` to recreate the isolated environment.

```bash
git clone [https://github.com/yanromb/PangenomeMatrix.git](https://github.com/yanromb/PangenomeMatrix.git)
cd PangenomeMatrix
mamba env create -f environment.yml
conda activate pangenoma
