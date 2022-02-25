## Overview

Query a single MS/MS spectrum across all public GNPS datasets in just a few seconds. This is an updated version of the traditional [MASST search](https://ccms-ucsd.github.io/GNPSDocumentation/masst/). 

## FastMASST Web Interface

Click [here](https://fastlibrarysearch.ucsd.edu/fastsearch/) for the FastMASST search interface, to get this start page:

![web_interface](https://user-images.githubusercontent.com/100324020/155648887-c5c9815d-3838-4806-89c1-6022f621d972.JPG)

## Parameters

### Spectrum Input

You can input the peaks through either the spectrum USI or manual entry. See additional information on spectrum USI [here](https://ccms-ucsd.github.io/GNPSDocumentation/usi/). 

For manual entry, the peaks input requires a peak mass per line followed by intensity, separated by a space or a tab. See a [demonstration](http://fastlibrarysearch.ucsd.edu/fastsearch/?usi1=mzspec%3AGNPS%3AGNPS-LIBRARY%3Aaccession%3ACCMSLIB00000001548&precursor_mz=299.1760&charge=1&library_select=gnpslibrary&analog_select=No&delta_mass_below=130&delta_mass_above=200&pm_tolerance=0.05&fragment_tolerance=0.05&cosine_threshold=0.7&use_peaks=1#%7B%22peaks%22%3A%20%22299.1744%5Ct2979.96%5Cn215.081%5Ct2382.46%5Cn187.0858%5Ct1273.06%5Cn241.0958%5Ct1089.87%5Cn256.119%5Ct907.52%5Cn243.1111%5Ct322.93%5Cn200.0685%5Ct198.52%5Cn100.113%5Ct168.6%5Cn170.0576%5Ct142.73%5Cn85.1002%5Ct103.75%5Cn198.0551%5Ct93.44%5Cn299.3268%5Ct91.46%5Cn94.0639%5Ct88.92%5Cn201.0788%5Ct86.23%5Cn57.0695%5Ct72.38%22%7D) input spectrum.

![image](https://user-images.githubusercontent.com/100324020/155649417-614738d2-36d2-4f41-bd92-d65fb0e2e431.png)

### Library Names

| Parameter  | Description          |
| ------------- |-------------|
| massivekb_index | ??? |
| massivedata_index | ??? |
| gnpsdata_index | ??? |
| gnpslibrary | search against the GNPS MS/MS spectra library |

### Search Options

| Parameter  | Description          | Default |
| ------------- |-------------| -----|
| PM Tolerance	| Precursor mass tolerance | 0.05 |
| Fragment Tolerance | MS2 peak tolerance | 0.05 |
| Cosine Threshold | Cosine score threshold to make a match | 0.7 |
| Analog Search | Will search data for analogs to library spectra | No |
| Delta Mass Below | Maximum mass shift between target and putative analog with lower PM | 130 |
| Delta Mass Above | Maximum mass shift between target and putative analog with higher PM | 200 |

## Results

Query results are separated into two categories, spectral match results and grouped data exploration. The top scoring match to public GNPS datasets are listed in the "Data Exploration – Match Results".

![Match_results_table](https://user-images.githubusercontent.com/100324020/155649996-3c09d7b4-d82f-4f32-86b5-34f44772a7f1.JPG)

Select the match of interest to view the spectrum mirror plots:

![Match_results_tableselection_mirrorplots](https://user-images.githubusercontent.com/100324020/155650020-34c5b4c5-b254-4a06-a558-7337aa4710fd.JPG)

![Match_results_mirrorplots](https://user-images.githubusercontent.com/100324020/155650048-b60a65db-dc9b-40a3-a39b-ac7d32ea6c2a.JPG)

The “Grouped Data” allows you to categorize the distributions of all the spectra matches based on delta mass, dataset, adduct form, or compound name.

![image](https://user-images.githubusercontent.com/100324020/155650162-b27478cc-f85a-4976-b1b6-c8edd78e97aa.png)

## Citation

!!! cite "Recommended Citation"
	[Wang, M., Jarmusch, A.K., Vargas, F. et al. Mass spectrometry searches using MASST. Nat Biotechnol (2020) doi:10.1038/s41587-019-0375-9](https://www.nature.com/articles/s41587-019-0375-9)


## Page Contributions

{{ git_page_authors }}
