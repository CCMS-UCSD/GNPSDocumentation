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

## Runing MetaboScape
## A. Profile Analysis
1. Open *Profile Analysis* and process your data following *Profile Analysis* documentation to generate the Bucket Table.
2. Define groups and/or attributes to enhance downstream data analysis (see **3.3.4** in **MetaboScape 2.0 tutorial**). The groups and/or attributes defined in *Profile Analysis* will be visualized in the molecular networks using pie chart diagram.
3. **IMPORTANT**: Create one common group named 'SAMPLE' for all the samples. It will be used to enhance molecular networking visualization.
4. Export the Bucket Table to MetaboScape (see **3.1** in **MetaboScape 2.0 tutorial documentation**).

## B. MetaboScape
1. Open MetaboScape 2.0.
2. Open the project in MetaboScape (see **3.7** in **MetaboScape 2.0 tutorial documentation**).
3. Assign MS/MS spectra to the Bucket Table (see **3.7** in **MetaboScape 2.0 tutorial documentation**).
4. Sort buckets based on the presence of MS/MS.
5. Select only the buckets that have MS/MS associated with.
6. Perform *Automatic molecular formula generation using SmartFormula* (see **3.11.1** in **MetaboScape 2.0 tutorial documentation**) on these buckets. Make sure to select 'selected buckets only'.

![img](img/metaboscapeexportforgnps/Metabo_2.PNG)
Figure X. Search molecular formula with SmartFormula.

7. Right-click on the Bucket Table and select *Export to GNPS format* (.mgf/.csv).

![img](img/metaboscapeexportforgnps/Metabo_3.png)
Figure X. Export MetaboScape results files for GNPS.

![img](img/metaboscapeexportforgnps/Metabo_4.PNG)
Figure X. Export MetaboScape result files for GNPS.

## Video Tutorial - Run MetaboScape 

## Follow-up Tutorial in GNPS

Checkout the follow-up [tutorial](featurebasedgnps.md) on how to take the output of MetaboScape to produce a molecular network at GNPS.

Other tutorials are available from the main page of [Feature Based Molecular Networking Workflow](../featurebasedmolecularnetworking). 

## Follow-up Tutorial for Visualization of Molecular Networks with Cytoscape

Checkout the follow-up [tutorial](featurebasedmolecularnetworking-cytoscape.md) on how to visualize feature-based molecular networking with Cytoscape after running GNPS.

Other tutorials are available from the main page of [Feature Based Molecular Networking Workflow](../featurebasedmolecularnetworking).
