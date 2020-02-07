# IIN with MZmine2

## Introduction

Ion Identity Network (IIN) is a computational method based on Pearson correlation that allows to correlate the different ions, including adducts, multimers and in-source fragmentation, that can be formed from the same molecule during the ESI ionization. This is an advanced option one might choose while processing data for [Feature Based Molecular Network (FBMN)](https://ccms-ucsd.github.io/GNPSDocumentation/featurebasedmolecularnetworking/). The supported tools for IIN are: MZmine, XCMS, and MS-DIAL.

You can find more information about IIN in this [playlist](https://www.youtube.com/playlist?list=PL4L2Xw5k8ITyxSyBdrcv70LDKsP8QNuyN).



## Development and Installation

For Ion Identity Network, download the MZmine software (MZmine-2.37.corr17.7_kai_merge2 version) available [here](https://github.com/robinschmid/mzmine2/releases).

## Data Processing with MZmine for FBMN and IIN
The sequence of steps for data processing in MZmine are essentially the same described in Data Processing with MZmine for FBMN in the standard workflow (from 1. data import, to 7. gap filling / 8. normalization),
however, before exporting to GNPS, some steps for IIN should be included for the edge annotations.
The scheme below shows the steps involved in the IIN workflow with MZmine.
























##Citations

This work builds on the efforts of our many colleagues, please cite their work:

**For IIN**: Schmid et al. In preparation.

**For FBMN**: Nothias, L.F. et al [Feature-based Molecular Networking in the GNPS Analysis Environment](https://www.biorxiv.org/content/10.1101/812404v1) bioRxiv 812404 (2019).



## Contributors
This integration was made possible by Hiroshi Tsugawa (Riken). This page was created by Louis Felix Nothias (UCSD).
