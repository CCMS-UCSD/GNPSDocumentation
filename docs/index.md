![logo](img/GNPS_logo_original.png)

# Welcome to GNPS Documentation

Global Natural Products Social Molecular Networking (GNPS, [https://gnps.ucsd.edu/](https://gnps.ucsd.edu/)) is a web-based mass spectrometry ecosystem that aims to be an open-access knowledge base for community-wide organization and sharing of raw, processed or identified tandem mass (MS/MS) spectrometry data. GNPS aids in identification and discovery throughout the entire life cycle of data; from initial data acquisition/analysis to post publication.

As there are many aspects to GNPS, it can be a bit overwhelming. Here is a quick description of main functionalities:

### Analyze and Annotate

* Perform [**molecular networking** and **spectral library search**](gnpsanalysisoverview.md) of LC-MS/MS data utilizing computational tools (See [Molecular Networking](networking.md), [Spectral Library Search](librarysearch.md), etc).
* [**Annotate/curate identified MS/MS spectra**](spectrumcuration.md) in open-access GNPS reference spectral libraries.
* Annotate peptidic natural products in LC-MS/MS data with [**DEREPLICATOR**/VarQuest/DEREPLICATOR+](dereplicator.md) and [RiPPQuest](https://gnps.ucsd.edu/ProteoSAFe/static/gnps-theoretical.jsp). <!--[MetaMiner](metaminer.md) , [CycloNovo](cyclonovo.md)-->
* Propagate in silico annotations in your LC-MS/MS data with [**Network Annotation Propagation** (NAP)](nap.md).
* **NEW!** Perform advanced molecular networking and spectral library search with [**Feature-Based Molecular Networking**](featurebasedmolecularnetworking.md). See [https://doi.org/10.1101/812404](https://doi.org/10.1101/812404).
* **NEW!** Analyze [**GC-MS data**](gcanalysis.md) with GNPS (See [GC-MS deconvolution](gc-ms-deconvolution.md), and [GC-MS library search/molecular networks](gc-ms-library-molecular-network.md)).
* **NEW!** Annotate your LC-MS/MS data with [**MolNetEnhancer**](molnetenhancer.md). See [https://doi.org/10.1101/654459](https://doi.org/10.1101/654459).
* **NEW!** Search spectral Mass2Motifs in your LC-MS/MS data [with **MS2LDA**](ms2lda.md).
* **NEW!** Give LC-MS/MS spectra biological/environmental context by searching against all public LC-MS/MS datasets ([**MASST Search**](masst.md)). See [https://doi.org/10.1101/591016](https://doi.org/10.1101/591016).
* **NEW!** Find and co- or re-analyze public LC-MS/MS data via systematic sample information at [**ReDU**](ReDU.md). See [https://doi.org/10.1101/750471](https://doi.org/10.1101/750471).

### Share and Explore

* Publish entire study datasets with the Mass Spectrometry Interactive Virtual Environment (MassIVE) data repository ([Dataset Submission](datasets.md)).
* [Browse](datasets#browsing-datasets) and [Reanalyze](datasets#reanalyze-datasets) over 1500 public datasets at GNPS
* Automatic reanalysis of public datasets with automated reports of new identifications ([Continuous Identification](continuousid.md)).
* Explore identifications of public datasets across entire repository ([Molecule Explorer](moleculeexplorer.md)).

For more detailed information, read on in the documentation, checkout the [GNPS publication](https://www.nature.com/articles/nbt.3597), and view some tutorial [videos](https://www.youtube.com/channel/UCufTdDIUPjfoN604Igv_29g/videos).

<!-- ## What is GNPS good for?

There are so many aspects to GNPS as it serves a diverse community. Here we wanted to highlight a few ways we think GNPS has been useful. We also highlight some of the creative ways the community has used GNPS's tools.

### Compound Identification (Dereplication)

Identify MS/MS spectra in your data to state of the art community MS/MS spectral libraries.

### Novel Analog Identification

We use GNPS's molecular networking to identify a novel analog of Stenothricin.

### Relative Quantification Across Samples

### Global Chemistry Visualization

When did we visualize stuff?

### Determine Biological/Chemical Context of Unknown Molecules



### Dataset Deposition for Publication

Today, the scientific community is clamouring for reproducibility of results that has resulted in cries for data transparency. Publications that lack public data are viewed with skepticism and rightfully so. GNPS is a place to deposit your data to in order to facilitate the review process as well as provide the community a resource to advance reproducible and rigorous science.

### Reference MS/MS Spectrum Publication for Re-identification

Put your MS/MS spectrum of a known compound in GNPS spectral libraries, so you never have to manually re-identify a compound in your own samples ever again. -->

### Contribute to GNPS

The GNPS community is always welcoming suggestions and contributions. Be part of the community and contribute ! See [that page for more informations](gnps_community.md).

### Citation

!!! cite "Recommended Citation"
	[Mingxun Wang, Jeremy J. Carver, Vanessa V. Phelan, Laura M. Sanchez, Neha Garg, Yao Peng, Don Duy Nguyen et al. "Sharing and community curation of mass spectrometry data with Global Natural Products Social Molecular Networking." Nature biotechnology 34, no. 8 (2016): 828. PMID: 27504778](https://www.nature.com/articles/nbt.3597)

### GNPS and MassIVE uptime

This is a brief overview of whether our web services are up: [here](https://stats.uptimerobot.com/Am4PLUWn3). 

And a more detailed functional test [status page](https://github.com/CCMS-UCSD/GNPS_Workflows#gnps-core-webserver-status).

### GNPS Documentation Site Authors

We would like to thank the following contributors to the documentation. 

However, we want to acknowledge that we have moved documentation in 2018 to GitHub from our previous wiki and those contributions are not reflected in these numbers
and were broadly subsumed into Ming Wang's contributions. These first additions to the documentation were invaluable and a few of those pioneers were 
Vanessa Phelan, Laura Sanchez, Laura Pace, Alexey Gurevich, and Don D. Nguyen. 

{{ git_site_authors }}
