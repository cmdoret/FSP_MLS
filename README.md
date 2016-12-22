# Do enhancer-associated lincRNAs contribute to chromosomal organization ?
First-step project, Master in Molecular Life Sciences, Bioinformatics
Author: Cyril Matthey-Doret

Supervisor: Jennifer Yihong Tan

Director: Ana Claudia Marques

December 2016, University of Lausanne

## Folder

This folder contains the source code used to generate results in the project.

## Contents

* __subset_genes__: These scripts were used conjointly with bedtools calls for subsetting lincRNAs into categories based on promoter/enhancer overlap. Bedtools calls are not included, but subsetted gene lists are available in the data folder.
    + enhanc_assoc.R: Used to produce bedfiles containing promoter regions of genes. Used conjointly with bedtools intersect calls to categorize lincRNAs based on enhancer overlap, or promoter overlap.
    + all_combinations.R: Used conjointly with bedtools to produce categories of lincRNAs based on promoter AND enhancer overlap, as shown in the report.
* __TAD_processing__: Scripts used to filter TADs or splitting them into bins.
    + TAD2bins.R: Code used to split TADs into bins of equally sized length.
    + small_TADs.R: Code used to filter out large encompassing small_TADs.
* __HiC_processing__: Scripts used to normalize and perform operations on HiC matrices.
    + script_norm_HiC.R: Code used to normalize Hi-C data
    + int_TAD_TAD.R: Code used to compute mean interactions per TAD
    + twosteps_normhiC2boundaries.R: Code used to compute boundaries from normalized Hi-C matrices.
* __gene_characterization__: Scipts used to compute different features of lincRNAs and protein coding genes and store them into compact tables containing gene categories (promoter/enhancer overlaps).
    + expression.R: Used to generate a compact table of median expression values for all genes.
    + seq_conservation.R: Code used to generate a compact table of averaged phastCons scored through mammalian and primate evolution for all genes.
    + tissue_spec.R: Code used to compute tissue specificity and generate a compact table.
* __GAT__: contains files required to perform enrichment tests
    + GAT_run_template.sh: Custom template for testing enrichment of many different segment in an annotation. Segments, annotations and workspace can be changed according to the desired test. Parameters are all set to what has been used in the report.
    + enrichment_analysis.R: Script used for processing GAT output. Allows to take all output files in a folder into a table, provided the filenames are consistent.
* __report_figures.R__: Code used to generate figures in the report
* __data__: Data used in the manuscript, excluding contact matrices and normalization vectors. See respective README files for more details.
    + chip_seq: Chip-seq peaks of CTCF, RAD21 and SMC3 used for enrichment tests.
    + conservation: averaged phastCons scores for protein-coding genes, lincRNAs and ancestral repeats.
    + DNA_contacts: Processed data from Hi-C matrix. Does not contain the raw/normalized Hi-C matrices.
    + expression: Median expression levels of lincRNAs and protein-coding genes. In GM12878, HUVEC, NHEK and K562.
    + GAT: Workspaces, isochore file and output from GAT enrichment tests.
    + genes: Original lists of genes and list of elincRNAs and other LCL-expressed lincRNAs. Also contains list of predicted regulatory elements from ENCODE.
    + TADs: lists of TADs, TAD boundaries and loop anchors.
    + tissue_specificity: List of genes with associated Tau tissue specificity indexes.


