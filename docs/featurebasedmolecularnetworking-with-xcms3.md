## Introduction

**Feature-Based Molecular Networking** (FBMN) is a computational method that bridges popular mass spectrometry data processing tools for LC-MS/MS and molecular networking analysis on [GNPS](http://gnps.ucsd.edu). The supported tools are: [MZmine2](featurebasedmolecularnetworking-with-mzmine2.md), [OpenMS](featurebasedmolecularnetworking-with-openms.md), [MS-DIAL](featurebasedmolecularnetworking-with-ms-dial.md), [MetaboScape](featurebasedmolecularnetworking-with-metaboscape.md), [XCMS](featurebasedmolecularnetworking-with-xcms3.md), and [Progenesis QI](featurebasedmolecularnetworking-with-progenesisQI.md).

The main documentation for Feature-Based Molecular Networking [can be accessed here:](featurebasedmolecularnetworking.md)

Below follows a description on how to use `xcms` version >= 3 (XCMS3) with the
FBMN workflow on GNPS.

## Mass spectrometry processing with XCMS3

### Installation

Install the latest version of XCMS3 from Bioconductor (version >= 3.4) in R
with:

```
install("BiocManager")
BiocManager::install("xcms")
```

See also the [xcms Bioconductor package] (https://www.bioconductor.org/packages/release/bioc/html/xcms.html).

Clone also the GitHub repository
[https://github.com/jorainer/xcms-gnps-tools](https://github.com/jorainer/xcms-gnps-tools)
for utility functions (*XCMS-GNPS-TOOLS*) specific to this workflow.

### Citations and development

This work builds on the efforts of our many colleagues, please cite their work:

[https://github.com/sneumann/xcms](https://github.com/sneumann/xcms)

Tautenhahn R, Boettcher C, Neumann S. [Highly sensitive feature detection for
high resolution LC/MS](https://doi.org/10.1186/1471-2105-9-504) BMC
Bioinformatics, 9:504 (2008).

Smith, C.A., Want, E.J., O'Maille, G., Abagyan,R., Siuzdak, G. [XCMS: Processing
mass spectrometry data for metabolite profiling using nonlinear peak alignment, matching and identification.](https://pubs.acs.org/doi/10.1021/ac051437y)
Analytical Chemistry, 78, 779–787 (2006).


### Mass Spectrometry Data Processing with XCMS3.

Here we will present key steps and representative scripts required to process
untargeted LC-MS/MS data collected using data dependent acquisition.

**SCRIPT AVAILABILITY:** Example XCMS3 scripts are accessible as *Jupyter
notebook* and *RCommander script* on
[https://github.com/DorresteinLaboratory/XCMS3_FeatureBasedMN](https://github.com/DorresteinLaboratory/XCMS3_FeatureBasedMN).

**IMPORTANT:** XCMS3 parameters will vary depending on the mass spectrometer,
the acquisition parameters, and the samples investigated. The following
documentation serves as a basic guideline for using XCMS3 with the Feature-Based
Molecular Networking workflow.

Please consult these resources for more details on XCMS3 processing and
definition of parameter settings:

- The official [XCMS3
  tutorial](https://bioconductor.org/packages/release/bioc/vignettes/xcms/inst/doc/xcms.html)
  (also provided as `xcms` vignette with the `xcms` R package).
- XCMS3 workshop from the Metabolomics 2018 conference:
  [xcms-preprocessing](https://jorainer.github.io/metabolomics2018/xcms-preprocessing.html)
  and [github repository](https://github.com/jorainer/metabolomics2018).

#### 1. Convert your LC-MS/MS Data to an Open Format

XCMS3 accepts different input formats. Note that we recommand to first convert
your files to the mzML format before using XCMS3 for processing. [See the
documentation here](fileconversion.md).

#### 2. Processing Steps with XCMS3

1. Import data (`readMSData`)
2. Peak picking (`findChromPeaks`)
3. Retention time alignment (`adjustRtime`).
4. Peak grouping (`groupChromPeaks`).
5. Gap filling (`fillChromPeaks`).
6. Export the data for FBMN on GNPS
	-	a *feature quantification table* with ion intensities (.TXT file format).
	- 	a *MS/MS spectral summary file* (.MGF file format). Note that it is recommended to use the maxTIC option for the MGF export.

### Perform the Feature-Based Molecular Networking on GNPS

The files exported from XCMS3 can be uploaded to the GNPS web-platform and a
Feature-Based Molecular Networking job can be launched.


FBMN with XCMS3 can be performed either using the [Superquick FBMN start page] (http://dorresteinappshub.ucsd.edu:5050/featurebasednetworking) or [the standard interface of the FBMN workflow](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22FEATURE-BASED-MOLECULAR-NETWORKING%22,%22library_on_server%22:%22d.speclibs;%22%7D) (you need to be logged in GNPS first).

More information on the Feature Based Molecular Networking workflow on GNPS can
be obtained at [this documentation page](featurebasedmolecularnetworking.md).

Note that you can upload a metadata table with your job. [See
documentation](networking.md#metadata).

### Representative files and job

Test files are accessible [here](tutorials/AG_tutorial_files/):

1. A *feature quantification table* - [Download here](tutorials/AG_tutorial_files/XCMS3-GNPS_AG_test_featuretable.txt)
2. A *MS/MS spectral summary* file from above - [Download here](tutorials/AG_tutorial_files/XCMS3-GNPS_AG_test_GNPS.mgf)
3. A *metadata table* - [Download here](tutorials/AG_tutorial_files/metadata_GNPS_table_AMG_key_ones_cleaned.txt)

Here is an example [FBMN job with XCMS3](https://proteomics2.ucsd.edu/ProteoSAFe/status.jsp?task=f3f28a930b334dd09f310795fceae4cd) from a subset of the American Gut Project.

## Tutorials

See our XCMS-FBMN tutorials using python and R with a subset of the American Gut Project samples on this repository [DorresteinLaboratory/XCMS3_FeatureBasedMN/](https://github.com/DorresteinLaboratory/XCMS3_FeatureBasedMN/).

## Page contributors

Johannes Reiner (Eurac Research), Madeleine Ernst (UCSD), Ricardo da Silva (UCSD), Michael Wittig (Munich University), Louis Felix Nothias (UCSD), Ivan Protsyuk (EMBL, Heidelberg, Germany). 

## Contribute to the Documentation

- For informations/feature request, please open an "Issue" on the [*CCMS-UCSD/GNPSDocumentation*]((https://github.com/CCMS-UCSD/GNPSDocumentation)) GitHub repository.
- To contribute directly to the GNPS documentation, fork the [*CCMS-UCSD/GNPSDocumentation*]((https://github.com/CCMS-UCSD/GNPSDocumentation)) repository, and make a "Pull Request".
