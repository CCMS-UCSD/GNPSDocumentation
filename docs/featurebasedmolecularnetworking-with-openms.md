## Introduction to FBMN

The Feature-Based Molecular Networking (FBMN) is a computational method that bridges popular mass spectrometry data processing tools for LC-MS/MS and molecular networking analysis on [GNPS](http://gnps.ucsd.edu). The tools supported are: [MZmine2](featurebasedmolecularnetworking-with-mzmine2.md), [OpenMS](featurebasedmolecularnetworking-with-openms.md), [MS-DIAL](featurebasedmolecularnetworking-with-ms-dial.md), [MetaboScape](featurebasedmolecularnetworking-with-metaboscape.md), and [XCMS](featurebasedmolecularnetworking-with-xcms3.md).

The main documentation for Feature-Based Molecular Networking [can be accessed here:](featurebasedmolecularnetworking.md)

The Feature-Based Molecular Networking workflow on GNPS [can be accessed here](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22FEATURE-BASED-MOLECULAR-NETWORKING%22,%22library_on_server%22:%22d.speclibs;%22%7D) (you need to be logged in GNPS first).

Below we are describing how to use MZmine2 with the FBMN workflow on GNPS.

### Citations

This work builds on the efforts of our many colleagues, please cite their work:

Röst, H. L. et al. OpenMS: a flexible open-source software platform for mass spectrometry data analysis. Nat. Methods 13, 741–748 (2016). [https://doi.org/10.1038/nmeth.3959](https://doi.org/10.1038/nmeth.3959)

Wang, M. et al. Sharing and community curation of mass spectrometry data with Global Natural Products Social Molecular Networking. Nat. Biotechnol. 34, 828–837 (2016). [https://doi.org/10.1038/nbt.3597](https://doi.org/10.1038/nbt.3597)

### Development

The GNPSExport UTIL code can be found on [OpenMS GitHub repository](https://github.com/OpenMS/OpenMS). 

The code for the Open-GNPS pipeline (ProteoSAFe workflow and python wrappers) is available on [this GitHub repository](https://github.com/Bioinformatic-squad-DorresteinLab/openms-gnps-workflow).

## Mass spectrometry processing with OpenMS

We have developed an OpenMS-GNPS pipeline that can be used for LC-MS/MS data processing with OpenMS and Feature Based Molecular Networking (FBMN) with GNPS. This pipeline uses OpenMS TOPP and required the development of the GNPSExport (OpenMS UTILS).

In brief, after running an *OpenMS "metabolomics" pipeline*, the *GNPSExport UTIL* can be used on the consensusXML file to generate files needed for FBMN on GNPS. These two files are:

- The MS2 spectral data file (.MGF format) which is generated  with the GNPSExport UTIL.
- The feature quantification table (.TXT format) which is generated with the TextExport TOOL.

### Running the OpenMS-GNPS pipeline on GNPS web-platform
The OpenMS-GNPS pipeline has been deployed on GNPS (experimental feature). The job can be configured as follow:
1. Input the mzML (prefered) or mzXML files (not recommended, because the pipeline would have to perform conversion to mzML)
2. Select the parameters from the presets (QTOF, Q-Exactive, UHPLC, HPLC). The corresponding OpenMS  configuration files (.INI files) are available from that [GitHub repository] (https://github.com/Bioinformatic-squad-DorresteinLab/openms-gnps-workflow/presets/)) 

### Running the OpenMS-GNPS pipeline 

A representative OpenMS-GNPS workflow has the following steps:
  1. Input mzML files
  
  2. Run the *FeatureFinderMetabo* tool on the mzML files.
  3. Run the *IDMapper* tool on the featureXML and mzML files.
  4. Run the *MapAlignerPoseClustering* tool on the featureXML files.
  5. Run the *MetaboliteAdductDecharger* on the featureXML files.
  6. Run the *FeatureLinkerUnlabeledKD* tool or *FeatureLinkerUnlabeledQT*, on the featureXML files and output a consensusXML file.
  8. Run the *FileFilter* on the consensusXML file to keep only consensusElements with at least MS/MS scan (peptide identification).  
  9. Run the *GNPSExport* on the "filtered consensusXML file" to export an .MGF file.
  10. Run the *TextExport* on the "filtered consensusXML file" to export an .TXT file.
  11. Upload your files to GNPS and run the Feature-Based Molecular Networking workflow. Instructions are here:
https://ccms-ucsd.github.io/GNPSDocumentation/featurebasedmolecularnetworking/

#### Requirements for OpenMS-GNPS pipeline
- The *IDMapper* has to be ran on the featureXML files, in order to associate MS2 scan(s) (peptide identification) with each features. These peptide identifications are used by the GNPSExport.
- The *FileFilter* has to be ran on the consensusXML file, prior to the GNPSExport, in order to remove consensusElements 
without MS2 scans (peptide identification).

### The GNPSExport UTILS

**Parameters for GNPSExport UTILS:**

- **Cosine Similarity Treshold** Compares the most intense annoted MS/MS spectra against all other identified MS/MS annotations and merges the MS/MS vectors.
- **Binning width** Determines the maximum distance the merged MS/MS annotations can be from the mean.

**Options for the GNPSExport spectral processing are:**

- **Most intense**: the GNPSExport will output the MS/MS scan with the highest precursor ion intensity as a representative MS/MS scan per consensusElement in the .MGF file.
- **Merge**: the GNPSExport will first merge all the MS/MS scans for a consensusElement, using the user-specified parameters (cosine score threshold, binning width), and output the merged MS/MS scan as as a representative MS/MS scan per consensusElement in the .MGF file.
**All MS/MS**: the GNPSExport will output all the MS/MS scan(s) for consensusElements in the .MGF file.
