In this tutorial you will be guided into running the [Feature Based Molecular Network (FBMN)](../featurebasedmolecularnetworking.md) workflow on GNPS to reproduce some findings of the [American Gut Project](http://humanfoodproject.com/americangut/) described in this manuscript:

McDonald, D. et al. American Gut: an Open Platform for Citizen Science Microbiome Research. mSystems 3, (2018). [http://dx.doi.org/10.1128/mSystems.00031-18](http://dx.doi.org/10.1128/mSystems.00031-18)

## Learning Objectives

1. Run the Feature Based Molecular Networking using MZmine2 outputted files along with a metadata table. [See the workflow here](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22FEATURE-BASED-MOLECULAR-NETWORKING%22,%22library_on_server%22:%22d.speclibs;%22%7D) (Note that you must be logged in GNPS first).
2. Explore Molecular Networking results briefly in GNPS
3. Export Molecular Network to Cytoscape

## Prerequisites

The LC-MS/MS data have first to be processed with MZmine2. The resulting MZmine2 output files needed for FBMN are provided here. If you have not learned that process yet, refer to this [MZmine2 tutorial](tutorials/americangutmzmine).

## Experimental Setup

We will use a subset of the LC-MS/MS analysis from the [American Gut Project](http://humanfoodproject.com/americangut/). The samples consist of fecal samples provided by participants and the subset selected consists of participants that have high and low consumption of plants. MZmine2 was used to detect features and output a feature quantification table (CSV format) and a MS2 spectral file (MGF format). 
The feature quantification table contains the intensity values for every aligned peak accross the samples, while the MS2 spectral file contains a single MS2 representing each aligned peak. There is a dedicated [MZmine2 tutorial](tutorials/americangutmzmine) describing that process.

## Data Availability

The LC-MS/MS data can be found in the [MassIVE dataset MSV000082678](https://massive.ucsd.edu/ProteoSAFe/dataset.jsp?task=de2d18fd91804785bce8c225cc94a444).

### Files Needed for Tutorial

|     File Type    | Download Link          |
| ------------- |------------- |
| Feature quantification table (CSV format) | [Download](ftp://massive.ucsd.edu/MSV000082678/updates/2018-08-02_lfnothias_4ee107d3/other/MZmine-GNPS_AG_test_featuretable.csv) |
| MS2 spectral file (MGF format) | [Download](ftp://massive.ucsd.edu/MSV000082678/updates/2018-08-02_lfnothias_4ee107d3/other/MZmine-GNPS_AG_test_GNPS.mgf) |
| Study metadata (.TXT format)| [Download](ftp://massive.ucsd.edu/MSV000082678/other/metadata_GNPS_table_AMG_key_ones_cleaned.txt) |
| (Optional) MZmine2 batch file (.XML format)| [Download](ftp://massive.ucsd.edu/MSV000082678/updates/2018-08-02_lfnothias_4ee107d3/other/qtof_batch_AG_training.xml) |
| (Optional) MZmine2 project| [Download](ftp://massive.ucsd.edu/MSV000082678/updates/2018-08-02_lfnothias_4ee107d3/other/MZmine-GNPS_AG_test.mzmine) |

### Demo GNPS job of Feature Based Molecular Networking
[Here is an example FBMN](https://gnps.ucsd.edu/ProteoSAFe/status.jsp?task=52a390c8eb654b7fa8d61a1c7a4aaab5) job with files resulting from MZmine2 processing of a subset of the [American Gut Project] (http://humanfoodproject.com/americangut/).

## Required Software Installs

1. FTP Client (e.g. WinSCP, DO NOT FileZilla!) [See instructions here](http://proteomics.ucsd.edu/service/massive/documentation/submit-data/upload-data/)
2. [Cytocape](http://www.cytoscape.org/download.php) for network visualization

## For step-by-step tutorial on Feature Based Molecular Networking

**IMPORTANT:** Note that the Feature Based Molecular Networking workflow has been slightly updated since the following videos were produced. Please refer to this page for the most recent description of [step-by-step MZmine2 processing for the FBMN workflow](../featurebasedmolecularnetworking-with-mzmine2.md). 

## Video Tutorial - Analyze Feature Based Molecular Networking in GNPS


<iframe width="800" height="500" src="https://www.youtube.com/embed/NTkQ0fS1aug"> </iframe>

## Video Tutorial - Quick MZMine2 Export to GNPS Feature Based Molecular Networking


<iframe width="800" height="500" src="https://www.youtube.com/embed/vFcGG7T_44E"> </iframe>
