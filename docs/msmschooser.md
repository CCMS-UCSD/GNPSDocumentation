# Open-source Protocol for Community-created Public MS/MS Reference Library (MSMS-Chooser)

## Summary
[MSMS-Chooser](https://proteomics2.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22MS-CHOOSER%22%7D) is a GNPS workflow and open-source protocol to empower the community to collect MS/MS reference data and contribute to the public MS/MS reference library.

**This is a community effort and welcome everyone to participate!**
  * We encourage individuals to implement the protocols in their own laboratory.
  * Individuals with chemical standards without access to instrumentation are encouraged to contact the Dorrestein lab to inquire about running standards in collaboration (see contact information below).

## Requirements for MSMS-Chooser Workflow and Subsequent Addition of Spectra to the GNPS Library
  * Complete MSMS-Chooser Template
  * Data containing MS/MS data convereted to open-file formats (.mzXML or .mzML)
  * Validation of MSMS-Chooser output (using drag-and-drop validator) + visual inspection of MS/MS spectra
  * Email contacting Dorrestein Lab with task ID (see contact information below)

## Step-by-Step Instructions

### Completion of [MSMS-Chooser Template](https://docs.google.com/spreadsheets/d/1C6bpcaC2b4KpXaimkpslH4whlqKlN4T9DB-BKNYshjQ/edit?usp=sharing)
1. Make a copy of the **MSMS-Chooser Template** by selecting “File” and then “Make a copy” - continue working in Google Sheets
2. Fill out the MSMS-Chooser Template in the **"MSMS-Chooser Template"** tab
    * A readme tab is included that describes what should be entered as well as an example and additional information is in documentation (GitHub). ** Important: You must record the position of each chemical in the 96-well plate. **
    * Only columns H-Q need to be complete if submitting samples to Dorrestein Lab - approval required before submitting samples.
    * **Please complete one row for each chemical in the positive mode and then copy and paste rows below and update the “IONMODE” column from “Positive” to “Negative”.
3. Download a copy of the **MSMS-Chooser Submission** tab.
    * The MSMS-Chooser File required for submission is automatically generated in the "MSMS-Chooser Submission" tab
4. Download a copy of the applicable Sequence Table using the **Sequence Table Generator** tab as a .csv from Google Sheets.
  * Please double check the chemicals and well position match in the sequence table.

### Sample Preparation - List of Required Materials
  * HPLC grade solvents in all sample preparation steps (highly encouraged)
  * 96-well plates and corresponding well plate covers (autosampler compatible)
 
| Manufacturer | Item Number | Item | Recommended Pairing |
|:------------- |:-------------:|:-----:|:------:|
| Eppendorf       | 951040048 | Microplate 96/U-PP with white border | 1 |
|-|-|-| 1 |
| Thermo Scientific | 12565368 | Microplate U96 PP-0.5ml, natural | 2 |
| Thermo Scientific | 12565560 | 96 well cap, natural | 2 |

### Sample Preparation - Protocol
1. Generate a solution of your sample (standard) at a concentration of 10 µM.
2. Transfer 10 µL of your sample (standard) into a well in the 96 well plate recording the well position and chemical added.
    * One sample should be added per well
3. Repeat transfer of 10 µL into wells
4. Record plate number, well position, etc. in the sample submission template.
5. Once all standards have been added to the 96-well plate, completely dry all solutions.
    * Evaporation of the liquid can be done using the following techniques:
      * Nitrogen gas evaporation.
      * Low pressure evaporation system (Centrivap systems are recommended)
6. Seal plate using the previously mentioned 96 Well plate cover. 
    * Important: The material in the plate must be dry.
7. Store plate at -20 °C prior to shipping.

### Data Acqusition 
Please select the following link:

| Vendor | Instrument | Version | Revision Date| Method Files|
|:---:|:---:|:---:|:---:|:---:|
|Thermo|[QExactive](msmschooserdataacquisitionQE.md)|v1.0|Sept 4, 2019| [Link](massive_link_here)|
|-|-|-|-|-|
|-|-|-|-|-|


### Post-Data Acqusition 
1. It is recommended to completely dry all solutions.
    * Evaporation of the liquid can be done using the following techniques:
      * Nitrogen gas evaporation.
      * Low pressure evaporation system (Centrivap systems are recommended)
2. Place plates into a -20C freezer
3. Convert raw data to .mzXML

| Vendor | Instrument | Recommended Software| Settings |
|:---:|:---:|:---:|:---:|
|Thermo|QExactive|[MSconvert](http://proteowizard.sourceforge.net/tools.shtml)| mzXML and binary encoding precision as 32-bit|
|-|-|-|-|
|-|-|-|-|

4. Create a GNPS/MassIVE Dataset
  * Upload the files to your GNPS account using an FTP client (preferred clients are WinSCP, CoreFTP, and CoffeeCup Free FTP)
  * Name the MassIVE data set using the following format: “GNPS - Chemical Standard to GNPS Library - [insert barcodes]”
  * Upload all .raw files into the RAW folder and all .mzXML files into the PEAKS folder
  * Upload the **MSMS-CHOOSER Submission** file (.tsv) from the NAS folder, download as .tsv, place in SUPPLEMENTAL folder
  * Make data public

### MSMS-Chooser (v1.0)
1. Navigate to [ProteoSAFe](https://proteomics2.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22MS-CHOOSER%22%7D).
  * Select all .mzXML files, negative and positive, from MassIVE
  * Select the **"MSMS-Chooser Submission"** file (.tsv) from MassIVE
2. Launch the Job
3. Download result file and test using the following [Validator](http://dorresteinappshub.ucsd.edu:5020/).
4. Send completed Job Link to Contacts (detailed below)

## Contacts
Morgan Panitchpakdi(mpanitch@ucsd.edu) and Mingxun Wang (miw023@ucsd.edu)

## Data Availability
All public MS/MS spectra are avaliable for download and browsing in GNPS.

## Citation
<br>

## Issues and Suggestions
Please submit any issues or suggestions via [GitHub](https://github.com/CCMS-UCSD/GNPS_Workflows). The use of the [GNPS forum](https://groups.google.com/forum/#!forum/molecular_networking_bug_reports) is encouraged.

## Page Contributions
Alan K. Jarmusch (UCSD)
