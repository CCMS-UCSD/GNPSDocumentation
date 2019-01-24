# Batch Upload of Annotated Spectra

While there is an interface to upload single spectra, users who wish to batch upload many spectra into the libraries might find adding one spectra at a time cumbersome. Here we provide a method to batch upload many spectra.

## Annotation Spread Sheet

To batch upload, this template must be used:

[Template Spreadsheet](https://bix-lab.ucsd.edu/download/attachments/14229110/Template.xlsx?version=1&modificationDate=1393554378000)

Annotation are to be added one spectrum per line. Columns may not be added, or deleted or changed. Each column **must have a value.** Refer to the table below for default values to enter when not known.

## Field Information

The field requirements are the same as on the single spectrum upload form, the other columns can be ignored. FIeld description are listed below.

Please note: Only letters, numbers and underscores are allowed in the filenames. Spaces and special characters are **NOT** allowed.

| Header        | Desc. |Default Value to Put When Not Known | Possible Values | Required |
| ------------- | ----- | ---------------------------------- | --------------- | -------- |
| FILENAME      | Input Filename (mzXML) | REQUIRED | only letters, numbers, underscores and periods are allowed | Yes |
| SEQ           | Peptide Sequence       | *..*     |                                                            | No  |
| COMPOUND_NAME | Compound Common Name   | REQUIRED |                                                            | YES |
| MOLECULEMASS  | Corrected Precursor MZ for Compound | 0 |                                                      | No  |
| INSTRUMENT    | Mass Analyzer Instrument            | REQUIRED | qTof, QQQ, Ion Trap, Hybrid FT, Orbitrap      | Yes |
| IONSOURCE     | Source of Ions                      | REQUIRED | LC-ESI, DI-ESI                                | Yes |
| EXTRACTSCAN   | Spectrum Scan of Spectrum           | REQUIRED |                                               | Yes |
| SMILES        | Smiles Structure                    | N/A      |                                               | No  |
| INCHI         | Inchi Structure                     | N/A      |                                               | No  |
| INCHIAUX      | Inchi Auxiliary Structure                             | N/A      |                                               | No  |
| CHARGE        | Charge of Precursor (0 to pull from the spectrum file) | 0 |                                                     | No  |
| IONMODE       | Ionization Mode (Positive/Negative)            | Positive | Positive, Negative                                   | Yes |
| PUBMED        | Pubmed ID where compound or data was published | N/A   |                                                         | No  |
| ACQUISITION   | Sample source of compound                      | Crude | Crude, Lysate, Commercial, Isolated, Other              | Yes |
| EXACTMASS     | Compound Exact Mass                            | 0     |                                                         | No  |
| DATACOLLECTOR | Individual collecting data                     | REQUIRED |                                            | Yes |
| ADDUCT        | Adduct of Ion Fragmented in MS2 (M+H, M+2H, etc.) | REQUIRED |                                        | Yes |
| INTEREST      | N/A                                         | N/A  |                                          | Yes |

