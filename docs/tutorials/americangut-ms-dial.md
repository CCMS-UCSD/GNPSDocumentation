
In this tutorial you will be guided into running MS-DIAL for the Feature Based Molecular Network (FBMN) workflow on GNPS to reproduce some findings of the [American Gut Project](http://humanfoodproject.com/americangut/) described in this manuscript:

McDonald, D. et al. American Gut: an Open Platform for Citizen Science Microbiome Research. mSystems 3, (2018). [http://dx.doi.org/10.1128/mSystems.00031-18](http://dx.doi.org/10.1128/mSystems.00031-18)


## Learning Objectives

1. Learn how to download files from a GNPS/MassIVE Dataset. [See instructions here](../fileupload.md).
2. Run MS-DIAL feature detection on LC-MS/MS data. [See tutorial here](../featurebasedmolecularnetworking-ms-dial.md), and output a feature quantification table and a MS2 spectral file.
3. Run the Feature Based Molecular Networking (FBMN) with MS-DIAL files on GNPS. [See the tutorial here](../featurebasedmolecularnetworking.md).
4. Visualize the results of FBMN with Cytoscape [See the tutorial here](../featurebasedmolecularnetworking.md).

## Experimental Setup

We will use a subset of the LC-MS/MS analysis from the [American Gut Project](http://humanfoodproject.com/americangut/). The samples consist of fecal samples provided by participants and the subset selected consists of participants that have high and low consumption of plants. MS-DIAL will be used to detect features and output a feature quantification table (TXT format) and a MS2 spectral file (MGF format). 
The feature quantification table contains the intensity values for every aligned peak accross the samples, while the MS2 spectral file contains a single MS2 representing each aligned peak.


## Data and Files Needed for the Tutorial

LC-MS/MS data can be found in the [MassIVE dataset MSV000082678](https://massive.ucsd.edu/ProteoSAFe/dataset.jsp?task=de2d18fd91804785bce8c225cc94a444).
Study metadata (.TXT format) can [downloaded here](https://github.com/lfnothias/GNPSDocumentation/raw/master/docs/tutorials/AG_tutorial_files/MS-DIAL-GNPS_AG_test_featuretable.txt).

## MS-DIAL representative output files
These files are not needed for the tutorial but are provided here as reference files, or if you wanna by pass the MS-DIAL processing.

|     File Type    | Download Link          |
| ------------- |------------- |
| Feature quantification table (TXT format) | [Download](%ftp link should be added) |
| MS2 spectral file (MGF format) | [Download](https://github.com/lfnothias/GNPSDocumentation/raw/master/docs/tutorials/AG_tutorial_files/MS-DIAL-GNPS_AG_test_GNPS.mgf) |
| Study metadata (.TXT format)| [Download](https://github.com/lfnothias/GNPSDocumentation/raw/master/docs/tutorials/AG_tutorial_files/MS-DIAL-GNPS_AG_test_featuretable.txt) |
| MS-DIAL project (created with version X(| [Download](%ftp link should be added) |

## Required Software Installs

1. FTP Client (e.g. WinSCP, DO NOT FileZilla!). [See instructions here](../fileupload/)
2. [MS-DIAL](http://prime.psc.riken.jp/Metabolomics_Software/MS-DIAL/) for feature detection (available only on Windows).
3. An account on GNPS [https://gnps.ucsd.edu/ProteoSAFe/static/gnps-splash2.jsp]
4. [Cytocape](http://www.cytoscape.org/download.php) for network visualization

## Video Tutorial - Running MS-DIAL for FBMN
<iframe width="800" height="500" src="%please add the Youtube link (do we have the video?)"> </iframe>

## Running FBMN on GNPS

- [See the FBMN documentation](../featurebasedmolecularnetworking.md).

## Analyzing the Results of FBMN with Cytoscape

- [See the documentation for using Cytoscape for FBMN analysis](../featurebasedmolecularnetworking-cytoscape.md).

## Follow up Tutorial in GNPS

Checkout the follow up [tutorial](featurebasedgnps.md) on how to do FBMN with MZmine2 and GNPS.

Other tutorials are available from the main [Feature Based Molecular Networking Workflow page] (../featurebasedmolecularnetworking.md). 
