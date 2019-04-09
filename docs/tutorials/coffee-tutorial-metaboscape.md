## Tutorial Using MetaboScape and GNPS

In this tutorial you will be guided into running MetaboScape for the Feature Based Molecular Network (FBMN) workflow on GNPS to reproduce some findings of the [Coffee project](http://humanfoodproject.com/americangut/).

## Learning Objectives

1. Run MetaboScape feature detection on LC-MS/MS data, and receive a feature quantification table and a MS2 spectral file as an output. [See the tutorial here](../featurebasedmolecularnetworking.md).
2. Run GNPS and visualize output in Cytoscape.

## Experimental Setup

We will use a subset of the LC-MS/MS analysis from the Coffee project. 

*Sample description still needed*. 

MetaboScape will be used to detect features and output a feature quantification table (.csv format) and a MS2 spectral file (.mgf format). The feature quantification table contains the intensity values for every aligned peak accross the samples, while the MS2 spectral file contains a single MS2 representing each aligned peak.

## Data and Files Needed for the Tutorial

LC-MS/MS data and files can be found in the MassIVE dataset.

## MetaboScape representative output files
These files are not needed for the tutorial but are provided here as reference files, or if you want to bypass the MetaboScape processing.

|     File Type    | Download Link          |
| ------------- |------------- |
| Feature quantification table (CSV format) | [Download](https://github.com/lfnothias/GNPSDocumentation/blob/master/docs/tutorials/AG_tutorial_files/MetaboScape-GNPS-Coffee_Tutorial_msmsonly_featuretable.csv) |
| MS2 spectral file (MGF format) | [Download](https://github.com/lfnothias/GNPSDocumentation/blob/master/docs/tutorials/AG_tutorial_files/MetaboScape-GNPS-Coffee_Tutorial.mgf) |

## Required Software Installations

1. FTP Client (e.g. WinSCP, DO NOT USE FileZilla!) [See instructions here](http://proteomics.ucsd.edu/service/massive/documentation/submit-data/upload-data/).
2. MetaboScape, commercially available from Bruker. 
3. [Cytocape](http://www.cytoscape.org/download.php) for network visualization.

## Running MetaboScape
Refer to the detailed step-by-step procedure to run Metaboscape [here](MetaboScapeexportforGNPSSiriusmodule.md).

## Video Tutorial - Run MetaboScape 

## Running GNPS

See the documentation to produce molecular network at GNPS with the output of the Coffee Project [here](featurebasedgnps.md).

## Running Cytoscape

See the documentation to perform visualization of the molecular networking on the data of the Coffee Project [here](featurebasedmolecularnetworking-cytoscape.md).


