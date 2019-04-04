# Feature-based molecular networking in Cytoscape

Cytoscape is an open source software platform used to visualize, analyze and annotate molecular networks from GNPS. Cytoscape is available for download from [here](https://cytoscape.org/). The instructions below assume that you have installed Cytoscape 3.7.

Shannon, P., Markiel, A., Ozier, O., Baliga, N. S., Wang, J. T., Ramage, D., . . . Ideker, T. (2003). Cytoscape: a software environment for integrated models of biomolecular interaction networks. Genome Res, 13(11), 2498-2504. doi:10.1101/gr.1239303

## Downloading Cytoscape Files from GNPS

The first step is to download the input file (.graphML file format) for import into Cytoscape. From the job status page in the Feature-Based Molecular Networking workflow, you will need to click on “Download Cytoscape Data”. Save and unzip the exported file.  

Unzip the downloaded folder files. The content will look like this:

## Importing Files from GNPS to Cytoscape

To import the file into Cytoscape, open it, click on “Import Network from File System” and then choose the “.graphml” file.  The imported network takes place in the main window. In the “Control Panel” at the “Network” tab, by a right click on the network, the “Rename Network” option can be used. 

## Rotation of the network
To rotate the entire network choose the tab “Layout” and click on “Node Layout tool”. In the opened window, unclick the box “Selected Only” to rotate the entire network and move the blue bar to 90. You can also select specific subnetworks and rotate them by clicking the box “Selected only”.

## Table panel visualization data
To enhance networking data analysis and exploration in Cytoscape, you may click on “Table Panel” and select network information such as name, “Compound_name” (name of the spectral library match), “parent mass” (precursor ion mass), ”RTconsensus” (retention time for the node), MZErrorPPM (“ppm error with the spectral library match) and Attributes of interest in your metadata table.

## Create a new style
A style can be created by clicking on "Create New Style" and a style name can be specified (e.g. High vs Low Plant Consumer). The crated style can be exported by going in the main menu at “File”, “Export” and “Styles to File”, or can be imported by clicking on “Import” then “Style From File” in the “File” section. 

## Node Styling

### Label
Through the “Control Panel”, go to the “Style” tab. Within the “Node” menu, you will be able to apply many parameters such as to label each node. You can choose the “Precursor mass” as node label for the networks generated using GNPS. Additionally, you need to select  “Passthrough Mapping” as the Mapping Type. Go to “Properties” to add more options. 

### Pie charts
If you have groups defined in your metadata file, you can visualize the summed or the meaned intensities from the MS1 feature table of these groups in pie charts for every node (Note: the mean/sum option is specified in the GNPS job). To make pie charts representing the summed feature intensity of the groups click on the left box of “Image/Chart1”. Choose the Pie Chart Icon and select the columns of groups you are interested in visualizing (e.g. GNPSGROUP: Less_than 5 (low plant consumers) and GNPSGROUP:More_than_30 (high plant consumers)). Click on “Options” (below “Data”) to choose colors for the Groups (numerized 1. And 2. According to the field “Selected Columns” in “ Data”). Click “Apply” when you finished. 

### Size
In “Style” panel, at Size option, select “sum(precursor intensity)” or “number of spectrum” as Column and “Continuous Mapping” as Mapping Type. The opened window allows to modify the node size in function of the parameter chosen for the column. Begin by “Set Min and Max”, and if necessary, click on “Add” to addition some nuances. 

## Edge Styling
### Width
To aid in the visualization of individual node relatedness within a cluster, the cosine score is used. Cosine scores define similarity between two MS/MS spectra. Scores ranging from 0 (totally dissimilar) to 1 (completely identical). This value will determine the thickness of the edge between related nodes. Again working within the “Style” Tab, select the “Edge” menu. From the “Width” drop down menu, select “cosine_score” for the Column and “Continuous Mapping” for the Mapping Type. Double click on the “Continuous Mapping” area of the menu to adjust the thickness of the edge. Click OK to apply the setting changes.

## Filtering nodes with Select tool

### Toolbar
Use Cytoscape’s toolbar for searching nodes (e.g., “shared name”).

### Select
Go to the “Control Panel” and click on “Select” tab. This tool can be used to create a selection of nodes and/or edges. At the top of “Select” panel appears the active filter name. To rename, remove, create a new filter, or other options , go on the button beside the select panel. Then, click on the “+” button and choose between column, degree, or topology filter to add an arbitrary number of sub-filters. The “x” button aims to delete sub-filter. For each sub-filters, the option “is” and “is not” for numeric column, or “contains” and “does not contain” for string column can be choosen. Here, we create “annotation filter” who select nodes with “MZErrorPPM” from 0 to 10. Click “Apply” and see just below the note that says how many nodes and edges are selected (160 nodes and 0 edges). A yellow circle surrounds the selected nodes by the filter.
For more details and options, follow this [link](http://manual.cytoscape.org/en/stable/Finding_and_Filtering_Nodes_and_Edges.html#filters).

## Bypass mode
A bypass could be applied on the previously selected nodes and/or edged by selecting in the  “Style” panel, the “Byp.” column for each option you want to change like “Border paint” and “Border Width” for example. For removing or set it, click right and choose “Remove Bypass” or “set Bypass” option. 

## Drawing structure in nodes

The first step consisting in the installation of a bioinformatics plugin for Cytoscape named chemViz2. To do that, in the main menu, go to “Apps” tab then open “App Manager...”. Through “Install Apps” click “chemViz2” then install it by clicking “Install” button. For more information about chemViz2, refer to the information available in the following [website link](http://www.cgl.ucsf.edu/cytoscape/chemViz/)

On “Apps” again, go to “Cheminformatics Tools” and click “Setting...”. Trough “Attribute Settings”, choose the “ Smile Attribute”  or the “InCHI Attribute” you need by clicking “node.Smiles” or “node.INCHI”, respectively, and apply it by clicking “OK” button. 

Finally, to draw structures in nodes, return to “Apps” and “Cheminformatics Tools” to go to “Paint Structures” and select “on all nodes” or “on selected nodes”. Visualize the results.




##### Below is the schematic representation of the LC-MS/MS data processing steps with MZmine2:

![complete workflow view](img/mzmine/Workflow_mzmine.png)


##### Below is the overview of the LC-MS/MS data processing steps in the MZmine2 batch mode:

![img](img/mzmine/batch_overview.png)

#### Batch Import

Here are some MZmine2 batch that are compatible with the Feature-Based Molecular Networking workflow. These batch files can be imported into MZMine2 (Batch mode):

| Instrument  | Gradient Length | Matrix Type | Sample Size | Download |
| ------------- |-------------| ----- | ----- | ----- |
| Bruker Maxis HD qTof | 10 Min | Stool | 20 | [Batch](static/maxis_12min_stool_20.xml) |


<!-- The prototype batch method for Bruker Maxis HD qTof can be [downloaded](static/qtof_batch.xml) and imported into MZmine2. -->

