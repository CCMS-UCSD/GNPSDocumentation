
In this tutorial you will be guided into running MetaboScape for the Feature Based Molecular Network (FBMN) workflow on GNPS to reproduce some findings of the [Coffee project](http://humanfoodproject.com/americangut/) described in this manuscript:

McDonald, D. et al. American Gut: an Open Platform for Citizen Science Microbiome Research. mSystems 3, (2018). [http://dx.doi.org/10.1128/mSystems.00031-18](http://dx.doi.org/10.1128/mSystems.00031-18)


## Learning Objectives

1. Learn how to download files from a GNPS/MassIVE Dataset.
2. Run MZmine2 feature detection on LC-MS/MS data, and output a feature quantification table and a MS2 spectral file. [See the tutorial here](../featurebasedmolecularnetworking.md)

## Experimental Setup

We will use a subset of the LC-MS/MS analysis from the [American Gut Project](http://humanfoodproject.com/americangut/). The samples consist of fecal samples provided by participants and the subset selected consists of participants that have high and low consumption of plants. MZmine2 will be used to detect features and output a feature quantification table (CSV format) and a MS2 spectral file (MGF format). 
The feature quantification table contains the intensity values for every aligned peak accross the samples, while the MS2 spectral file contains a single MS2 representing each aligned peak.


## Data and Files Needed for the Tutorial

LC-MS/MS data and files can be found in the [MassIVE dataset MSV000082678](https://massive.ucsd.edu/ProteoSAFe/dataset.jsp?task=de2d18fd91804785bce8c225cc94a444), and can be retrieved from the table below:


|     File Type    | Download Link          |
| ------------- |------------- |
| Feature quantification table (CSV format) | [Download](ftp://massive.ucsd.edu/MSV000082678/updates/2018-08-02_lfnothias_4ee107d3/other/MZmine-GNPS_AG_test_featuretable.csv) |
| MS2 spectral file (MGF format) | [Download](ftp://massive.ucsd.edu/MSV000082678/updates/2018-08-02_lfnothias_4ee107d3/other/MZmine-GNPS_AG_test_GNPS.mgf) |
| Study metadata (.TXT format)| [Download](ftp://massive.ucsd.edu/MSV000082678/other/metadata_GNPS_table_AMG_key_ones_cleaned.txt) |
| (Optional) MZmine2 batch file (.XML format)| [Download](ftp://massive.ucsd.edu/MSV000082678/updates/2018-08-02_lfnothias_4ee107d3/other/qtof_batch_AG_training.xml) |
| (Optional) MZmine2 project| [Download](ftp://massive.ucsd.edu/MSV000082678/updates/2018-08-02_lfnothias_4ee107d3/other/MZmine-GNPS_AG_test.mzmine) |

## Required Software Installs

1. FTP Client (e.g. WinSCP, DO NOT FileZilla!) [See instructions here](http://proteomics.ucsd.edu/service/massive/documentation/submit-data/upload-data/)
2. [MZMine2](https://github.com/mzmine/mzmine2/releases) for feature detection
3. [Cytocape](http://www.cytoscape.org/download.php) for network visualization


## Video Tutorial - Run MetaboScape 

**IMPORTANT:** MZmine2 processing for FBMN has been slightly updated since this video was produced. Please refer to this page for up-to-date informations on MZmine2 processing for the FBMN [step-by-step documentation for MZmine2 processing](../featurebasedmolecularnetworking-with-mzmine2). 

<iframe width="800" height="500" src="https://www.youtube.com/embed/5jjMllbwD-U"> </iframe>

## Follow up Tutorial in GNPS

Checkout the follow up [tutorial](featurebasedgnps.md) on how to take the output of MZMine2 to produce a molecular network at GNPS.

Other tutorials are available from the main [Feature Based Molecular Networking Workflow page] (../featurebasedmolecularnetworking). 
