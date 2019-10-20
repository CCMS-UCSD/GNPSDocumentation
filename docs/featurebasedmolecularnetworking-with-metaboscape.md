## Introduction

**Feature-Based Molecular Networking** (FBMN) is a computational method that bridges popular mass spectrometry data processing tools for LC-MS/MS and molecular networking analysis on [GNPS](http://gnps.ucsd.edu). The supported tools are: [MZmine](featurebasedmolecularnetworking-with-mzmine2.md), [OpenMS](featurebasedmolecularnetworking-with-openms.md), [MS-DIAL](featurebasedmolecularnetworking-with-ms-dial.md), [MetaboScape](featurebasedmolecularnetworking-with-metaboscape.md), [XCMS](featurebasedmolecularnetworking-with-xcms3.md), [Progenesis QI](featurebasedmolecularnetworking-with-progenesisQI.md), and the [mzTab-M format](featurebasedmolecularnetworking-with-mztab-m.md).

The main documentation for FBMN [can be accessed here](featurebasedmolecularnetworking.md).

Below we describe how to use MetaboScape with the FBMN workflow on GNPS.

## Using MetaboScape and the Feature-Based Molecular Networking

MetaboScape can be used to process LC-MS/MS Bruker Daltonics data files (i.e. *.d files). After the processing with MetaboScape, the output files can be used to run the Feature-Based Molecular Networking workflow on GNPS either using the [Superquick FBMN start page] (http://dorresteinappshub.ucsd.edu:5050/featurebasednetworking) or [the standard interface of the FBMN workflow](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22FEATURE-BASED-MOLECULAR-NETWORKING%22,%22library_on_server%22:%22d.speclibs;%22%7D) (you need to be logged in to GNPS first).

**Requirements:** 
Install [MetaboScape](https://www.bruker.com/products/mass-spectrometry-and-separations/ms-software/metaboscape/overview.html) (at least version 2.0) and get a valid license. 

## A. Perform Feature Detection with Profile Analysis
1. Open *Profile Analysis* and perform feature detection on your data following *Profile Analysis* documentation to generate an ion feature bucket table.
2. Define groups and/or attributes to enhance downstream data analysis (see **3.3.4** in the **MetaboScape 2.0 tutorial documentation**). The groups and/or attributes defined in *Profile Analysis* will be visualized in the molecular networks using pie chart diagram.
3. **IMPORTANT**: Create one common group named 'SAMPLE' for all the samples. It will be used for molecular networking visualization.
4. Export the bucket table to MetaboScape (see **3.1** in the **MetaboScape 2.0 tutorial documentation**).

## B. Use MetaboScape to Annotate MS/MS spectra
1. Open MetaboScape.
2. Open the project in MetaboScape (see **3.7** in **MetaboScape 2.0 tutorial documentation**).
3. Assign MS/MS spectra to the bucket table (see **3.7** in **MetaboScape 2.0 tutorial documentation**).
4. Sort buckets based on the presence of MS/MS.
5. Select only the buckets that have MS/MS associated with them.
6. Perform *Automatic molecular formula generation using SmartFormula* (see **3.11.1** in **MetaboScape 2.0 tutorial documentation**) on these buckets. Make sure to select *Selected buckets only*.
7. Search molecular formula with **SmartFormula**.

![img](img/metaboscapeexportforgnps/Metabo_2.PNG)

8. Right-click on the bucket table and select *Export to GNPS format* (.mgf/.csv).

![img](img/metaboscapeexportforgnps/Metabo_3.png)

9. Select *Export all formats*.

![img](img/metaboscapeexportforgnps/Metabo_4.PNG)

10. The .mgf file ('gnps.mgf') and the bucket table will be used to perform a **Feature-Based Molecular Networking** job on GNPS (see below). 

## C. Perform FBMN Job on GNPS
Go to GNPS to perform a FBMN job. [Refer to that documentation](featurebasedmolecularnetworking.md).

## D. Step-by-Step Tutorial
See the [step-by-step tutorial using MetaboScape 2.0 and the FBMN](tutorials/coffee-tutorial-metaboscape.md) for the Coffee tutorial (part of the **MetaboScape 2.0 documentation**).

![img](img/metaboscapeexportforgnps/Cyto13.PNG)

### Page contributors
Louis Felix Nothias (UCSD), Tam Dang (Tech. Univ. Berlin), Kevin Ngoc (UCSD), Ivan Protsyuk (EMBL, Heidelberg, Germany).

### Join the GNPS Community !

- For informations/feature request, please open an "Issue" on the [*CCMS-UCSD/GNPSDocumentation*]((https://github.com/CCMS-UCSD/GNPSDocumentation)) GitHub repository.
- To contribute to the GNPS documentation, please use GitHub by forking the [*CCMS-UCSD/GNPSDocumentation*]((https://github.com/CCMS-UCSD/GNPSDocumentation)) repository, and make a "Pull Request" with the changes.