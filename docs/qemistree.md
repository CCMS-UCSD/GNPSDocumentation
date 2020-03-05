QEMISTREE – in silico tool to build a tree of molecules and annotate by chemical taxonomy
 
Introduction: Qemistree is a computation tool to build a tree of mass-spectrometry (LC-MS/MS) features to perform a chemically-informed comparison of untargeted metabolomic profiles. 
 
**STEP 1: Collecting the right input files**

Running a QEMISTREE job in GNPS requires 4 input files which can be generated using a combination of LC-MS/MS processing software [MZmine](https://ccms-ucsd.github.io/GNPSDocumentation/featurebasedmolecularnetworking-with-mzmine2/) and [Feature-Based Molecular Networking](https://ccms-ucsd.github.io/GNPSDocumentation/featurebasedmolecularnetworking/). The files are:

Required: A SIRIUS file generated from the MZmine workflow
Required: A quant table called `qiime2_table` with all the features which can be downloaded from a processed FBMN job (found in folder qiime2_output)
Optional: A metadata file called `qiime2_metadata` which can also be downloaded from a processed FBMN job (also found in folder qiime2_output)
Optional: A library identification file (tsv) which can also be downloaded from a processed FBMN job (found in folder `DB_result`)

Follow the steps below to generate the files:

a. Follow the documentation for [Feature-Based Molecular Networking using MZmine2](https://ccms-ucsd.github.io/GNPSDocumentation/featurebasedmolecularnetworking-with-mzmine2/) to generate an aligned feature list for your LC-MS/MS data and export the necessary mgf and csv files for FBMN in GNPS.\
b. While still in MZmine2, select your aligned feature list, then click on the tab for Feature list methods and select Export/Import, followed by Export for SIRIUS.\
c. Choose the Mass list that you used to generate your feature list, and specify a path and Filename for your SIRIUS file. Click OK.\
d. Go to GNPS server and run an [FBMN](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22FEATURE-BASED-MOLECULAR-NETWORKING%22,%22library_on_server%22:%22d.speclibs;%22%7D) job using the GNPS quant csv, GNPS mgf (both generated in step a, above) and [ReDU](https://mwang87.github.io/ReDU-MS2-Documentation/HowtoContribute/) metadata file\
e. Once completed, go to the status page and click on the button Download qiime2 Emperor qzv\
f. In the downloaded folder, go to `qiime2_output` for the files `qiime2_table.qza` and `qiime2_metadata.tsv` and to `DB_result` for the tsv file within.
        	
 
**STEP 2: Running a Qemistree job**

 
a. Go to the [Proteomics2](https://proteomics2.ucsd.edu/ProteoSAFe/index.jsp) server and select the QEMISTREE from the dropdown menu called workflow\

b. In the input section add the following files:

1. SIRIUS file for the Spectrum files
2. qiime2_table for quant_table
3. qiime2_metadata for metadata_table
4. DB_result file for library_identifications

c. Under the header, Advanced options select the instrument type (orbitrap or Q-tof). If you are signed in to the server the email address will auto-populate. If not, add your email address and click on submit. The runtime depends on the number of features in your dataset -- a typical dataset (few thousand features) will take a few hours.

**STEP 3: Analysing the results from a Qemistree job**

Once the job is finished successfully, you will be able to see the status page as below. Here, go to the View Summary page. This page tabulates the annotations for all features for which molecular fingerprints could be predicted using Sirius and CSI:FingerID (Dührkop et. al). Click on the download button to download the output files for downstream analyses and visualization.



In the downloaded folder, the `output_folder ` has several data files. The qemistree.qza and qemistree-pruned.qza are tree files that can be uploaded to [iTOL](https://itol.embl.de/upload.cgi) to visualize the features and how they are related to one another. The qemistree.qza file contains all the features with molecular fingerprints, including those that were not annotated either using MS2 fragmentation (spectral library match) or Sirius+CSI:FingerID (in silico). It may, therefore, be useful to prune the tree for visualizations purposes and keep only the annotated features. By default, the workflow outputs `qemistree-pruned.qza`  which contains the features that were annotated up  to class level by ClassyFire (Djoumbou et. al.).

Here are the output files you need for the downstream steps:

1. classified_feature_data.qza
2. merged_feature_table.qza
3. qemistree-pruned.qza
4. qemistree.qza

**STEP 4: Annotating Qemistree in QIIME2**

Qemistree supports the classification of the features/molecules based on chemical taxonomy such as kingdom, superclass, class, subclass, direct_parent, and smiles.  Python scripts written in the QIIME 2 environment for the Qemistree program can be used to annotate the leaves based on classified chemical taxonomy. To use the python scripts, QIIME2 has to be installed on your computer. This can be done using the documentation [here](https://docs.qiime2.org/2019.10/install/). 
Once QIIME 2 is installed, activate your QIIME 2 environment and install q2-qemistree following the steps below:

```bash
git clone https://github.com/biocore/q2-qemistree.git
cd q2-qemistree
pip install .
qiime dev refresh-cache
```

For subsequent sessions, use the command conda activate qiime2-2019.10  to activate QIIME2 environment.

The python script used to enhance the visualization of the tree in iTOL is called _itol_metadata.py and is included in the q2-qemistree package. The following command is used to generate a color and a label file at the desired taxonomy level:
Make sure to provide the path to _itol_metadata.py  unless already in the q2-qemistree/q2_qemistree folder

```bash
python _itol_metadata.py \
  --classified-feature-data classified-feature-data.qza \
  --feature-data-column subclass \
  --ms2-label False \
  --color-file-path /path-to-clade-colors-file.txt/ \
  --label-file-path /path-to-tip-label-files.txt/
  ```

Both the path-to-clade-colors-file.txt and path-to-tip-label-files.txt files can be dragged and dropped on the iTOL website after the tree file has been uploaded.
In addition, you can also compare the frequency of each tip (i.e. feature) across a user-defined  metadata category. The following command can be used to generate bar charts at the tips of the tree specifying the prevalence of the feature in particular metadata category:
You will need the metadata file (`qiime2_metadata.tsv` for `metadata.tsv` below) from the FBMN job (typically in the qiime2_output folder).

```bash
python _itol_metadata.py \
  --classified-feature-data classified-feature-data.qza \
  --feature-data-column subclass \
  --feature-table merged-feature-table.qza \
  --sample-metadata metadata.tsv \
  --sample-metadata-column groups \
  --barchart-file-path /path-to-barchart-subclass-file.qza/
```

Generating the final output:
As described above, you need 4 files to visualize the tree in iTOL: a tree file (.qza extension), a clade color file (.txt extension), a tip label file (.txt extension) and a bar chart file (.qza extension). Then follow the step below:

1. Go to the [iTOL](https://itol.embl.de/upload.cgi) website (Letunic et al). Enter desired tree name, tree text. Upload the qemistree.qza (or qemistree-pruned.qza file pruned at the desired taxonomy).
2. Drag and drop the clade color file (.txt) and tip label file (.txt)
3. Drag and drop the bar chart file (.qza)

CITATIONS:

[Dührkop, K., Shen, H., Meusel, M., Rousu, J. & Böcker, S. Searching molecular structure databases with tandem mass spectra using CSI:FingerID. Proc. Natl. Acad. Sci. U. S. A. 112, 12580–5 (2015)](https://www.pnas.org/content/112/41/12580)

[Djoumbou Feunang, Y. et al. ClassyFire: automated chemical classification with a comprehensive, computable taxonomy. J. Cheminform. 8, 61 (2016)](https://jcheminf.biomedcentral.com/articles/10.1186/s13321-016-0174-y)

[Letunic, I. & Bork, P. Interactive Tree Of Life (iTOL) v4: recent updates and new developments. Nucleic Acids Research vol. 47 W256–W259 (2019)](https://academic.oup.com/nar/article/47/W1/W256/5424068)
