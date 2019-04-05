## Introduction

The Feature-Based Molecular Networking (FBMN) is a computational method that bridges popular mass spectrometry data processing tools for LC-MS/MS and molecular networking analysis on [GNPS](http://gnps.ucsd.edu). The tools supported are: [MZmine2](featurebasedmolecularnetworking-with-mzmine2.md), [OpenMS](featurebasedmolecularnetworking-with-OpenMS.md), [MS-DIAL](featurebasedmolecularnetworking-with-ms-dial.md), [MetaboScape](featurebasedmolecularnetworking-with-metaboscape.md), and [XCMS](featurebasedmolecularnetworking-with-XCMS3.md).

The main documentation for FBMN [can be accessed here:](featurebasedmolecularnetworking.md)

Below we are describing how to use MetaboScape with the FBMN workflow on GNPS.

## Using MetaboScape and the Feature-Based Molecular Networking

MetaboScape can be used to process LC-MS/MS Bruker Daltonics data files (.d format). The results of MetaboScape can be used to run the Feature-Based Molecular Network workflow on [GNPS] (http://gnps.ucsd.edu).

**Requirements:** 
Installing [MetaboScape](https://www.bruker.com/products/mass-spectrometry-and-separations/ms-software/metaboscape/overview.html) (version 2.0 minimum) and having a valid licence. 

## A. Perform Feature Detection with Profile Analysis
1. Open *Profile Analysis* and perform feature detection on your data following *Profile Analysis* documentation to generate the Bucket Table.
2. Define groups and/or attributes to enhance downstream data analysis (see part **3.3.4** in the **MetaboScape 2.0 tutorial** documentation). The groups and/or attributes defined in *Profile Analysis* will be visualized in the molecular networks using pie chart diagram.
3. **IMPORTANT**: Create one common group named 'SAMPLE' for all the samples. It will be used for molecular networking visualization.
4. Export the Bucket Table to MetaboScape (see **3.1** in the **MetaboScape 2.0 tutorial** documentation).

## B. Use MetaboScape to Annotate MS/MS spectra
1. Open MetaboScape.
2. Open the project in MetaboScape (see **3.7** in **MetaboScape 2.0 tutorial documentation**).
3. Assign MS/MS spectra to the Bucket Table (see **3.7** in **MetaboScape 2.0 tutorial documentation**).
4. Sort buckets based on the presence of MS/MS.
5. Select only the buckets that have MS/MS associated with.
6. Perform *Automatic molecular formula generation using SmartFormula* (see **3.11.1** in **MetaboScape 2.0 tutorial documentation**) on these buckets. Make sure to select 'selected buckets only'.
7. Search molecular formula with SmartFormula**.

![img](img/metaboscapeexportforgnps/Metabo_2.PNG)

8. Right-click on the Bucket Table and select *Export to GNPS format* (.mgf/.csv).

![img](img/metaboscapeexportforgnps/Metabo_3.png)
9. Select **Export all formats**.

![img](img/metaboscapeexportforgnps/Metabo_4.PNG)

10. The .MGF file ("gnps.mgf") and the Bucket Table will be used to perform a **Feature-Based Molecular Networking** job on GNPS (see below).

## C. Performing a FBMN job on GNPS
Go to GNPS to perform a FBMN job. [Refer to that documentation] (featurebasedmolecularnetworking.md).

## D. Step-by-step tutorial
See the [step-by-step tutorial using MetaboScape 2.0 and the FBMN](tutorials/coffee-tutorial-metaboscape.md) for the coffee tutorial (part of the MetaboScape documentation).
