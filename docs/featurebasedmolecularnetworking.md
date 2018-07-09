
The Feature Finding Molecular Networking brings together LC-MS feature detection tools (e.g. MZmine2, OpenMS, MS-DIAL, MetaboScape), molecular networking (GNPS, http://gnps.ucsd.edu), and other in silico annotation tools, such as Sirius, CSI:FingerID, or Network Annotation Propagation.

The key improvements of the new Feature Finding Molecular Networking are:

1. Importing information derived from the feature detection tools into the molecular networks
2. Discriminate isomers by retention time and remove isotopic peak
3. Allows the annotation MS/MS of spectra with in silico tools and mapping in the molecular networks

## Feature Detection

In summary, these tools have been adapted by providing an .MGF export module for the result of LC-MS/MS feature detection.

1. The data have to be processed as recommended by the developers.
2. The spectral data from the aligned data can be exported as .MGF, the aligned quantification table has to be exported as well.
3. The .MGF file can be used as input for any GNPS tools. The aligned quantification table can be imported into Cytoscape.
3. The metadata table groups can be generated automatically with a dedicated workflow for MZmine2, or post-processed with other solutions (Jupyter notebooks, excel).

Currently, we are recommending using the MZmine2 workflow, as it has been thoroughly tested. See the documentation below.

### Mass spectrometry data Feature Detection with MZmine2

Download MZmine2 software (version MZmine v2.30 minimum) at [https://github.com/mzmine/mzmine2/releases](https://github.com/mzmine/mzmine2/releases).

See documentation and videos here: [http://mzmine.github.io/documentation.html](http://mzmine.github.io/documentation.html).

Please make sure your files are converted to mzXML or mzML.

#### MZMine Batch Steps

In MZmine2, a sequence of steps must be performed. The following batch method (.XML format) can be downloaded (temporary email nothias@ucsd.edu ) and imported into MZmine2.


### Citation

This work builds on the efforts of our many colleagues, please check out their work:

[MZmine 2 Data-Preprocessing To Enhance Molecular Networking Reliability. Olivon et al.](https://pubs.acs.org/doi/10.1021/acs.analchem.7b01563)

[MZmine 2: Modular framework for processing, visualizing, and analyzing mass spectrometry-based molecular profile data. Pluskal et. al.](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-11-395)
