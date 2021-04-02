The [GNPS Dataset Explorer](https://gnps-explorer.ucsd.edu) is a simple interface to enable users to list out and select all files from a public dataset or analysis task. 

It current supports the following data sources:

1. MassIVE Public Datasets
1. GNPS Public Datasets
1. Metabolights Public Datasets
1. Metabolomics Workbench Public Datasets
1. GNPS Analysis Data Files (LC and GC)
1. PRIDE Proteomics Public Datasets
1. ProteomXchange Public Datasets

## Listing Dataset Files

Once you have entered an accession, a set of files will appear in the table. You may select one or more files to visualize. You can select "Visualize Files" below to see them in the GNPS Dashboard of the underlying raw data. Or you can choose to network them in GNPS by clicking "Molecular Network Files at GNPS". 

!!! note
    You may select to visualize all files if you do not want to select them. It is limited to the first 50 in the table, so if you filter the table, the it will trim down this 50. 

### Metadata

We attempt to gather metadata from several sources for public mass spectrometry data in MassIVE/GNPS. 

1. Default (MS information from run)
1. ReDU
1. MassIVE Metadata Uploads
1. Metabolights Study Information

## Listing GNPS Tasks

The Dataset Explorer will list out all the files selected in the gnps analysis and attempts to pull in the metadata from the analysis as well. 
## Comparing Two Files for LCMS Viewer

There are two tables with identical entries right above/below one another. This enables easily to select two sets of files to visualize in the GNPS Dashboard. Simply put a check mark next to the files in each table you want to compare and select the "Visualize Files" button below. 
