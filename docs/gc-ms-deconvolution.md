# GC-MS Deconvolution for GNPS

The GC-MS data have to be processed before performing the **spectral library search and molecular networking workflow**. [See more information here](gc-ms-library-molecular-network.md). Here it is described how to use the GC-MS deconvolution workflow on GNPS based on MSHub algorithm. Alternatively, any other tools such as MZmine/ADAP or MS-DIAL can be used and output of those tools analyzed using the library search workflow.

The MSHub algorithm in this workflow auto-estimates all of the deconvolution settings (although it is possible for user to manually override the auto settings). This user-independent parameter optimization is accomplished via fast Fourier transform, multiplication and inverse Fourier transform for each ion across entire data sets followed by unsupervised neural network matrix factorization. 

MSHub conducts deconvolution on all files in the dataset at once to utilize all of the information of spectral patterns present in the data. As machine learning approaches rely on sufficiently comprehensive training data for optimal performance, MSHub deconvolution gives the best results when more files are included into analysis. In the scenario that the user only has a few files, (less than 10), it is encouraged to perform spectral deconvolution using MZmine, MSDial, XCMS or other spectral deconvolution tools. The molecular networking can be performed in the same fashion, as described in the **spectral library search and molecular networking workflow** portion of the tutorial: [See more information here](gc-ms-library-molecular-network.md). 

The reproducibility of spectral patterns for each spectral feature deconvolved across the entire data set can then be summarized as a parameter termed “balance score”.  Balance score is a new quality metric that only exists for dataset-wide deconvolution, and it gives insight into how well the spectral feature is explained across the data: when it is high, it means that the spectrum is consistent across different samples (no missing peaks of spurious noise peaks). The spectral patterns that are consistent across samples, even if only a few samples in the data contain them, would result in a high value of the balance score. Applying balance score threshold allows eliminating spurious features that are likely to be noise .




## GC-MS Deconvolution Workflow on GNPS with MS-Hub


### Configure the Workflow
Log in to GNPS  ([gnps.ucsd.edu](https://gnps.ucsd.edu/ProteoSAFe/static/gnps-splash.jsp)). If an account has to be created first, refer to GNPS documentation at the [quickstart](https://ccms-ucsd.github.io/GNPSDocumentation/quickstart/) banner. Before starting, files from GC-MS analysis must be converted from proprietary vendor formats to .mzML, or .CDF file formats. To convert, please see our [conversion guide](https://ccms-ucsd.github.io/GNPSDocumentation/fileconversion/). 

The GNPS home page includes two sections to launch GNPS GC-MS data analysis job, one for data processing - deconvolution and one for GC-MS library search/networking. By clicking on the **“Process Raw GC-MS data” icon**, a job page opens.

![img](img/GC-MS_documentation/Fig_1A.png)

(1) Start by entering the title of your job. 

(2) The **“Select Files” section** allows importing existing or previously uploaded dataset(s) from MassIVE. Select the files that need to be processed by clicking on “Select Input Files”. A pop-up window appears with three tabs: “Select Input Files”, “Upload Files”, and “Share Files”. To upload files to GNPS using the browser (limited to 20MB), you can use our web drag and drop uploader in the “Upload Files” banner. See the documentation [here](https://ccms-ucsd.github.io/GNPSDocumentation/fileupload/) for more information. 

(3) Readers following the tutorial can go to the “Share Files” tab, enter the MassIVE accession number for the dataset (e.g. [MSV000084226](https://gnps.ucsd.edu/ProteoSAFe/result.jsp?task=671cd79ac3af4c4493e4025d62d161e1&view=advanced_view)) in the “Import Data Share” box.

(4) Then click on “Import”. 

(5) This specific dataset is now available directly in your GNPS user workspace at the “Select Input Files” section. 

(6) Select the input file, who appears highlighted in blue color, and click on “Spectrum files”. 

(7) When the selected files are visible in the “Selected Spectrum Files” box, click on the “Finish Selection” button.

![img](img/GC-MS_documentation/Fig_2.png)

**NOTE:** 

- All of the data used for the job must be collected using the same GC protocol (temperature program, column, injection mode). Multiple datasets could be combined as long as the data have been collected using the same protocol. 
- When creating a dataset on MassIVE ([massive.ucsd.edu](https://massive.ucsd.edu/ProteoSAFe/static/massive.jsp)), include “GNPS” and “GC” in the name (As GNPS_GC_Name of the GNPS-MassIVE dataset). See the documentation about [Dataset Creation/Sharing](https://ccms-ucsd.github.io/GNPSDocumentation/datasets/) and an example of a MassIVE dataset [MSV000084226](https://gnps.ucsd.edu/ProteoSAFe/result.jsp?task=671cd79ac3af4c4493e4025d62d161e1&view=advanced_view) for more information.
- An insufficient volume of data causes unstable deconvolution resulting in spurious low-quality spectra. It is recommended for datasets smaller than ~10 files to use alternative deconvolution solutions such as MZMine2/ADAP, MS-Dial or XCMS. Increasing the number of files, for example, could be done by co-analyzing multiple datasets obtained with the same experimental protocol. 



The **“Advanced MSHub Processing” section** displays some automatic setting parameters (related to peak symmetry and baseline adjustment) determined internally by MSHub. The user does not need to provide settings, although they can be set manually, should the user choose to do so. 

(8) In the **“Advanced Clustering” section**, the cluster spectra have to be turned off (CLUSTER_SPECTRA = NO). The TIME_UNIT must be set as minutes or seconds, depending on the chromatography time units of your data (typically the default time units are seconds in NetCDF files and minutes in .mzML files). 

(9) Enter your email address.

(10) Finish by clicking “Submit”.

![img](img/GC-MS_documentation/Fig_3.png)

### Inspect the Results

The analysis is linear with the number of files and scales as ~1 minute per file. The analysis time may vary depending on the cluster job load during peak vs. off-peak hours. When the job has been completed, you will receive a notification email and the status “DONE” appears on your GNPS job. All submitted jobs appear under the “jobs” link from the GNPS main menu. 

![img](img/GC-MS_documentation/Fig_4.png)

By selecting the job of interest and clicking on the “Done” button, the **“Job Status” window** opens with different options:

(i) Explore deconvolution results with the “View All Deconvolved Spectra” option.

(ii) Download/export quantification results and feature table by clicking on “Download Spectra as MGF”, “Download Feature Table” (MZmine formatted), "Download MSHub Data Integral Table", or "Download MSHub Spectra Data".

(iii) Continue the process with the “Search Spectral Library and Molecular Network” tool to conduct a library search and create a molecular network.

![img](img/GC-MS_documentation/Fig_5.png)

The first line of the MSHub data integral table indicates the retention time (in min.) with a balance score in parenthesis (in percentage). The “Rel. Max Integral” and “Sample\Best order” values relate to the relative proportion of each peak in the data and the ranking of the feature in terms of its size, correspondingly.

![img](img/GC-MS_documentation/Fig_6.png)

The feature table is formatted as a MZmine table output. 

![img](img/GC-MS_documentation/Fig_6B.png)



## GC-MS data processing with ADAP-MZmine

[to be completed]

## GC-MS data processing with MS-DIAL
[to be completed]

## Page contributors
Alexander Aksenov (UCSD), Melissa Nothias-Esposito (UCSD), Mabel C. Gonzales (UCSD), Louis Felix Nothias (UCSD).
