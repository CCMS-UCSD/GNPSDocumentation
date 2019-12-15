# Ion Identity Networking (IIN)

## Introduction

The Ion Identity Networking (IIN) workflow complements the [Feature-Based Molecular Networking (FBMN)](featurebasedmolecularnetworking.md) by grouping MS2 spectra not only 
through similarity of MS2 spectra, but also of MS2 spectra whose precursor ions fulfill the retention time, peak shape, user-defined. It enables the visualization of patterns of ion species and brings together subnetwork from the same molecule to create an ion identity molecular family.

## Running the IIN workflow

The Ion Identity Networking workflow is run throught the [FBMN workflow](featurebasedmolecularnetworking.md) by providing Supplementary Annotation/Pairs files in the "Advanced Extras" panel of the standard [FBMN workflow interface](featurebasedmolecularnetworking.md).

![img](img/iin/iin_supplementary_pairs.png)

Alternatively, the [quickstart interface for FBMN ](https://gnps-quickstart.ucsd.edu/featurebasednetworking) can also be used:

![img](img/iin/quickstart_iin_clear.png)

Note that multiple Supplementary Pairs files can specified. Their content will be added.

## Generating Supplementary Pairs

The Supplementary Annotations/Pairs files can be generated with the following software:

- **MZmine**: [See the documentation](fbmn-iin-mzmine.md)
- **XCMS-CAMERA**: [See the documentation](fbmn-iin-xcms.md)
- **MS-DIAL**: [See the documentation](fbmn-iin-msdial.md)

Alternatively, the results of other software could be used as long as the LC-MS feature identifier (ID) matches the "SCANS=" number in the MGF file.

#### Supplementary pairs

The Supplementary Pairs is a .CSV format file (coma separated), and must contains the following columns:

| Header        | Description |
| ------------- |-------------|
| ID1 | Node ID 1 matching the row IDs |
| ID2 | Node ID 2 matching the row IDs |
| EdgeType | Any string describing the type of edge |
| Score | A numerical value for the score (cannot be empty) |
| Annotation | A string annotation |

See an example of the Supplementary Pairs used in the Ion Identity Networking (IIN) workflow

![img](img/featurebasedmolecularnetworking/fbmn_iin_edges.PNG)


## Exploring the IIN workflow in Cytoscape

## TO DO NOTES
- Cytoscape documentation
- Poiting

## Page contributors
Robin Schmid (WWU, Münster, Germany), Daniel Petras (UCSD), Louis Felix Nothias (UCSD), Ming Wang (UCSD).