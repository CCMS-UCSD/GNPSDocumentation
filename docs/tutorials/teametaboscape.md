#EDIT THAT PAGE FOR TEA EXAMPLE
In this tutorial you will be guided into running MZmine2 for the Feature Based Molecular Network (FBMN) workflow on GNPS to reproduce. 

The main [Feature Based Molecular Networking Workflow documentation can be accessed here] (../featurebasedmolecularnetworking). 


## Learning Objectives

1. Learn how to download files from a GNPS/MassIVE Dataset.
2. Run MZmine2 feature detection on LC-MS/MS data, and output a feature quantification table and a MS2 spectral file. [See the tutorial here](https://ccms-ucsd.github.io/GNPSDocumentation/featurebasedmolecularnetworking/)

## Experimental Setup

We will use a subset of the LC-MS/MS analysis from the [American Gut Project](http://humanfoodproject.com/americangut/). The samples consist of fecal samples provided by participants and the subset selected consists of participants that have high and low consumption of plants. MZmine2 will be used to detect features and output a feature quantification table (CSV format) and a MS2 spectral file (MGF format). 
The feature quantification table contains the intensity values for every aligned peak accross the samples, while the MS2 spectral file contains a single MS2 representing each aligned peak.


## Data Availability

LC-MS/MS data can be found in the [MassIVE dataset MSV000082678](https://massive.ucsd.edu/ProteoSAFe/dataset.jsp?task=de2d18fd91804785bce8c225cc94a444).

## Required Software Installs

1. FTP Client (e.g. WinSCP, DO NOT FileZilla!) [See instructions here](http://proteomics.ucsd.edu/service/massive/documentation/submit-data/upload-data/)
2. [MZMine2](https://github.com/mzmine/mzmine2/releases) for feature detection
3. [Cytocape](http://www.cytoscape.org/download.php) for network visualization
4. MetaboScape [LINK]


## Video Tutorial - Run MZmine2

**IMPORTANT:** MZmine2 processing for FBMN has been slightly updated since this video was produced. Please refer to this page for up-to-date informations on MZmine2 processing for the FBMN [step-by-step documentation for MZmine2 processing](../featurebasedmolecularnetworking-with-mzmine2). 

<iframe width="800" height="500" src="https://www.youtube.com/embed/5jjMllbwD-U"> </iframe>

## Follow up Tutorial in GNPS

Other tutorials using different processing softwares are available from the main [Feature Based Molecular Networking Workflow page] (../featurebasedmolecularnetworking). 
