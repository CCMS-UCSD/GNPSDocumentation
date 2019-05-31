In this tutorial you will be guided into running the MSHUB deconvolution integrating GC Library Search workflow on GNPS.

## Pipeline

### To create and launch GNPS feature detection job:
1. Log in to GNPS (gnps.ucsd.edu)
2. Upload data to MassIVE (massive.ucsd.edu) or import an existing dataset. All of the data must be collected using the same GC protocol.
3. How to reach GC interface (MSHub) or clone the job
4. Select the files that need to be processed and click “Submit” (no explicit settings need to be entered as MSHub determines optimal settings internally without user input).
5. When the job has completed, the feature table and .mgf file for all detected features could be downloaded by clicking “[ all_features_table ]” and “[Download Quant Table]”.

### To create and launch GNPS library search job:

1. When feature detection job is completed, the link “launch library search” will become available. Clicking this link will launch library search job.
Alternatively, the .mgf file of all features downloaded from the feature detection workflow could be uploaded in the same way as the original data. The file can then be selected by clicking “Spectrum Files” under “Search Options” tab and selecting the uploaded .mgf file. Once files have been selected, the popup window can be closed by clicking on “Finish Selection”.
NOTE: The default parameters recommended for obtaining good results have been determined and prepopulated. However, users are encouraged to adjust the settings as appropriate for their analysis.
2. After the appropriate settings are entered, the job can be launched by clicking Submit”.

## Parameter Explanation
###  Advanced Network Options  
| Fillable Field  | Description | Recommended User Input |
| ------------- |-------------|-------------|
| Min pairs cos | Minimum cosine score required for an edge to be formed between nodes |0.85 value is set as default. This value has been determined to effectively delineate subclasses and Levels 6 and 7. |
| Node TopK | Pairs of nodes are reported only if they are found to be best matches in the topK in both directions that are above the minimum cosine score. | Default is set to 10. This value enables the network to be more or less stringent.|
| Maximum connected component size | Maximum number of nodes that can be connected in a single sub-network of a molecular network. This process iteratively breaks up large ‘hairball’ networks (of false positives) by removing the lowest scoring alignments (by cosine score) first until the resulting pieces fall below the maximum size. | Default setting is 100 – this value can be set to 0 to allow for an unlimited number of nodes or a higher setting can be used for larger data sets or for data sets containing many structurally-related molecules|
| Maximum shift between precursors | The maximum allowed difference in precursor m/z differences. | Must be set to a large value for EI data since no precursor information is available (default value of 500)|
### Advanced Search Options
| Fillable Field  | Description | Recommended User Input |
| ------------- |-------------|-------------|
| Library Class | The level of library to include hits from. | Keep default of “Bronze” to include all possible hits including to public libraries.|
| Top Hits Per Spectrum | How many top hits ranked by the cosine score to include into the results.| The default of 10. It is recommended to keep this number relatively high to allow for correct annotation selection if it is not a top hit.|
| Spectral Library | Selection of spectral libraries to include in the search. | Make sure to select all appropriate EI libraries by selecting them and clicking “Library Files”. Click “Finish Selection” when completed.|
| Search Analogs | Used for tandem MS data. | Keep default of “Don’t Search”. |
| Maximum Analog Search Mass Difference | Maximum shift of the precursor m/z for analog search. | Disabled when above option is set at “Don’t Search”. |
### Advanced Kovats Index Calculation Options
| Fillable Field  | Description | Recommended User Input |
| ------------- |-------------|-------------|
| Perform Kovats Calculation | Whether to perform calculation of Kovats retention index. | Select to calculate Kovats RIs for the compounds during library search. The Input Carbon Marker File could be provided for Kovats markers as comma separated values for each of the carbon markers and its corresponding retention time. The analysis must be conducted with identical protocol as the rest of the experiment. If the Input Carbon Marker File is not provided, the Kovat’s RIs will be estimated based on dataset-wide annotations. |
| Input Carbon Marker File (Optional) | If provided, this information will be used for RI estimation. | The RI markers information should be submitted as a comma separated values (.csv) file in the following format (header followed by names or available reference compounds and their retention times in seconds)|
| Cosine Threshold for Kovats Filter | The minimal value of cosine score for the library match to be used for Kovats RI values assignment. | Default value is set at 0.9 to limit inclusion of erroneous annotations that may introduce errors into calculation.|
| Retention time window starts/ends (mins) | The portion of chromatogram across the dataset to be used for selecting annotations for Kovats RI assignment. |  Select values according to specifics of experiment. The front end portion of chromatogram that contains dead volume elution, solvent delay, solvent peak or otherwise is unusable, as well as back end portion after all of the meaningful compounds have eluted (e.g. bakeout ramp) should be excluded. |
| Kovats Index Filtering Window (+/- %) |  The allowable error window for the calculated/assigned Kovats RI for the annotation to be retained.| Default of +/-10%. All of the annotations are shown when exploring results in the browser. The filtered results can be downloaded under “Download Filtered Computed Kovats Index Files” link upon job completion.|
### Advanced Filtering Option
| Fillable Field  | Description | Recommended User Input |
| ------------- |-------------|-------------|
| Filter below std dev| For use with tandem MS data.| It is highly recommend to use a default value of 0 so that no filter is applied.|
| Filter SNR Intensity | All ions in the EI spectrum below this raw intensity will be deleted. |Use a default value of 0 so that no filter is applied, especially if the raw intensities of your data are very low.|
|Filter precursor window|All peaks in a +/- 17 Da around precursor ion mass are deleted. This removes the residual precursor ion, which is frequently observed in tandem MS spectra in the comparison of all spectra for molecular networking.|Don’t Filter is set as default for the EI data.
|Filter library|Applies the above precursor ion window filter to the library as well.|Don’t Filter is set as default for the EI data.|
|Filter peaks in 50 Da window|Removes peaks that are not one of the top 6 most intense within a +/- 50 Da window.|Depending on the deconvolution results, this could be turned on or off: if fragmentation patterns contain a large number of small peaks, this filtering should be turned off, as it may filter out relevant peaks that could be signals.|

