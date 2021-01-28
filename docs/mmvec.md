**mmvec** is a tool for multi-omics integration between metabolomics and microbiome data. 

See the article:
[Morton, J.T., Aksenov, A.A., Nothias, L.F. et al. Learning representations of microbe–metabolite interactions. Nat Methods 16, 1306–1314 (2019)](https://doi.org/10.1038/s41592-019-0616-3)

And the repository at [https://github.com/biocore/mmvec](https://github.com/biocore/mmvec).

Note that the present GNPS workflow allows to access only some functionalities of mmvec. So we recommend running mmvec as recommended in the github repository.

## Input Formats

### Microbiome Metadata

This is a tsv file that describes the taxonomy of hte input sequences. The required header is: FeatureID. 

### Microbiome Quantification Data

This data can come from several locations:

1. Import into qiime2 manually (see below)
1. TODO

### Metabolomics Metadata

This is a tsv file that describes the identification of the metabolites. The required header is featureid or sampleid that provides the identifier for each metabolite. 

### Metabolomics Quantification Data

This data can come from several locations:

1. GNPS [FBMN](featurebasedmolecularnetworking.md) outputs a qza for this
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
