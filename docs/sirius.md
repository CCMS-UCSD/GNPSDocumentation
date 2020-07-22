# SIRIUS

## Introduction

SIRIUS is an tool for the computational annotation of fragmentation spectra tool developed by the [Böcker Lab at Jena University](https://bio.informatik.uni-jena.de/software/sirius/).

## GNPS Workflow

#### Workflow description
We are working on deploying SIRIUS on GNPS to enable users to perform automated high throughput computational annotation. Various annotations using the SIRIUS modules:

1. Molecular formula prediction with *SIRIUS* and *ZODIAC*.
2. Structure assignment with *CSI:FingerID* and *COSMIC*.
3. Compound class prediction with *CANOPUS*.

Checkout the beta workflow [here](https://proteomics2.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22SIRIUS%22%7D).

For more information on SIRIUS, [please refer to the official SIRIUS documentation](https://bio.informatik.uni-jena.de/software/sirius/).

### With the Feature-Based Molecular Networking

The MGF file from the [Feature-Based Molecular Networking workflow](featurebasedmolecularnetworking.md) can be used as input for the SIRIUS workflow. The results can then be mapped on the molecular networks. When using MZmine, for best results, uses the SIRIUSExport module from the same aligned peaklist.

### With the SIRIUS mzML parser [Experimental]

SIRIUS has now a built-in mzML parser. The SIRIUS workflow on GNPS allows the selection of one mzML file. This is an experimental features under development.

## Results

### Viewing the results
> **View Molecular Formula Summary**: view molecular formula annotations results from *SIRIUS* and *ZODIAC*.

> **View Compound Summary**:  view structure assignment with *CSI:FingerID* and *COSMIC*.

> **View CANOPUS results**: view compound class prediction with *CANOPUS*.

### Mapping the results onto the molecular networks

If you used the [Feature-Based Molecular Networking workflow](featurebasedmolecularnetworking.md), you can map SIRIUS annotation onto the molecular networks in Cytoscape.

- Clic on the "download" button to download the results. 
- Import the results onto your network. More informations should be added here

## Citations

The GNPS workflow is brought to you Ming Wang and Louis Felix Nothias. If you found this workflow useful for your data analysis, please cite the relevant literature from below.

### Main citations

1. **SIRIUS**: [K. Dührkop, et al., SIRIUS 4: a rapid tool for turning tandem mass spectra into metabolite structure information. Nat. Methods 16, 299–302 (2019).](https://www.nature.com/articles/s41592-019-0344-8)
2. **ZODIAC**: [M. Ludwig, et al., ZODIAC: database-independent molecular formula annotation using Gibbs sampling reveals unknown small molecules. bioRxiv (2019).]()
3. 	**CSI:FingerID** [K. Dührkop, H. Shen, M. Meusel, J. Rousu, S. Böcker, Searching molecular structure databases with tandem mass spectra using CSI:FingerID. Proc. Natl. Acad. Sci. U. S. A. 112, 12580–12585 (2015).](https://www.pnas.org/content/112/41/12580)
4. 	**CANOPUS** [K. Dührkop, et al., Classes for the masses: Systematic classification of unknowns using fragmentation spectra. bioRxiv, 2020.04.17.046672 (2020).](https://www.biorxiv.org/content/10.1101/2020.04.17.046672v1)

### Additional citations
1. [S. Böcker, M. C. Letzel, Z. Lipták, A. Pervukhin, SIRIUS: decomposing isotope patterns for metabolite identification. Bioinformatics 25, 218–224 (2009).]()
2. 	[S. Böcker, K. Dührkop, Fragmentation trees reloaded. J. Cheminform. 8, 5 (2016).]()


## Page Contributors

{{ git_page_authors }}