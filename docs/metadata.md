# Metadata

## Summary
The metadata file used in GNPS describes the properties of a file (*e.g.* sample type, year of analysis, and collection method). Metadata adhering to the accepted formatting for each tool enhances data analysis and visualization options. We strongly encourage you to prepare metadata files in advance and [upload](https://mwang87.github.io/ReDU-MS2-Documentation/HowtoContribute/) to the supplementary file folder in the corresponding MassIVE dataset.

## Format
The recommended starting point is the [ReDU Sample Information Template](https://docs.google.com/spreadsheets/d/1v71bnUd8fiXX51zuZIUAvYETWmpwFQj-M3mu4CNsHBU/edit?usp=sharing) (additional documentation can be found [here](https://mwang87.github.io/ReDU-MS2-Documentation/HowtoContribute/)). Users can add an unlimited amount of additional columns to the ReDU Sample Information Template. There are specific instructions on required columns and formatting detailed for GNPS tools below.

Metadata file used must be a tab-delimited text file. A .tsv can be downloaded from the ReDU Sample Information Template. Users that create a metadata file without using the ReDU Sample Information Template using a text editor (e.g. Microsoft Excel, Notepad++ for Windows, gedit for Linux, TextWrangler for Mac OS) should save as a .txt (tab-delimited). 

!!! warning
  Excel (xlsx), rich text (rtf) are not supported.

**Example metadata file without using the ReDU Sample Information Template**
[Right-click, and Save link as](https://raw.githubusercontent.com/DorresteinLaboratory/GNPS-Trinity/master/GNPS-Trinity_template_files/metadata_GNPS_AMG_demo.txt) to download. A text editor can be used to edit it as desired. 

!!! note 
  The only required columns in the metadata is **"filename"** and the file names should match those uploaded to MassIVE.    **Capitalization matters.**

## Requirements Specific to Molecular Networking
The use of a metadata file is an alternative way to assign groups when selecting data input files within the workflow of GNPS. The current version of molecular networking allows to use the metadata table as an input. 
!!! tip
  Indicate which metadata columns should be considered in analysis by opening the file in a text editor and adding             "ATTRIBUTE_" to the header of the column.
* Save the file (must be tab-delimited text file)
* Users must upload their data file
* Users must select the metadata file and place it in the **"Metadata File"** folder

!!! note 
  Although it is possible to use the legacy group mapping and attribute mapping file, we strongly advise against using this   method.

## Requirements Specific to Qiime2
GNPS communicates with Qiime2. PCoA visualized using EMPeror and Qiime outputs (.qza/.qzv), including a BIOM formated output, can be generated. Microbe-metabolite interactions can also be studied with [MMVEC](https://www.nature.com/articles/s41592-019-0616-3). GNPS will parse any extra column in the metadata file and output them in the Qiime2 supported files (BIOM/qza files). Note that by default the mass spectrometry filename will be used as sample name for Qiime2 files. Alternatively, it is possible to specify an additional metada column called "sample_name" that will be used instead as sample name in Qiime2, to enable joint mass spectrometry - metabolomics analysis such as MMVEC.

* Save the file (must be tab-delimited text file)
* Users must upload their data file
* Users must select the metadata file and place it in the **"Metadata File"** folder
* **Optional** Add an extra column called "sample_name" to the metadata file using a text editor. The sample name will replaced the mass spectrometry filename in the Qiime2 output. For joint mass spectrometry - sequencing analysis with MMVEC, provide the sequencing sample name as indicated in the qiime2 file used (BIOM/qza file).

## Requirements Specific to Qiita
GNPS communicates with Qiita. Specifically, you can use the output of GNPS to add metabolomics data into an existing Qiita dataset. This is handled through the Biom table output as a qiime2 qza artifact. The key feature is renaming the mass spectrometry file into a sample identifier so that the identifiers are concordant. **Note: a Qiita ID with corresponding information must be created**

* **Add an extra column called "sample_name" to the metadata file using a text editor.** The identifer must contain the Qiita ID prepended to the sample identifier using a period (*e.g.* 10317.000096815).

* Save the file (must be tab-delimited text file)
* Users must upload their data file
* Users must select the metadata file and place it in the **"Metadata File"** folder

**Note:** if performing additional analysis in Qiime using the .qza it is required to add a row indicating the type of variable.


## Requirements Specific to 'ili
The metadata can also be used to specify spatial coordinates for direct visualization of the data in ['ili toolbox](https://ili.embl.de/). It creates really cool plots like this:
![ili_example](img/networking/ili_example.png)
* **Extra columns are required in the metadata file** A text editor should be used to add the following columns in order (required):
1. "COORDINATE_X" - X coordinate on the 2D/3D model
2. "COORDINATE_Y" - Y coordinate on the 2D/3D model
3. "COORDINATE_Z" - Z coordinate on the 2D/3D model
4. "COORDINATE_radius" - radius for the spot in 'ili toolbox.
**"filename" must be the first column
![ili](img/networking/ili-table.png)

* Save the file (must be tab-delimited text file)
* Users must upload their data file
* Users must select the metadata file and place it in the **"Metadata File"** folder
* Users must upload the corresponding .STL file and place it in the **"STL Model for ili"** folder

## Page Contributions
Alan K. Jarmusch, Louis Felix Nothias (UCSD)
