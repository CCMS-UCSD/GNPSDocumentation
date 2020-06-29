# Welcome to GNPS's Living Data

## About the Living Data

Living data is a continuous identification effort that aims to crowd annotated datasets from the MassIVE database.

## MassIVE Link to Living Data

[This link contains all the living data analyses](https://massive.ucsd.edu/ProteoSAFe/dataset.jsp?task=25cc4f9135c6428aabe1f41a9e54c369), including molecular networks, clustering, and library identifications that are up to date. 

## Organization of the FTP Repository

They are organized respectively in 4 folders: 

1. **CLUSTERSUMMARY** - Represents the clusters for each dataset and the associated metadata (e.g. mz, rt, and number of MS2 spectra)
2. **CLUSTERINFO** - Represents the clustering enabling tracing back from the clusters to the original files and scans they came from MGF - Clustered MS/MS spectra represented as an MGF file - scan numbers correspond to cluster index in 
3. **CLUSTERSUMMARY PAIRS** - Molecular Networking alignment pairs representing spectral similarity
4. **IDENTIFICATIONS** - Spectral library identifications reported by living data/continuous id to the latest GNPS spectral libraries (scan numbers also correspond to cluster index) [doi:10.25345/C5WQ0T](https://creativecommons.org/publicdomain/zero/1.0/) [dataset license: CC0 1.0 Universal (CC0 1.0)](https://creativecommons.org/publicdomain/zero/1.0/) 
