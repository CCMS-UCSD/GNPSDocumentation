# Introduction

**Feature-Based Molecular Networking** (FBMN) is a computational method that bridges popular mass spectrometry data processing tools for LC-MS/MS and molecular networking analysis on [GNPS](http://gnps.ucsd.edu). The supported tools are: [MZmine](featurebasedmolecularnetworking-with-mzmine2.md), [OpenMS](featurebasedmolecularnetworking-with-openms.md), [MS-DIAL](featurebasedmolecularnetworking-with-ms-dial.md), [MetaboScape](featurebasedmolecularnetworking-with-metaboscape.md), [XCMS](featurebasedmolecularnetworking-with-xcms3.md), [Progenesis QI](featurebasedmolecularnetworking-with-progenesisQI.md), and the [mzTab-M format](featurebasedmolecularnetworking-with-mztab-m.md).

The main documentation for Feature-Based Molecular Networking [can be accessed here:](featurebasedmolecularnetworking.md)

Below follows a description on how to use mz-Tab-M format with the FBMN workflow on GNPS.

# The mzTab-M format

## Introduction

## Citations and development

This work builds on the efforts of our many colleagues, please cite their work: [https://github.com/sneumann/xcms](https://github.com/sneumann/xcms)

Tautenhahn R, Boettcher C, Neumann S. [Highly sensitive feature detection for
high resolution LC/MS](https://doi.org/10.1186/1471-2105-9-504) BMC
Bioinformatics, 9:504 (2008).


	- **Option A** - Export a **feature quantification table** and a **MS/MS spectral summary file**:
		-	Export a **feature quantification table** with ion intensities (.TXT file format) (`writeMgfData`).
		-  	Export a **MS/MS spectral summary file** (.MGF file format). Note that it is recommended to use the maxTIC option for the MGF export. (`write.table`)
	- **Option B** - Export an **mzTab-M file**:
 
 		- Export and select the **mzTab-M file** in the interface. The use of the mzTab-M requires the subsequent upload of the mzML files used during the XCMS processing. See and cite this [publication](https://pubs.acs.org/doi/abs/10.1021/acs.analchem.8b04310).
 

### Perform FBMN on GNPS

The files exported from XCMS3 can be uploaded to the GNPS web-platform and a
FBMN job can be launched.

FBMN with XCMS3 can be performed either using the [Superquick FBMN start page] (http://dorresteinappshub.ucsd.edu:5050/featurebasednetworking) or [the standard interface of the FBMN workflow](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22FEATURE-BASED-MOLECULAR-NETWORKING%22,%22library_on_server%22:%22d.speclibs;%22%7D) (you need to be logged in GNPS first).

More information on the FBMN on GNPS can
be obtained at [this documentation page](featurebasedmolecularnetworking.md).

Note that you can upload a metadata table with your job. [See
documentation](networking.md#metadata).

![img](img/featurebasedmolecularnetworking/xcms_quickstart.png)

**Option B** - With a mzTab-M file:

1. The **mzTab-M** file - [Download here](tutorials/AG_tutorial_files/TBProvided)
2. The corresponding **mzML** file(s) - [Download here](tutorials/AG_tutorial_files/TBProvided)

Support the mzTab-M 2.0 (release 1.0.5)
Here is an example [FBMN job with XCMS using a mzTab-M file and mzML files](TBProv) from a subset of the American Gut Project.

### Page contributors

Johannes Rainer (Eurac Research), Madeleine Ernst (UCSD), Ricardo da Silva
(UCSD), Michael Witting (Helmholtz Zentrum Munich), Louis Felix Nothias (UCSD) and Ming Wang (UCDS). 

### Join the GNPS Community !

- For feature request, or to report bugs, please open an "Issue" on the [*CCMS-UCSD/GNPS_Workflows* GitHub repository](https://github.com/CCMS-UCSD/GNPS_Workflows).
- To contribute to the GNPS documentation, please use GitHub by forking the [*CCMS-UCSD/GNPSDocumentation*]((https://github.com/CCMS-UCSD/GNPSDocumentation)) repository, and make a "Pull Request" with the changes.
