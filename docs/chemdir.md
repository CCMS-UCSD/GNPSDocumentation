


## Chemical Directionality (ChemDir)

The Chemical Directionality (ChemDir) concept applied here is defined by relative abundance changes between two neighbouring nodes within a molecular network. By taking advantage of the [feature-based molecular network workflow (FBMN)](https://www.biorxiv.org/content/10.1101/812404v1.full), we used the raw peak area across the longitudinal (or spatial) data series as a measure of the abundance for each detected feature among events. ChemDir facilitates the prioritisation of putative transformations in tandem mass spectrometry (MS/MS) data using the Global Natural Products Social Molecular Network [(GNPS)](https://gnps.ucsd.edu/ProteoSAFe/static/gnps-splash.jsp) environment.

!!! note "FBMN Version Compatibility"
    We require a FBMN that is release_18 or newer. If your job is older than that, simply clone to latest to get the latest version and it should be compatible with ChemDir

**Workflow** 
Make sure you select the ChemDir workflow 

![img](img/ChemDir/ChemDir_step1.PNG)
 
**Title** 
Name your job to be easily recognize by yourself as it will be available in your jobs tab

![img](img/ChemDir/ChemDir_step2.PNG)

**Enter GNPS Network Task ID (Required)**
Copy and paste the FBMN task ID from your previous FBMN  job

![img](img/ChemDir/ChemDir_step3.PNG)

**METADATA_COLUMN**
Define a metadata column header based on the exact metadata table provided for the FBMN job ID you are using in this ChemDir workflow

![img](img/ChemDir/ChemDir_step4.PNG)

**TIME_SERIES**
Provide the variables that you are interested in based on your longitudinal analysis. Example: 0,1,2,3; comma separated values, can be integers or strings; no spaces between variables. The variables provided here must match entries from the metadata column specified in METADATA_COLUMN.

![img](img/ChemDir/ChemDir_step5.PNG)

**MIN_AREA_THRESHOLD** 
Min peak area; defined during feature finding; job specific. The value used here will replace any 0 value from your dataset for ChemDir.

![img](img/ChemDir/ChemDir_step6.PNG)

**METADATA_FILTER_COLUMN**
It is possible to filter the dataset based on the columns of interest. 

![img](img/ChemDir/ChemDir_step7.PNG)

**METADATA_FILTER_TERM**
It is possible to filter the column used from your dataset based on the specific term of interest for the analysis.

![img](img/ChemDir/ChemDir_step8.PNG)

**Job status**
Once your job is finished, you will be able to explore the results.

![img](img/ChemDir/ChemDir_step9.PNG)

**Summary table**
This table provides the general overview of every pair node compared via ChemDir.  

![img](img/ChemDir/ChemDir_step10.PNG)

**Direct Cytoscape preview**
This enables you to directly download and explore the data in Cytoscape.

![img](img/ChemDir/ChemDir_step11b.PNG)

**ChemDir dashboard**
This enables you to quickly explore the maximum ChemDir scores and their correspondent DeltaMZ observed from your dataset.

![img](img/ChemDir/ChemDir_step12.PNG)

## Development
Source code
There are two portions of the ChemDir infrastructure: [ChemDir GNPS/ProteoSAFe workflow](https://github.com/mwang87/ChemDir) and the [ChemDir Results Exploration Dashboard](https://github.com/mwang87/ChemDir_Dashboard). 

## Citation
To be updated

## Page Contributions

{{ git_page_authors }}
