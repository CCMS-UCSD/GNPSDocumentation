# Qemistree
##### Canonically pronounced *chemis-tree*.
##### A tool which expresses the hierarchical “tree-like” relationships among molecules for chemically-informed analysis of metabolomes

Qemistree organizes the thousands of metabolites detected from untargeted metabolomics studies into a phenetic tree based on chemical substructures predicted from fragmentation spectra analysis with [SIRIUS and CSIFingerID](https://www.ncbi.nlm.nih.gov/pubmed/26392543). Qemistree enables the application of a series of phylogeny-based tools to study the chemical diversity of samples. Additionally, by placing mass spectra of unknown metabolites in their chemical context and integration of in silico annotation tools, Qemistree further facilitates the annotation of unknown metabolites in untargeted LC-MS/MS data.

## Inputs

The current workflow takes the following files as inputs:

1. Sirius export (MGF file) [MZmine2](http://mzmine.github.io)[required]
2. Quantification table from feature-based molecular networking (`qiime2_output/qiime2_table.qza`) [required]
3. Metadata from feature-based molecular networking (`qiime2_output/qiime2_metadata.tsv`) [optional, useful for visualizing emperor plots]
4. Library identifications from feature-based molecular networking (`DB_result/filename.tsv`) [optional, recommended for improved annotation]

**Note:** Please make sure that the inputs to feature-based molecular networking i.e. GNPS export (MGF file) and quant table (CSV file) from [MZmine2](http://mzmine.github.io) correspond to the Sirius export used above i.e. each row ID corresponds to the same MS1 feature across all the files.

