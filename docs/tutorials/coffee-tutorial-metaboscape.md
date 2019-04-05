## Tutorial Using MetaboScape and GNPS

In this tutorial you will be guided into running MetaboScape for the Feature Based Molecular Network (FBMN) workflow on GNPS to reproduce some findings of the [Coffee project](http://humanfoodproject.com/americangut/). *Is there any publication to this project?*

## Learning Objectives

1. Run MetaboScape feature detection on LC-MS/MS data, and output a feature quantification table and a MS2 spectral file. [See the tutorial here](../featurebasedmolecularnetworking.md)
2. Run GNPS and visualize output in Cytoscape.

## Experimental Setup

We will use a subset of the LC-MS/MS analysis from the Coffee project. *sample description*. MetaboScape will be used to detect features and output a feature quantification table (.csv format) and a MS2 spectral file (.mgf format). The feature quantification table contains the intensity values for every aligned peak accross the samples, while the MS2 spectral file contains a single MS2 representing each aligned peak.

## Data and Files Needed for the Tutorial

LC-MS/MS data and files can be found in the MassIVE dataset.

## Required Software Installations

1. FTP Client (e.g. WinSCP, DO NOT FileZilla!) [See instructions here](http://proteomics.ucsd.edu/service/massive/documentation/submit-data/upload-data/).
2. MetaboScape, commercially available from Bruker. 
3. [Cytocape](http://www.cytoscape.org/download.php) for network visualization.


## Video Tutorial - Run MetaboScape 

## Follow-up Tutorial in GNPS

Checkout the follow-up [tutorial](featurebasedgnps.md) on how to take the output of MetaboScape to produce a molecular network at GNPS.

Other tutorials are available from the main [Feature Based Molecular Networking Workflow page] (../featurebasedmolecularnetworking). 
