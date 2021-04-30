## 1. Introduction

This page describes how you can convert raw data from Waters machines.

One of the most frequent questions from Waters users is if they can use MSe data for molecular networking. 
Bascially, <b>MSe data is not available for classical molecular networking workflow</b>, because it is a type of data-independent acquisition method so does not have precursor ion information.
However, <b>MSe data can be deconvoluted</b> (currently MS-DIAL is the proper software for it) <b>and applied to the FBMN workflow</b>. You can find relevant information [here](https://ccms-ucsd.github.io/GNPSDocumentation/featurebasedmolecularnetworking-with-mzmine2/).

There are two different file formats currently used by Waters. If you have .Raw data files acquired by MassLynx software, go to 3. Conversion of .Raw files. 
If you are using Waters machines operated by UNIFI software, see 2. Export UNIFI data.

## 2. Export UNIFI data

UNIFI keeps data in Oracle database architecture, so you cannot get your raw data by simple copy and paste.
As a first step of data conversion, you should export your data as MassLynx .Raw files.

TBU

## 3. How to convert Waters .Raw files to .mzML

If you convert Waters .Raw files directly following our [guideline](https://ccms-ucsd.github.io/GNPSDocumentation/fileconversion/), you will find some strange things.

Sometimes, Waters users find that the precursor m/z values are shifted severely, more than 0.01 Da. Here is the supposed reason:
When you open your data in MassLynx, MassLynx will show you m/z values 'corrected' by Lockspray data. However, the correction will not be made on the raw data files themselves, so if you convert them, Lockspray will not be applied to the resulting .mzML files.

You can make a Lockspray correction by using 'Accurate mass Measure' module of MassLynx. You can find it here:

![img](img/conversion/Waters_guide_1.png)


TBU
