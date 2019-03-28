In this tutorial we highlight how to take the quantification/ms2 spectra to create a molecular network at GNPS.

## Prerequisites

If you have learned how to detect features, please checkout the [MZmine2 tutorial](tutorials/americangutmzmine).

## Experimental Setup

LC-MS/MS analysis of American Gut Stool samples for participants that consumed plants. MZmine2 was used to detect features and output a quantification table and MS2 Spectra MGF file with a single MS2 representing each consensus feature across all samples.

## Learning Objectives

1. Run Feature Based Molecular Networking for output from MZmine2 feature finding in GNPS. [See the workflow here](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22FEATURE-BASED-MOLECULAR-NETWORKING%22,%22library_on_server%22:%22d.speclibs;%22%7D) (Note that you must be logged in GNPS first).
2. Explore Molecular Networking Results briefly in GNPS
3. Export Molecular Network to Cytoscape


## Required Software Installs

1. FTP Client (e.g. WinSCP, DO NOT FileZilla!) [See instructions here](http://proteomics.ucsd.edu/service/massive/documentation/submit-data/upload-data/)
2. [Cytocape](http://www.cytoscape.org/download.php) for network visualization

## Data Availability

Full LC-MS/MS data can be found in the [MassIVE dataset MSV000082678](https://massive.ucsd.edu/ProteoSAFe/dataset.jsp?task=de2d18fd91804785bce8c225cc94a444).

### Files Needed for Tutorial

|     File Type    | Download Link          |
| ------------- |------------- |
| Feature Quantifications | [Download](ftp://massive.ucsd.edu/MSV000082678/updates/2018-08-02_lfnothias_4ee107d3/other/MZmine-GNPS_AG_test_featuretable.csv) |
| MS2 Spectra MGF | [Download](ftp://massive.ucsd.edu/MSV000082678/updates/2018-08-02_lfnothias_4ee107d3/other/MZmine-GNPS_AG_test_GNPS.mgf) |
| Study Metadata | [Download](ftp://massive.ucsd.edu/MSV000082678/other/metadata_GNPS_table_AMG_key_ones_cleaned.txt) |

## Video Tutorial - Analyze Feature Based Molecular Networking in GNPS

<iframe width="800" height="500" src="https://www.youtube.com/embed/NTkQ0fS1aug"> </iframe>

## Video Tutorial - Quick MZMine2 Export to GNPS Feature Based Molecular Networking

<iframe width="800" height="500" src="https://www.youtube.com/embed/vFcGG7T_44E"> </iframe>
