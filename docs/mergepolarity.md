Here we merge polarity between positive and negative networks. 

Pardon our dust as this is a work in progress.

## Workflow
The workflow is available on GNPS: https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22MERGE_NETWORKS_POLARITY%22%7D. 

## Input
A GNPS job is run on postitive mode data and another job is run on negative mode data; the input is then the GNPS ID of both jobs. 

## Interpreting Results
A merged graphml file is created along with summary statistics and evaluations. To provide an assessment of accuracy of the edges inserted, new edges where both nodes in the respective positive and negative networks are identified with structure, a tanimoto score is calculated between the structures. We assume a tanimoto score of greater than 0.9 indicates concordance of structure. 

## Citation
Source code is available on Github: https://github.com/mwang87/MergePolarity
