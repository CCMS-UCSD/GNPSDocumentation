# Batch Upload of Annotated Spectra

While there is an interface to upload single spectra, users who wish to batch upload many spectra into the libraries might find adding one spectra at a time cumbersome. Here we provide a method to batch upload many spectra.

Here is a quick instructional video we have put together:

<iframe width="560" height="315" src="https://www.youtube.com/embed/IbXBpud57Z8?start=1796" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Materials

The materials that are required are:

1. Annotation Spread Sheet (This can be produced below manually by selecting scans in the mass spec data, or automatically generated with the MSMS-Chooser workflow - see documentation)
2. Source mzXML/mzML/mgf mass spectra files to pull MS/MS spectra 

**ATTENTION: Batch Annotation Workflow should be used to create spectral libraries of 50 spectra or more. Please contact CCMS Team with questions (ccms-web@cs.ucsd.edu)**

## Annotation Spread Sheet

To batch upload, this template must be used:

[Template Spreadsheet](static/Template.xlsx)

Annotation are to be added one spectrum per line. Columns may not be added, or deleted or changed. Each column **must have a value.** Refer to the table below for default values to enter when not known.

Export from this Excel file as a tab separated text file (recommended export from Windows office 2013 or newer. Verify that line endings are UNIX and not Windows line endings).

### Batch File Annotation

To check the validity of your batch file, check out our [batch validator](https://gnps-quickstart.ucsd.edu/validatebatch).

## Field Information

The field requirements are the same as on the single spectrum upload form, the other columns can be ignored. FIeld description are listed below.

Please note: Only letters, numbers and underscores are allowed in the filenames. Spaces and special characters are **NOT** allowed.

| Header        | Desc.                                    |Default Value to Put When Not Known | Possible Values             | Required |
| ------------- | ---------------------------------------- | ---------------------------------- | --------------------------- | -------- |
| FILENAME      | Input Filename (mzXML, mzML, or mgf)                   | REQUIRED | only letters, numbers, underscores and periods are allowed | Yes |
| SEQ           | Peptide Sequence                         | \*..\*     |  Please enter \*..\* here only                                                          | No  |
| COMPOUND_NAME | Compound Common Name                     | REQUIRED |                                                            | Yes |
| MOLECULEMASS  | Corrected Precursor MZ for Compound      | 0        | Entering 0 means we will attempt to read the mz value from file                                                           | No  |
| INSTRUMENT    | Mass Analyzer Instrument                 | REQUIRED | qTof, QQQ, Ion Trap, Hybrid FT, Orbitrap, ToF                   | Yes |
| IONSOURCE     | Source of Ions                           | REQUIRED | LC-ESI, DI-ESI, EI, APCI, ESI                                             | Yes |
| EXTRACTSCAN   | Spectrum Scan of Spectrum                | REQUIRED |                                                            | Yes |
| SMILES        | Smiles Structure                         | N/A      |                                                            | No  |
| INCHI         | Inchi Structure                          | N/A      |                                                            | No  |
| INCHIAUX      | Inchi Auxiliary Structure                | N/A      |                                                            | No  |
| CHARGE        | Charge of Precursor (0 to pull from the spectrum file) | 0 |                                                     | No  |
| IONMODE       | Ionization Mode (Positive/Negative)      | Positive | Positive, Negative                                         | Yes |
| PUBMED        | Pubmed ID where compound or data was published | N/A   |                                                         | No  |
| ACQUISITION   | Sample source of compound                | Crude    | Crude, Lysate, Commercial, Isolated, Other                 | Yes |
| EXACTMASS     | Compound Exact Mass                      | 0        |                                                            | No  |
| DATACOLLECTOR | Individual collecting data               | REQUIRED |                                                            | Yes |
| ADDUCT        | Adduct of Ion Fragmented in MS2 (M+H, M+2H, etc.) | REQUIRED |                                                   | Yes |
| INTEREST      | N/A                                      | N/A      |                                                            | No  |
| LIBQUALITY    | Quality of Library (1 for Gold, 2 for Silver, 3 for Bronze) | 3     | 1,2,3                                      | Yes |
| GENUS         | Genus                                    | N/A      |                                                            | No  |
| SPECIES       | Species                                  | N/A      |                                                            | No  |
| STRAIN        | Strain                                   | N/A      |                                                            | No  |
| CASNUMBER     | Chemical Abstracts Service compound identification number | N/A  |                                               | No  |
| PI            | PI overseeing compound acquisition and analysis           | Required |                                           | Yes |

It must be noted that filenames must match exactly to those users are uploading. Filenames must also be unique, and can only contain numbers, letters, hyphens, underscores, and periods. All fields for each row must have some content -- blank fields are unacceptable. Fields other than filename also **cannot** contain return carriages or tabs.

## Spectrum Upload

Users will need to upload their files into GNPS. To do this please refer to the upload documentation [here](fileupload.md).

## Creation/Publication of Spectral Library

To actually add the spectra to the libraries, users will

1. Export excel file as a tab separated text file and upload to GNPS (recommended export from Windows office 2013 or newer. Verify that line endings are UNIX and not Windows line endings)
1. Launch Batch Validator Workflow with all spectrum files and annotation table found [here](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22ADD-BATCH-ANNOTATED-VALIDATOR%22%7D). NOTE: Creating spectral libraries from MGF files is discouragedas it is not a well defined format. If you do insist, you must make sure each MGF start from scan 1 (e.g. SCANS=1 in the file) and are incremented sequentially without any missing scan numbers. 
1. Users will then need to contact the Wang Bioninformatics Lab (mingxun.wang@cs.ucr.edu) and send her the completed job from above.
1. A private spectral library will then be created by Jasmine. 
1. After the contributor may review the library to be made into a public library and will be made public after approval. 

### License

All GNPS Reference spectra contributed directly to GNPS by default will have the [CC0](https://creativecommons.org/publicdomain/zero/1.0/) license.

Third party libraries imported may not conform to the CC BY license and should be verified by users. 

## Page Contributions

{{ git_page_authors }}
