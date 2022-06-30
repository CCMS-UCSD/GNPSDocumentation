# Community Curated MS/MS Spectral Libraries

GNPS provides a platform for users to contribute their own annotated MS/MS spectra to the spectral libraries. There are several requirements for annotation: 1) the compound must be of known structure and 2) the MS/MS must be of sufficient quality to support the annotation of the compound. By contributing these spectra, users will expand the spectral libraries and allow dereplication of these compounds within other datasets.

## Library Quality Level

The spectral libraries are categorized based upon quality of the data. The level indicates both the quality of the MS/MS spectra as well as the trust worthiness of the annotations. These reflect both quality of the MS/MS spectra as well as the trust worthiness of the annotations.

|     Quality Level    | Description          | Quality Number |
| ------------- |-------------| -----|
| Gold :star: | Synthetic, Complete structural characterization with NMR, crystallography or other standard methods as defined in the publication guidelines for Journal of Natural Products, Privileged users | 1 |
| Silver | Isolated or lysate/crude, Published data showing presence of molecule in the sample | 2 |
| Bronze | Any other putative, complete or partial annotation | 3 |
| Challenge :muscle: | Unknown Identity, open to community to help annotate | 10 |

By default, users will have access to Bronze, but approval is required to contribute to silver and gold libraries. To obtain training and access please email [Mingxun Wang](mailto:mingxun.wang@cs.ucr.edu).

## Adding Single Spectra

### Input Formats

mzXML, mzML, and mgf file formats are accepted.

Additionally, spectra to be added to the library should be centroided. Profile data is not processed correctly by our algorithms. If you are unsure of how to convert spectra to these formats, please checkout the documentation [here](fileconversion.md).

### Adding Spectrum

From the [GNPS Splash Page](https://gnps.ucsd.edu/ProteoSAFe/static/gnps-splash.jsp), users can click on

![img](img/libraries/add_selection.png)

to be brought to the Add Single Annotated Spectrum workflow. By default, users will contribute bronze quality reference spectra. Permission is required to contribute higher quality spectra to the gold and silver workflows.

Select an input spectrum file.

!!! note
	Do not change the spectral library that is selected.

### Annotation Fields

For a full set of parameters, see [this](batchupload.md#field-information)

**Sample Parameters**

|     Field    | Description          | Default |  Required |
| ------------- |-------------| -----| ------- |
| Ion Source | Source of Ions | LC-ESI | Yes |
| Instrument | Mass Analyzer | qTof | Yes |
| Ion Mode | Ionization Mode | Positive | Yes |
| Compound Source | Sample source of compound | Commercial | Yes |
| Principle Investigator | PI overseeing compound acquisition and analysis | N/A | Yes |
| Data Collector | Individual Collecting Data | N/A | Yes |

**Annotation**

|     Field    | Description          | Default |  Required |
| ------------- |-------------| -----| ------- |
| Scan | Spectrum Scan of Spectrum | 0 | Yes |
| Adduct | Adduct of Ion fragmented in MS2 | M+H | Yes |
| Compound Name | Compound Common Name | N/A | Yes |
| Precursor MZ | Experimental Precursor MZ for Compound | 0 (will read from spectrum file if 0) | Yes |
| Charge | Charge of Precursor | 0 (will read from spectrum file if 0) | Yes |

**Advanced Annotation**

|     Field    | Description          | Default |  Required |
| ------------- |-------------| -----| ------- |
| CAS Number | Chemical Abstracts Service compound identification number | N/A | No |
| Pubmed ID | Pubmed ID where compound or data was published | N/A | No |
| Exact Mass | Compound Exact Mass | 0 | No |
| Smiles | Smiles Structure | N/A | No |
| Inchi | Inchi Structure | N/A | No |
| Inchi Aux | Inchi Auxiliary Structure | N/A | No |

### Guidance on Providing Names to the Annotations in GNPS

| Source | Structure | Structural Position of Analog | Mass Shift of Analog | Guidance | Example |
| ----- | ----- | ----- | ----- | ----- | ----- | 
| Chemical Standard | Full Structure Known | Known | N/A |  please annotate with the **common name** and provide the SMILES and Inchi in the corresponding text fields. | 7-Methylxanthine | 
| Your Data | Full Structure Proposed | Proposed based on MS/MS | N/A | please annotate with the **common name** and provide the SMILES and Inchi in the corresponding text fields (a bronze star rating will indicate a putative status) | 7-Methylxanthine |
| Your Data |  Incomplete Structure Proposed | Cannot based on MS/MS | N/A | please annotate with the **common name** and indicate the position is unknown using "X" | (X)-Methylxanthine |
| Your Data | No Structure Information | No Position Information | Mass shift provided via Molecular Networking | please annotate with the **common name** of the chemical it is connected to and indicate mass shift. Mass shift indicated by nominal mass followed by putative formula difference (if the formula difference is unknown please enter "X"). No SMILES or Inchi should be provided. | Caffeine +14(CH2) <br> Caffeine +52(X)|

### License

All GNPS Reference spectra contributed directly to GNPS by default will have the [CC0](https://creativecommons.org/publicdomain/zero/1.0/) license.

Third party libraries imported may not conform to the CC BY license and should be verified by users. 

## Page Contributors

{{ git_page_authors }}
