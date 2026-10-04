# Metagenomic diversity analysis of metagenome-derived viral sequences from a Neotropical river

The file "AnalysisViromaFinal.Rmd" contains the script to perform taxonomic annotation, filtering, and alpha/beta diversity 
analysis of metagenomic sequencing data obtained from water column and 
sediment samples collected along a pollution gradient in the Virilla River, 
Costa Rica. Sampling was performed during the dry and rainy seasons of the year 2022.

Main Steps:
 1. Installation and loading of required R packages.
 2. Taxonomic assignment using local SQLite database and `taxonomizr`.
 3. Construction of `phyloseq` objects from OTU table, taxonomic assignments, 
    and metadata.
 4. Rarefaction of samples to normalize sequencing depth.
 5. Prevalence- and abundance-based filtering of taxa and samples.
 6. Subsetting of samples by habitat (water vs. sediment) and season (dry vs. rainy).
 7. Alpha diversity analysis using Observed richness, Shannon, and Inverse Simpson indices.
 8. Visualization of alpha diversity across sites and sample types.
 9. Statistical testing using Kruskal-Wallis and Dunn’s post-hoc tests.
 10.Ordination analysis on CLR-transformed microbial community data to visualize patterns in sample composition using Principal Component Analysis (PCA). 
 11. COGs categories visual analysis.
