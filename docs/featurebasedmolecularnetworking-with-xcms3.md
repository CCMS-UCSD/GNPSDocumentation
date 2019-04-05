## Introduction

The Feature-Based Molecular Networking (FBMN) is a computational method that bridges popular mass spectrometry data processing tools for LC-MS/MS and molecular networking analysis on [GNPS](http://gnps.ucsd.edu). The tools supported are: [MZmine2](featurebasedmolecularnetworking-with-mzmine2.md), [OpenMS](featurebasedmolecularnetworking-with-OpenMS.md), [MS-DIAL](featurebasedmolecularnetworking-with-ms-dial.md), [MetaboScape](featurebasedmolecularnetworking-with-metaboscape.md), and [XCMS](featurebasedmolecularnetworking-with-XCMS3.md).

The main documentation for Feature-Based Molecular Networking [can be accessed here:](featurebasedmolecularnetworking.md)

Below follows a description on how to use XCMS3 with the FBMN workflow in GNPS.

## Mass spectrometry processing with XCMS3

###Installation
Install the latest version of XCMS3 from the [XCMS3 GitHub repository] (https://github.com/sneumann/xcms) or the [Bioconductor XCMS3 package] (https://www.bioconductor.org/packages/release/bioc/html/xcms.html).

### Citations and development

This work builds on the efforts of our many colleagues, please cite their work:

[https://github.com/sneumann/xcms](https://github.com/sneumann/xcms)

Benton, H.P., Wong, D.M., Trauger, S.A., Siuzdak, G. [XCMS2: Processing Tandem Mass Spectrometry Data for Metabolite Identification and Structural Characterization.](https://pubs.acs.org/doi/abs/10.1021/ac800795f) Analytical Chemistry 80, 6382-6389 (2008).

Smith, C.A., Want, E.J., O'Maille, G., Abagyan,R., Siuzdak, G. [XCMS: Processing mass spectrometry data for metabolite profiling using nonlinear peak alignment, matching and identification.](https://pubs.acs.org/doi/10.1021/ac051437y) Analytical Chemistry, 78, 779–787 (2006).

### Mass Spectrometry Data Processing with XCMS3

As for all preprocessing software tools, a sequence of steps is performed to process mass spectrometry data in XCMS3. 

Here we will present key steps and representative scripts required to process untargeted LC-MS/MS data collected using data dependent acquisition. 

**SCRIPT AVAILABILITY:** Example XCMS3 scripts are accessible as *Jupyter notebook* and *RCommander script* on [https://github.com/DorresteinLaboratory/XCMS3_FeatureBasedMN](https://github.com/DorresteinLaboratory/XCMS3_FeatureBasedMN).

**IMPORTANT:** XCMS3 parameters will vary depending on the mass spectrometer, the acquisition parameters, and the samples investigated. The following documentation serves as a basic guideline for using XCMS3 with the Feature-Based Molecular Networking workflow.

Please consult these resources for more details on XCMS3 processing:

- The official [XCMS3 tutorial](add link).
- The video tutorial about [XCMS3 processing for Feature Based Molecular Networking](tutorials/americangutxcms3.md).

#### 1. Convert your LC-MS/MS Data to an Open Format
XCMS3 accepts different input formats. Note that we recommand to first convert your files to the mzML format before using XCMS3 for processing. [See the documentation here](fileconversion.md).

#### 2. Processing Steps with XCMS3
1. Import data
2. Peak picking
3. Retention time alignment
4. Peak grouping
5. Gap filling
6. Export the data for FBMN on GNPS
	-	a feature table with ion intensities (.TXT file format).
	- 	a MS/MS spectral data file (.MGF file format).
	
### Perform the Feature-Based Molecular Networking on GNPS

The files exported from XCMS3 can be uploaded to the GNPS web-platform and a Feature-Based Molecular Networking job can be launched.

See that documentation for [the FTP upload] (https://ccms-ucsd.github.io/GNPSDocumentation/fileupload/) and prepare your FBMN job [directly on GNPS](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22FEATURE-BASED-MOLECULAR-NETWORKING%22,%22library_on_server%22:%22d.speclibs;%22%7D) (you must be logged in first).

Note that you can upload a metadata table with your job. [See documentation](networking.md#metadata). 

More information on the Feature Based Molecular Networking workflow on GNPS can be obtained at [this documentation page](featurebasedmolecularnetworking.md).

### Representative files and job
Test files are accessible [here](tutorials/AG_tutorial_files/):

1. Feature Table - [Download here](tutorials/AG_tutorial_files/XCMS3-GNPS_AG_test_featuretable.txt)
2. MGF for MS/MS from above - [Download here](tutorials/AG_tutorial_files/XCMS3-GNPS_AG_test_GNPS.mgf)
3. A metadata table - [Download here](tutorials/AG_tutorial_files/metadata_GNPS_table_AMG_key_ones_cleaned.txt)

Here is an example [FBMN job with XCMS3](https://proteomics2.ucsd.edu/ProteoSAFe/status.jsp?task=f3f28a930b334dd09f310795fceae4cd) from a subset of the American Gut Project.

## Tutorials

See our [XCMS3 tutorial](tutorials/americangutxcms3.md) on using Feature Based Molecular Networking for a subset of the American Gut Project sample.
