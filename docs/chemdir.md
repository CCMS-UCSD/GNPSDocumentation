

Pardon our dust, this is a work in progress...

**ChemDir**

The Chemical Directionality (ChemDir) approach enable us to identify time points where high differential changes occur between two chemically related compounds, directly connected nodes in a network, that can be considered putative educt and product of a chemical or biochemical transformation.

**Workflow**: ChemDir workflow: make sure you select the ChemDir workflow

**Title**: name your job to be easily recognize by yourself as it will be available in your jobs tab

**Enter GNPS Network Task ID (Required)**: copy and paste the FBMN task ID from your previous FBMN job

**METADATA_COLUMN**: define a metadata column header based on the exact metadata table provided for the FBMN job ID you are using in this ChemDir workflow

**TIME_SERIES**: Provide the variables that are interested in based on your longitudinal analysis. Example: 0,1,2,3; comma separated values, can be integers or strings. The variables provided here must match entries from the metadata column specified in METADATA_COLUMN

**MIN_AREA_THRESHOLD**: min peak area; defined during feature finding; job specific. The value used here will replace any 0 value from your dataset for ChemDir

**METADATA_FILTER_COLUMN**: it is possible to filter the dataset based on the columns of interest.

**METADATA_FILTER_TERM**: it is possible to filter the column used from your dataset based on the specific term of interest for the analysis.

**Job status**: once your job is finished, you will be able to explore the results

**Summary table**: this table provides the general overview of every pair node compared via ChemDir.

**Direct Cytoscape preview**: this enables you to directly download and explore the data in Cytoscape

**ChemDir dashboard**: this enables you to quickly explore the maximum ChemDir scores and their correspondent DeltaMZ observed from your dataset
