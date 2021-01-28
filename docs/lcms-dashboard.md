# LCMS Dashboard

Pardon our dust, this is a work in progress!

Help us by adding to it. 

This LCMS Dashboard Interface is designed to enable easy visualization of mass spectrometry data files directly in the browser. Broadly the data can come from the following sources:

1. MassIVE Public Datasets
1. GNPS Public Datasets
1. Metabolights Public Datasets
1. Metabolomics Workbench Public Datasets
1. GNPS Analysis Data Files (LC and GC)
1. PRIDE Proteomics Public Datasets
1. ProteomXchange Public Datasets

We aim to enable the visualization without having users download a single file and to easy share visualizations as a url with all settings preserved and saved. The high level capabilities are:

1. 2D mz vs RT Heatmap
1. XIC/EIC Plots of single and multiple files
1. TIC Plots of single and multiple files
1. Box Plots of XIC/EIC integration between two cohorts of samples
1. Interactive Feature Finding with MZmine2 and Dinosaur
1. Visualization of MS1/MS2 spectra within mass spec files

## Selecting Input Data

### Supported Input Data File Types

1. mzML
1. mzXML
1. CDF
1. Thermo RAW

## 2D m/z RT Heatmap

Lorem Ipsum

## XIC/EIC Plots
Obtain single or multiple XIC/EIC plots for one or more files

!!! note
    Default integration type is AUC but options MS1 Sum or MAXPEAKHEIGHT exist under XIC Integration Type dropdown menu
1. Drag and drop files or input USI links
1. Specify m/z or multiple m/z separated by ";" under XIC Options
1. Export or view your XIC values under XIC Integration  
1. Share or save your work by clicking "Link to these plots" or copy the link address 


## TIC Plots

For every LCMS File that is selected, the LCMS Viewer shows the total ion current for the entire LCMS run. Here we have the option of choosing the sum (TIC) or base peak intensity (BPI). 

TODO: Add image for selection here

!!! note 'Multiple TIC for multiple files'
    This is possible by turning on the multiple TIC option. 

## Box Plots

Lorem Ipsum

## Integrated Feature Finding

Lorem Ipsum

## Sharing Visualizations

Lorem Ipsum


## Collaborative Visualization

You can share visualizations as URLs and interactively Collaborate. There are several ways to collaboratively view data:

1. Visualize data and send others the visualization link
2. Creating a session where you may lead and others may follow (mirror) your activity

### Sychronized Leader/Follow Visualization

To create a visualization as a leader, you will need to do the following

1. Click on Sychronization Options
1. Create a session id, this can be anything, random numbers or your name/class
1. Select Under Teaching Sychronization (Beta), select LEADER
1. Click Get Token (this protects your session so others cannot hijack being leader)
1. Copy the link under "Follower URL" and send to others to follow your work

To initiate following a visualization, you will need to do the following

1. Get a follower URL from your collaborator who will function as the leader
1. Click "Sync Initiate"
1. Watch for updates from your leader

You may also stop syncing as a follower by clicking the "Sync Terminate" so that you do not receive any more updates. Then you may build upon the visualiation that has been done by the leader. 

### Teaching Mass Spectrometry Data/Analysis

We think this tool might be a good tool for teaching LC/MS visualization. The Leader/Follower options are a way for students to follow along to get started. Once the initial setup and instruction are done, they can stop syncing and build upon the visualization. We have tested this tool to scale up to a few dozen concurrent followers. If you do intend to use this for a class, please let us know so that we do not do maintenance during your class. 

## Repositories Supported

1. MassIVE Public Datasets
1. GNPS Public Datasets
1. Metabolights Public Datasets
1. Metabolomics Workbench Public Datasets
1. GNPS Analysis Data Files (LC and GC)
1. PRIDE Proteomics Public Datasets
1. ProteomXchange Public Datasets

!!! note
    To get a file list for a dataset, checkout out [GNPS Dataset Explorer Tool](https://gnps-dataset-explorer.herokuapp.com/). 
