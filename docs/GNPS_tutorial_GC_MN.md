

# GC-MS EI Data Analysis

## GC/MS Deconvolution Submission

**1)** Log in to GNPS  ([gnps.ucsd.edu](https://gnps.ucsd.edu/ProteoSAFe/static/gnps-splash.jsp)). If an account has to be created first, refer to GNPS documentation at the [quickstart](https://ccms-ucsd.github.io/GNPSDocumentation/quickstart/) banner. Before starting, files from GC-MS analysis must be converted from proprietary vendor formats to .mzML, or .CDF file formats. To convert, please see our [conversion guide](https://ccms-ucsd.github.io/GNPSDocumentation/fileconversion/). 

**2)** The GNPS home page includes two sections to launch GNPS GC/MS data analysis job, one for data processing - deconvolution and one for GC/MS library search/networking (**Fig. 1**) By clicking on “Process Raw GC-MS data” icon, a job page opens (**Fig. 2**). Start by entering the title of your job (1). Then, the “Select Files” section allows importing existing or previously uploaded dataset(s) from MassIVE. Select the files that need to be processed by clicking on “Select Input Files” (2). A pop-up window appears with three tabs: “Select Input Files”, “Upload Files”, and “Share Files”. To upload files to GNPS using the browser (limited to 20MB), you can use our web drag and drop uploader in the “Upload Files” banner. See the documentation [here](https://ccms-ucsd.github.io/GNPSDocumentation/fileupload/) for more information. Readers following the tutorial can go to the “Share Files” tab, enter the MassIVE accession number for the dataset (e.g. [MSV000084226](https://gnps.ucsd.edu/ProteoSAFe/result.jsp?task=671cd79ac3af4c4493e4025d62d161e1&view=advanced_view)) in the “Import Data Share” box (3), and click on “Import” (4). This specific dataset is now available directly in your GNPS user workspace at “Select Input Files” section (5). Select the input file, who appears highlighted in blue color, and click on “Spectrum files” (6). When the selected files are visible in the “Selected Spectrum Files” box, click on the “Finish Selection” button (7).

**NOTE:** All of the data used for the job must be collected using the same GC protocol (temperature program, column, injection mode). Multiple datasets could be combined as long as the data have been collected using the same protocol. When creating a dataset on MassIVE ([massive.ucsd.edu](https://massive.ucsd.edu/ProteoSAFe/static/massive.jsp)), include “GNPS” and “GC” in the name (As GNPS_GC_Name of the GNPS-MassIVE dataset). See the documentation about [Dataset Creation/Sharing](https://ccms-ucsd.github.io/GNPSDocumentation/datasets/) and an example of a MassIVE dataset [MSV000084226](https://gnps.ucsd.edu/ProteoSAFe/result.jsp?task=671cd79ac3af4c4493e4025d62d161e1&view=advanced_view) for more information. An insufficient volume of data causes unstable deconvolution resulting in spurious low-quality spectra. It is recommended for datasets smaller than ~10 files to use alternative deconvolution solutions such as MZMine2/ADAP, MS-Dial or XCMS. Increasing the number of files, for example, could be done by co-analyzing multiple datasets obtained with the same experimental protocol. 

**Fig. 1**

**![img](\img\GC-MS_documentation\fig_1.png)**

**Fig. 2**

![img](\img\GC-MS_documentation\fig_2.png)

**3)** The “Advanced MSHub Processing” section displays some automatic setting parameters (related to peak symmetry and baseline adjustment) determined internally by MSHub (**Fig. 3**). The user does not need to provide settings, although they can be set manually, should the user choose to do so. In the “Advanced Clustering” settings, be sure that cluster spectra are turned off (CLUSTER_SPECTRA = NO) (8). The TIME_UNIT must be set as minutes or seconds (8), depending on the chromatography time units of your data (typically the default time units are seconds in NetCDF files and minutes in .mzML files). Then, enter your email address at the bottom (9) and finish by clicking “Submit” (10).

**Fig. 3**

![img](\img\GC-MS_documentation\fig_3.png)

**4)** When the job has been completed, you will receive a notification email and the status “DONE” appears on your GNPS job. All submitted jobs appear under “jobs” link from the GNPS main menu (**Fig. 4**). By selecting the job of interest and clicking on the “Done” button, the “Job Status” window opens with different options (**Fig. 5**) to (i) explore deconvolution results with the “View All Deconvolved Spectra” option, (ii) download quantification results and feature table by clicking on “Download Spectra as MGF” and “Download Quant Table”, or (iii) continue the process with “Process Library Search” tool (11).

**NOTE:** The first line of the feature/quantification table (**Fig. 6**) indicates the retention time (in min.) with a balance score in parenthesis (in percentage). The “Rel. Max Integral” and “Sample\Best order” values relate to the relative proportion of each peak in the data and the ranking of the feature in terms of its size, correspondingly.

**Fig. 4**

![img](\img\GC-MS_documentation\fig_4.png)

**Fig. 5**

![img](\img\GC-MS_documentation\fig_5.png)

**Fig. 6**

![img](\img\GC-MS_documentation\fig_6.png)



## GC/MS Library Search Submission

**5)** To conduct a library search and create a molecular network, proceed to launch GNPS library search job by clicking “Search Spectral Library and Molecular Network” link from the “Job Status” window of the completed feature detection job (**Fig. 5**). A new job window appears (**Fig. 7**), with four fields of advanced search, filtering, network, and Kovats index calculation options. Click on the “Show Fields” button to show advanced options. The default parameters recommended for obtaining good results have been determined and pre-populated as described in **table 1**. However, users are encouraged to adjust the settings as appropriate for their analysis. The .mgf spectrum file and the quantification table are directly included in this new job. However, into the pop-up window appearing by clicking on “Select Input File” from the job window (1), library files, metadata table, and carbon marker files can be added as the same manner as described previously (**Fig. 8**, 4 and 5). Readers following the tutorial can use the following carbon marker table file “GC_Kovats_SKIN.csv” available in the example dataset [MSV000084226](https://gnps.ucsd.edu/ProteoSAFe/result.jsp?task=671cd79ac3af4c4493e4025d62d161e1&view=advanced_view). After the appropriate settings are entered, as well as the email address (2), the job can be launched by clicking on the “Submit” button (3). 

**NOTE:** The metadata and carbon marker files must be formatted as a tab-separated .txt file. To create your metadata table properly, see the documentation [here](https://ccms-ucsd.github.io/GNPSDocumentation/metadata/). The carbon marker table must have one “Compound_Name” column that includes the name and the number of carbon into parentheses, and another column named “RT_Query” with the retention time in seconds, as shown in the **Figure 9**. The libraries used in this example tutorial are protected by copyright. However, each users can add their own libraries on GNPS by following the instructions [here](https://bix-lab.ucsd.edu/display/Public/Add+Batch+Spectra+Documentation), or by uploading them in .mgf format (drag and drop on “Upload File” section) and add by clicking on “Library Files” on “Select Input Files” section (**Fig. 8**). The user still has the option to add his/her own .mgf spectrum file and the associated quantification table if the balance score is included.

**Fig. 7**

![img](\img\GC-MS_documentation\fig_7.png)

**Fig. 8**

**![img](\img\GC-MS_documentation\fig_8.png)**

**Fig. 9**

![img](\img\GC-MS_documentation\fig_9.png)

**Table 1.** Parameters for Library Search 

| ***Search Options***                                         |                                                              |                                                              |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **Fillable Field**                                           | **Definition**                                               | **Recommended User Input**                                   |
| Spectrum Files                                               | Selection of files needed to analyze.                        | The deconvoluted files usually are directly included into the Library search/Networking job. Allowed file formats are .mzML or .CDF. |
| FORCE_EXACT_MATCH                                            |                                                              | Keep default value of 1.                                     |
| Precursor Ion Mass Tolerance                                 | Maximum mass deviation between the observed precursor ion and the ions selected within the libraries included in the search. | The choice of the precursor mass tolerance setting usually is influenced directly by the accuracy of the mass analyzer being used to measure the precursor spectra in LC-MS analysis, but modification of this parameter are not meaningful for EI data because there is no precursor ion. 20000 is the default value to encompass all ions. |
| Min Matched Peaks                                            | Minimum number of common fragment ions that should share a spectra to be considered as a spectral library annotation. | Default value is 6, but note that this parameter should be tuned depending on the molecules of interest and experimental conditions. It is recommended to perform several jobs modifying this parameter for testing possible outcomes variations in annotations. Typically high quality features contain more than 15 ions in EI data. |
| Fragment Ion Mass Tolerance                                  | Maximum mass deviation between the observed fragments and the ions selected within the libraries included in the search. | The choice of the precursor mass tolerance setting is influenced directly by the accuracy of the mass analyzer being used to measure the precursor spectra. Default value is ± 0.025 Da for high-resolution mass spectrometers (q-TOF, q-Orbitrap). For low-resolution MS/MS instruments (e.g. , ion traps, triple-quadrupole/QqQ), a PIMT ion mass tolerance of ± 2.0 Da is recommended. Note that this parameters should be tuned depending on data. |
| Score Threshold                                              | Minimum cosine score to be considered as an annotation in spectral library search. | 0.85 value is set as default. This value has been determined to effectively delineate subclasses and Levels 6 and 7 and usually performs well with data obtained through experiments without derivatization, but that will depend on the quality of the mass spectra obtained. For derivatized compounds the cosine value for good matches is generally lower by ~0.1 due to an inferior quality of the EI spectra. |
| ***Advanced Search Options***                                |                                                              |                                                              |
| **Fillable Field**                                           | **Definition**                                               | **Recommended User Input**                                   |
| Library Class                                                | The level of library to include hits from.                   | Keep default of “Bronze” to include all possible hits from libraries. |
| Top Hits Per Spectrum                                        | How many top hits ranked by the cosine score to be included into the results. | The default of 1. It is recommended to keep this number relatively high (for example, 10 to include top 10 matches) to allow for correct annotation selection if it is not a top hit. |
| Spectral Library                                             | Selection of spectral libraries to include in the search.    | Select all appropriate EI libraries by selecting them and clicking “Library Files”. Click “Finish Selection” when completed. Any of the user’s own libraries could be included into the search as long as they are converted into .mgf format. If the libraries are curated and could be shared with the community, it is encouraged to upload them to GNPS as described [here](https://bix-lab.ucsd.edu/display/Public/Add+Batch+Spectra+Documentation). |
| Search Analogs                                               | Used for tandem MS data.                                     | Keep default of “Don’t Search”. This option is used for LC-MS data. |
| Maximum Analog Search Mass Difference                        | Used for tandem MS data.                                     | Disabled when above option is set at “Don’t Search”.         |
| ***Advanced Filtering Options***                             |                                                              |                                                              |
| **Fillable Field**                                           | **Definition**                                               | **Recommended User Input**                                   |
| Filter StdDev Intensity                                      | Used for tandem MS data.                                     | It is highly recommended to use a default value of 0 so that no filter is applied. |
| Filter precursor window                                      | Used for tandem MS data.                                     | “Don’t Filter” is set as default for the EI data because there is no precursor ion. |
| Filter peaks in 50 Da window                                 | Removes peaks that are not one of the top 6 most intense within a +/- 50 Da window. | Depending on the deconvolution results, this could be turned on or off: if fragmentation patterns contain a large number of small peaks, this filtering should be turned off, as it may filter out relevant peaks that could be signal. |
| Filter SNR Intensity                                         | All ions with a signal to noise ratio (SNR) in the EI spectrum below this value raw intensity will be deleted. | Use a default value of 0 so that no filter is applied, especially if the raw intensities of your data are very low. This value can be modified by the user for excluding background ions and just include the mass spectra of certain quality. |
| Filter library                                               | Used for tandem MS data.                                     | Don’t Filter is set as default for the EI data because there is no precursor ion. |
| Min Peak Int                                                 | All ions with a signal in the EI spectrum below this raw intensity will be deleted. | Use a default value of 0 so that no filter is applied, especially if the raw intensities of your data are very low. |
| ***Advanced Network Options***                               |                                                              |                                                              |
| **Fillable Field**                                           | **Definition**                                               | **Recommended User Input**                                   |
| Meta-table (Optional)                                        | Selection of metadata to include in the search.              | The metadata file describes the samples properties and allows more flexibility for data analysis and visualization. It is an alternative way to assign groups when selecting data input files within the workflow of GNPS, see an example [here](https://ccms-ucsd.github.io/GNPSDocumentation/metadata/). |
| Min pairs cos                                                | Minimum cosine score required for an edge to be formed between nodes. Lower value will increase the size of the clusters by inducing the clustering of less related spectra, higher value will limit do the opposite. | 0.7 value is set as default. This value has been determined to effectively delineate subclasses and Levels 6 and 7 and usually performs well with data obtained through experiments without derivatization, but that will depend on the quality of the mass spectra obtained. For derivatized compounds the cosine value for good matches is generally lower due to an inferior quality of the EI spectra. |
| Network TopK                                                 | Pairs of nodes are reported only if they are found to be best matches in the topK in both directions that are above the minimum cosine score. | Default is set to 10. This value enables the network to be more or less complex. |
| Quant-table (Optional)                                       | Table including feature ID, retention time (in min.) with balance score, Rel. Max Integral and Sample\Best order. | The quantification table (**Fig. 6**)  usually is directly included into the Library search/Networking job or can be imported externally. External deconvolution tools do not provide balance score and it will not be available in the search results. |
| Maximum shift between precursors                             | The maximum allowed difference in precursor m/z differences. | Must be set to the higher m/z expected in the analysis for EI data since no precursor information is available (default value of 500) |
| Maximum Connected Component Size                             | Maximum number of nodes that can be connected in a single sub-network of a molecular network. This process iteratively breaks up large ‘hairball’ networks (of false positives) by removing the lowest scoring alignments (by cosine score) first until the resulting pieces fall below the maximum size. | Default setting is 100 – this value can be set to 0 to allow for an unlimited number of nodes or a higher setting can be used for larger data sets or for data sets containing many structurally-related molecules. Low value encourages breaking up the “hairball” clusters but increases the chance that some nodes become disconnected and fall out of the network. |
| ***Advanced Kovats Index Calculation Options***              |                                                              |                                                              |
| Perform Kovats Calculation                                   | Whether to perform calculation of Kovats retention index.    | If the user need to calculate Kovats RIs for the compounds during library search this parameter should be selected. (i) The Input Carbon Marker File could be provided for Kovats markers (**Fig. 9**), but it must be conducted with identical protocol as the rest of the experiment. (ii) The Carbon Marker File is not provided, so the Kovat’s RIs will be estimated based on dataset-wide annotations and perform a polynomial fitting to generate satisfactory regression based in the annotations with higher Cosine and its Kovats RIs (experimental feature, may not be suitable for all datasets). |
| Input Carbon Marker File (Optional)                          | If provided, this information will be used for RI estimation. | The RI markers information should be submitted as a comma separated values (.csv) file in the following format (header followed by names or available reference compounds and their retention times in seconds). |
| Cosine Threshold for Kovats Filter (Can be left blank, experimental feature) | The minimal value of cosine score for the library match to be used for Kovats RI values assignment. | Default value is set at 0.9 to limit inclusion of erroneous annotations that may introduce errors into the calculation. This value can be lower (0.85) for experiments with derivatization because the variation between experimental and theoretical Kovats RIs usually is higher. |
| Kovats Retention Index Filtering Window (+/- %) (Can be left blank, experimental feature) | The allowable error window for the calculated/assigned Kovats RI for the annotation to be retained. | Default of +/-10%. This value can be higher according to the quality of the mass spectra or for experiments with derivatization because the variation between experimental and theoretical Kovats RIs usually is higher. Have in mind that all of the annotations will be shown when exploring results in the browser after completing the job. |
| Retention time window starts/ends (mins) (Can be left blank, experimental feature) | The portion of chromatogram across the dataset to be used for selecting annotations for Kovats RI assignment. | Select values according to the specifics of experiment. The front end portion of chromatogram that contains dead volume elution, solvent delay, solvent peak or otherwise is unusable, as well as back end portion after all of the meaningful compounds have eluted (e.g. bakeout ramp, column bleeding) should be excluded. |

**6)** After the job has been completed, the job status page gives access to three different views and also links to export/download network files (**Fig. 10**) with the “Download GraphML” button (1). The link (i) “View All Spectra DB” opens the interface that allows visualization of spectral matches to the reference database from selected libraries. It will display all of the top matches for each feature to different libraries and relevant information including retention time. The displayed columns could be edited by clicking “Select columns” link in the upper left corner (2). The possible annotations could be sorted by their cosine value to aid in selecting the best annotation using the researcher's judgment. The “Scan” field corresponds to the feature number in the mgf file generated at the feature detection step and corresponds to the “No” field listed in the feature table. Clicking on the spectrum icon (3) at the left side of the screen will show a mirror plot comparison between the query spectrum and the reference spectrum. This allows assessing the quality of matches between the deconvolution and the reference spectra. The button at the top of the page “Back to status page” (4) allows to go back. Clicking the (ii) “View All Compounds” option accesses the list of top hits (Compound_Name) with the corresponding cosine and the balance score for all annotated spectra. The link (iii) “View Kovats Calculation Result” shows Kovats calculation results for each spectrum if selected when launching the job. 

**NOTE:** The Kovats estimation feature is experimental. When clicking on “View Kovats Calculation Result”, if the following error is displayed: “There was an error retrieving the result data for block ‘main’ of workflow type ‘MOLECULAR-LIBRARYSEARCH-GC’”, this is an indication that the dataset does not contain a sufficient number of reference points for polynomial fitting to generate satisfactory regression (it does not pass internal quality check), because the information for RI reference markers is necessary to generate Kovats estimates for the submitted data. You just need to increase the number of files.

**Fig. 10**

![img](\img\GC-MS_documentation\fig_10.png)

**7)** To visualize molecular networks generated, the user has to download the input network files from “Download GraphML” link, save the folder, and unzip it (**Fig. 10**). The network can be visualized in an external software such as Cytoscape1, an open source software platform used to visualize, analyze, and annotate molecular networks from GNPS. Cytoscape is available for download from[ here](http://www.cytoscape.org/). This software allowed to encode any property of the network (i.e. node shape or color, edge thickness) with a metadata category (i.e. cohort, cosine score, compound family). An online tutorial, created with Cytoscape 3.7, used for molecular networking generated with LC-MS/MS data, can be accessed [here](https://ccms-ucsd.github.io/GNPSDocumentation/featurebasedmolecularnetworking-cytoscape/). Many of these steps could be reproduced in the same way for molecular networking from GC-MS data. 

1. Shannon, P., et al. (2003). Cytoscape: a software environment for integrated models of biomolecular interaction networks. *Genome Res, 13*(11), 2498-2504. doi:10.1101/gr.1239303



## Share Data, Clone Job, and Add Reference Spectra

**cloning a job:** If the same analysis needs to be repeated, it is possible to clone the job by clicking “clone” on the job status page. Cloning a job allows users to view all parameters and files that were used and rerun the job with the same, or adjusted parameters and files. Note that if data were imported from private user workspace and not from within MassIVE, other users will not have access to the data and consequently will not be able to rerun or reproduce the GNPS job.  

**sharing data:** The analysis conducted on GNPS as well as the deposited raw data could be shared as a hyperlink to the GNPS job(s) and the MassIVE accession number, correspondingly. GNPS stores data inputs and setting used for the analyses of the data, so the analysis could be shared and reproduced. 

**adding standards:** High confidence spectra from experimental data or pure standards could be added as a reference spectrum to GNPS for future reference. If the user wishes to upload >50 reference spectra to GNPS, a batch upload should be used to as detailed in the online help. The compliance of the file format can be verified using an online .



# Visualization

## Network Visualization in Cytoscape

Here we show an example of molecular networks in **Figure 11A**, visualizing in Cytoscape, generated from a study of volatiles related to aging of IPA beer (GNPS link: https://gnps.ucsd.edu/ProteoSAFe/status.jsp?task=1b300f711b404a3a8a9325352974adcd). In Cytoscape, the different aging times (0, 1, 2, 3, 4, 5, 6, 8, 12, and 20 days) are represented by different colors, and the metabolites present in the beer (each nodes) can be mapped on the molecular networks. The size of each node represents the total abundance of the feature and the colors in the pie chart shows the proportions of the compound at different aging duration times (gradient from green to yellow to red). As an example, a zoom in a cluster of terpenes annotated with compounds name, is shown in **Figure 11B**. Networking can facilitate the interpretation of data by visualizing chemical changes. In this example, the annotated compounds E-nerolidol and alpha-limonene-diepoxide, framed in pink, appear to be present only in fresh beer (0 days) and disappear as the beer ages. Other information can be mapped onto the network, for example in **Figure** **11C**, the same zoom with cosine values between nodes is shown instead of compound name annotations.

**Fig. 11**

**![img](\img\GC-MS_documentation\fig_11.png)**



## Molecular mapping in ili

Spatial distribution of different chemical features could be visualized in 2D or 3D using ili, a visualization app for 3D molecular cartography.2 ‘ili could be used either on the [website](http://ili.embl.de/) or as a [Chrome extension](https://goo.gl/3KAA8U). For mapping, two files need to be uploaded (DRAG AND DROP): an image for 2D (PNG or JPG format) or model for 3D (STL format), and a .cvs file with the coordinates of the spots on the model  that correspond to the sampled locations. Examples of mapping applications are available on ‘ili [website](https://ili.embl.de/). Here it is demonstrated how to map the volatilome data on the same model as shown in the “Human skin metabolome” example (**Fig. 12**). 

To create the .csv table, download the quantification table from GNPS deconvolution (example GNPS job: https://gnps.ucsd.edu/ProteoSAFe/status.jsp?task=9127bd48c09b4087ab0fd9a1407b3da1) output and add four columns with the x, y, z and radius coordinates from the different sampling points as described2.  For ease of navigation, the rows with feature descriptors could be deleted (the example shown on  **Figure 13** shows the retention time and the balance score as feature identifiers). The detailed instructions on creating the correctly formatted table with coordinates are given [here](https://github.com/alexandrovteam/Optimus/blob/master/Obtaining coordinates of sampling spots.md). 

To create chemical maps, drag and drop the example [volatilome table](https://github.com/aaksenov1/Human-volatilome-3D-mapping-) human 3D model. Different parameters can be set such as the spots, the mapping color, or the angles of visualization (**Fig. 14**). To display different features, click on the feature identifier value listed above the color scale on the bottom right corner of the screen and select feature to display. To annotate molecular features of interest, refer to the GNPS library search job for the matching features.

**Fig.12**

![img](\img\GC-MS_documentation\fig_12.png)

**Fig. 13**

**![img](\img\GC-MS_documentation\fig_13.png)**

**Fig. 14**

![img](\img\GC-MS_documentation\fig_14.png)

1. Protsyuk, I., et al. (2018). 3D molecular cartography using LC–MS facilitated by Optimus and'ili software. *Nature protocols*, *13*(1), 134.https://doi.org/10.1038/nprot.2017.122