## Assessing the results of library search

Once the job has completed, the putative matches to all selected libraries could be viewed under one of the links: “View All Spectra DB”; “View All Compounds”; “View Kovats Calculation Result”.
The possible annotations could be sorted by their cosine value and/or RI error rate to aid in selecting best annotation using researcher’s judgement.
In addition, the results could be downloaded as a table for all of the matches (“Download Not Filtered Computed Kovats Index Files”) or matches filtered by the Kovats RI window set when launching the job (“Download Filtered Computed Kovats Index Files”).
If clicking on the “View Kovats Calculation Result” results in an error: “There was an error retrieving the result data for block "main" of workflow type "MOLECULAR-LIBRARYSEARCH-GC"”, this is indication that the dataset does not contain sufficient number of reference points for polynomial fitting to generate satisfactory regression (it does not pass internal quality check). In this case submitting the information for RI reference markers is necessary to generate Kovats estimates for the submitted data.
The results can be visualized as a network (see “Molecular Networking” and the “Biological Case Study” sections below) by downloading and importing the GraphML file “Download GraphML”. The detailed

### View All Spectra DB
This option will display all of the top matches for each feature and relevant information including retention time. The “Scan” field corresponds to the feature number in the .mgf file generated at the feature detection step and corresponds to the number listed in the feature table. Clicking on the spectrum icon at the left side of the screen would show mirror plot that could be investigated.

### View All Compounds
This option will display only the cop hits for each feature of the top match.

### “View Kovats Calculation Result”
This option will display all of the top matches for each feature and in addition will list the information for the Kovats RI calculation or assignment. This information includes:

### Kovats_Index_Lib_Record
This is the library value of Kovats RI for the match. In no record available, “None” is listed.
### Kovats_Index_calculated
This is the value of calculated or assigned value of the RI.

### Kovats_Index_Error
This is the error between the calculated/assigned RI value and the library entry. If no library value was available, “None” is listed.


## Capturing information by adding reference spectra from your data.

High confidence spectra from experimental data or pure standards could be added as a reference spectrum to GNPS for future reference.
Single spectrum submission
If the user wishes to upload >50 reference spectra to GNPS, a batch upload should be used to as detailed in the online help documentation. The compliance of the file format can be verified using online tool.

## Data Sharing and Cloning a Job
The analysis conducted on GNPS as well as the deposited raw data could be shared as a hyperlink to the GNPS job(s) and the MassIVE accession number, correspondingly. GNPS stores data inputs and setting used for the analyses of the data, so the analysis could be shared and reproduced.
If the same analysis needs to be repeated, it is possible to clone the job by clicking ‘clone’ on the job status page.  Cloning a job allows users to view all parameters and files that were used and rerun the job (feature detection or library search) with the same (or adjusted) parameters and files. Note that if data were imported from private user workspace and not from within MassIVE, other users will not have access to the data and consequently will not be able to rerun or reproduce the GNPS job.  

## Troubleshooting
| Erro Description  | solution | 
| ------------- |-------------|
| When clicking on “View Kovats Calculation Result”, error is displayed: “There was an error retrieving the result data for block "main" of workflow type "MOLECULAR-LIBRARYSEARCH-GC"”   | The retention indices could not be reliably estimated from the annotations available within the dataset. Increasing the number of files, for example, by co-analyzing multiple datasets obtained with the same experimental protocol could resolve the issue. Alternatively, the information for the reference mix needs to be supplied.  |
|A large number of spectra appear as a single peak.|Insufficient volume of data cause unstable deconvolution resulting in spurious low-quality spectra. Increasing the number of files, for example, by co-analyzing multiple datasets obtained with the same experimental protocol would resolve the issue. Otherwise, an external deconvolution could be carried out to ensure that the high quality spectral pattern are obtained.|
|GNPS job fails due to improper metadata format|The metadata file must be formatted as a tab-separated .txt file|
