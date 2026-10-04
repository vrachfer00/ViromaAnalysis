# Metagenomic diversity analysis of metagenome-derived viral sequences from a Neotropical river

This repository contains the R code, processed abundance matrices, and metadata supporting the manuscript:
Seasonality has a stronger influence than pollution on metagenome-derived viral communities in a Neotropical river
Author: Rachelle Fernández-Vargas.
Journal / Status: Submitted for publication
Raw Sequencing Data: Submitted to NCBI SRA under BioProject Accession PRJNA1240286.


Overview:
This analysis pipeline performs taxonomic annotation, filtering, and alpha/beta diversity analysis of metagenomic viral sequencing data. Samples were collected from water column (free-living particles) and sediment (settled particles) matrices across three pollution gradient sites along the Virilla River (Costa Rica) during both dry and rainy seasons of the year 2022.


Repository Structure:

├── README.md               # Overview and execution instructions

├── LICENSE                 # Open-source license (MIT / CC-BY 4.0)

├── AnalysisViromaFinal.Rmd # Main R script containing the full pipeline

├── COG_Analysis.xlsx.      # Tables used for calculating functional profiles

├── viromes.csv             # OTU / viral abundance count matrix

├── mdata2.csv              # Sample metadata

└── taxaid.csv              # List of target NCBI Taxonomy IDs

System Requirements:
R version: 4.2.0 (or superior) and RStudio (recommended)

Main Steps:
1. Taxonomic Annotation: Queries NCBI Taxonomy IDs against accessionTaxa.sql using taxonomizr.
2. Phyloseq Construction: Merges OTU counts, taxonomy annotations, and sample metadata into a unified phyloseq object.
3. Data Preprocessing and Filtering.
4. Alpha Diversity Analysis: Calculates Observed Richness, Shannon, and Inverse Simpson indices across habitat types, seasons, and sites. Includes Kruskal-Wallis non-parametric tests and Dunn post-hoc comparisons.
5. Beta Diversity and Ordination: Aggregates relative abundances at Class and Order ranks and constructs Principal Component Analysis (PCA) plots on CLR-transformed data.

