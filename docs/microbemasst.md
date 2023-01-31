# microbeMASST

[MicrobeMASST](https://masst.gnps2.org/microbemasst/) is a domain-specific MASST that allows users to search for one or multiple MS/MS spectra against a reference database of MS/MS data acquired from bacterial and fungal monocultures that have been deposited and made publicly available on GNPS-Massive (current version is updated to July 2022).

Users are allowed to search for both known and unknown MS/MS spectra. 

## INPUT

If the known spectrum is already deposited in GNPS, users can enter a known library spectrum associated with a specific molecule from the GNPS libraries (Figure 1). A full list of the molecules and >500K library spectra associated with them present in the GNPS libraries can be found at this [link](https://gnps-library.ucsd.edu/). 

**Figure 1**

![img](img/microbeMASST/usi.png)

Otherwise, users can search for MS/MS spectra using Universal Spectrum Identifiers (USI). An example is through the use of the [GNPS Dashboard](https://gnps-lcms.ucsd.edu/). Users can inspect their data directly in the Dashboard. Using the example already provided in the Dashboard (mzspec:MSV000084494:GNPS00002_A3_p), we can inspect a MS2 scan (54) and click on “View Metabolomics USI” (Figure 2A). A new prompt will open that allows to inspect the spectrum (Figure 2B). Under Spectrum USI is possible to retrieve the USI of the spectrum that can be then copied and pasted into microbeMASST for the search (Figure 2C).

**Figure 2A**

![img](img/microbeMASST/gnps_dashboard1.png)

**Figure 2B**

![img](img/microbeMASST/gnps_dashboard2.png)

**Figure 2C**

![img](img/microbeMASST/gnps_dashboard3.png)

Finally, users can search for MS/MS spectra by manually providing a list of ions and their intensities (Figure 3). In this case, the m/z of the precursor ion of interest has to be specified while the charge is not required.

**Figure 3**

![img](img/microbeMASST/spectrum.png)

## SEARCH

Default search parameters are already provided (Figure 4). These include a 0.05 Da tolerance for both the parent mass (precursor m/z) and the fragment ions. A cosine threshold of minimum 0.7 and at least 3 matching peaks. These parameters can be modified by the users. Users can also decide to include analogs in their search (default is analog search OFF) by providing delta mass boundaries. 

Users will have to click on “Search microbeMASST by USI” if they have provided a USI for the search or “Search microbeMASST by Spectrum Peaks” if they have provided a list of fragment ions and their intensities for the search. The search job setting can be shared with other users by clicking on “Copy Link”, making each job reproducible. Finally, by clicking on “Open External MASST Search Results” a new [fastMASST webpage](https://fasst.gnps2.org/) that will search for the spectrum of interest against the whole GNPS repository and report all the samples in which that specific spectrum was found.

**Figure 4**

![img](img/microbeMASST/search.png)

## OUTPUT

The primary output of the microbeMASST search consists of an interactive taxonomic tree (Figure 5).  All the bacterial or fungal samples in which the spectrum of interest was found are categorized according to their taxonomy. By default, the tree is showing information up to Species level. This can be modified by changing the “Show level” parameter. Taxonomic ranks from Phylum to Species can be represented. The “Minimum matches” parameter indicates how many matches have to be found for a specific node in order to be visualized. We advise to keep this to 1 since microbeMASST is intended to be a discovery tool. The full tree information can also be visualized by changing the “Tree” setting from Matched to Full.

**Figure 5**

![img](img/microbeMASST/microbemasst.png)

By moving the cursor on each node, the contained information can be visualized (Figure 6). This includes not only the name of the taxon, but also its NCBI ID, its taxonomic rank, and the number of samples of this specific taxon that presented the specific MS/MS spectrum of interest, together with the total number of available in the reference database for the specific taxon. This information allows to calculate an occurrence ratio, which is also visualized in the form of the pie chart.

**Figure 6**

![img](img/microbeMASST/node.png)

By clicking the “Library matches” tab, a list of matching metabolites present in the GNPS libraries can be visualized (Figure 7). In this example case, we used the MS/MS spectrum of phenylalanine – cholic acid (Phe-CA) and we obtained an almost to perfect match to the Phe-CA deposited in the GNPS libraries. Interactive links allow to further investigate the molecule. The annotation process utilizes the also the GNPS Suspect Library to maximize the annotation chance when unknown molecules are investigated. If matches to actual metabolites are found, we advise to use that information rather than the predictions of the Suspect library. This table can be copied or exported in excel.

**Figure 7**

![img](img/microbeMASST/library.png)

By clicking on the “Dataset matches”, a list of matching samples present in the reference database of microbeMASST to the MS/MS spectrum of interest can be found (Figure 8). Here, not only the name, NCBI ID, and taxonomic rank of the taxon can be found but also the number of matching fragments that the sample spectrum and the spectrum of interest have. Files can be directly open in the GNPS Dashboard (Open file) for further investigation. When the MS/MS spectrum of interest has been searched through USI of deposited samples in GNPS-Massive, a mirror plot between the matching spectra can be visualized following the link in the USI column.

**Figure 8**

![img](img/microbeMASST/dataset.png)

Finally, the “Taxa matches” tab returns a list of all the matching taxa at every different taxonomic level (Figure 9). In this example (Phe-CA), has been found in 18 samples of the 44836 bacterial sample deposited in microbeMASST, with an occurrence ratio of 0.0004. Nevertheless, when looking at sample obtained from Bifidobacterium adolescentis cultures, 4 out of the 15 deposited samples presented Phe-CA, with an occurrence ratio of 0.2667

**Figure 9**

![img](img/microbeMASST/taxon.png)


## Page Contributors

{{ git_page_authors }}
