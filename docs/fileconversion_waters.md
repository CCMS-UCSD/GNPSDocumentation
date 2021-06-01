## 1. Introduction

This page describes how you can convert raw data from Waters machines.

One of the most frequent questions from Waters users is if they can use MSe data for molecular networking. 
Bascially, <b>MSe data is not available for classical molecular networking workflow</b>, because it is a type of data-independent acquisition method so does not have precursor ion information.
However, <b>MSe data can be deconvoluted</b> (currently MS-DIAL is the proper software for it) <b>and applied to the FBMN workflow</b>. You can find relevant information [here](https://ccms-ucsd.github.io/GNPSDocumentation/featurebasedmolecularnetworking-with-mzmine2/).

There are two different file formats currently used by Waters. 
If you have .Raw data files acquired by MassLynx software, see 3. Conversion of .Raw files. 
If you are using Waters machines operated by UNIFI software, see 2. Export UNIFI data.

## 2. Export UNIFI data

UNIFI keeps data in Oracle database architecture, so you cannot get your raw data by simple copy and paste.
As a first step of data conversion, you should export your data as MassLynx .Raw files.

TBU

UNIFI do not have any option for centroid mode acquisition, so your exported data will be continuum. 
The data should be centroided, and during centroiding, you also can make a Lockspray correction via 'Accurate mass Measure' module of MassLynx. You can find it here:

![img](img/conversion/Waters_guide_1.png)

## 3. How to convert Waters .Raw files to .mzML

ProteoWizard msConvert has been updated several times, and the recent version resolved many problems known for Waters data conversion.

[Here](https://www.dropbox.com/s/lqrqrqjwc8ubj3k/GNPS_Vendor_Conversion.zip?dl=1) is an updated version (with Proteowizard Release 3.0.21120)of the double-click converter we provided in our [guideline](https://ccms-ucsd.github.io/GNPSDocumentation/fileconversion/).



TBU
