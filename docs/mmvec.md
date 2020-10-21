MMVEC is a tool for multi-omics integration between metabolomics and microbiome data. 

Pardon our dust as this page is a work in progress...

## Input Formats

### Microbiome Metadata

This is a tsv file that describes the taxonomy of hte input sequences. The required header is: featureid. 

### Microbiome Quantification Data

This data can come from several locations:

1. Import into qiime2 manually (see below)
1. TODO

### Metabolomics Metadata

This is a tsv file that describes the identification of the metabolites. The required header is featureid or sampleid that provides the identifier for each metabolite. 

### Metabolomics Quantification Data

This data can come from several locations:

1. GNPS FBMN outputs a qza for this
1. Import into qiime2 manually (see below)

!!! note 
    Sample identifiers will need to match between the microbiome and metabolomics quantification files. One of the ways to do this if you run your metabolomics in GNPS' FBMN, you can specify a sample_name column in the metadata to rewrite the sample identifiers for the metabolomics qza to line up with the metabolomics. 

## Running the Workflow

Lorem Ipsum

## Exploring the Results

Lorem Ipsum

## Demonstration Data

Lorem Ipsum

## Page Contributors

{{ git_page_authors }}
