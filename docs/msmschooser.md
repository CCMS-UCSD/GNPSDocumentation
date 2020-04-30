# Open-source Protocol for Community-created Public MS/MS Reference Library (MSMS-Chooser)

---

## Summary
[MSMS-Chooser](https://proteomics2.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22MS-CHOOSER%22%7D) is a GNPS workflow and open-source protocol to empower the community to collect MS/MS reference data and contribute to the public MS/MS reference library.

**This is a community effort and welcome everyone to participate!** <br>
  - We encourage individuals to implement the protocols in their own laboratory. <br>
  - Individuals with chemical standards without access to instrumentation are encouraged to contact the Dorrestein lab to inquire about running standards in collaboration (see contact information below). <br>

---

## Requirements for MSMS-Chooser Workflow and Subsequent Addition of Spectra to the GNPS Library
  - Complete MSMS-Chooser Template
  - Data containing MS/MS data convereted to open-file formats (.mzXML or .mzML)
  - Validation of MSMS-Chooser output (using drag-and-drop validator) + visual inspection of MS/MS spectra
  - Email contacting Dorrestein Lab with task ID (see contact information below)

---

## Step-by-Step Instructions

### Completion of MSMS-Chooser Template - [Link Here](https://docs.google.com/spreadsheets/d/1C6bpcaC2b4KpXaimkpslH4whlqKlN4T9DB-BKNYshjQ/edit?usp=sharing)
1. Make a copy of the **MSMS-Chooser Template** by selecting “File” and then “Make a copy”. We **strongly encourage** users to continue working in Google Sheets as the formatting will be maintained.
2. Fill out the MSMS-Chooser Template in the **"MSMS-Chooser Sample Template"** tab.

    > Notes: <br>
      - The first tab describes what should be entered as well as an example and additional information is in documentation (GitHub). **Important: You must record the position of each chemical in the 96-well plate.** <br>
      - Only columns H-Q need to be complete if submitting samples to Dorrestein Lab - approval required before submitting samples. <br>
      - **Please complete one row for each chemical in the positive mode and then copy and paste rows below and update the “IONMODE” column from “Positive” to “Negative”.** <br>
  
3. Download a copy of the **MSMS-Chooser Submission File** tab as a .tsv file by selecting "File", "Download", and then "Tab-separated value (.tsv, current sheet)."

    > Notes: <br>
      - The MSMS-Chooser File required for submission is automatically generated in the "MSMS-Chooser Submission" tab. <br>

4. Download a copy of the applicable Sequence Table using the **Sequence Table Generator** tab as a .csv file from Google Sheets by selecting "File", "Download", and then "Comma-separated value (.csv, current sheet)."

    > Notes: <br>
      - Please double check the chemicals and well position indicated in the submission file match the sequence table. <br>

---

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
    > Notes: <br>
      - The amount of material needed for detection is not universal and will vary by chemical. The value is a suggested starting place. <br>
      
2. Transfer 10 µL of your sample (standard) into a well in the 96 well plate recording the well position and chemical added.

    > Notes: <br>
      - One sample should be added per well. <br>

3. Repeat transfer of 10 µL into wells
4. Record plate number, well position, etc. in the sample submission template.
5. Once all standards have been added to the 96-well plate, completely dry all solutions.

    > Notes: <br>
      - Evaporation of the liquid can be done using the following techniques: Nitrogen gas evaporation or low pressure evaporation system (Centrivap systems are recommended). <br>

6. Seal plate using the previously mentioned 96 well plate cover.
7. If analysis is to be performed in your laboratory, then we suggest storing the material dried in the 96 well plate, covered, at -20 °C prior to analysis. If you desired to collaborate with the Dorrestein lab, then the material **must be dried in a 96 well plate and covered** for shipping and should be stored at -20 °C.

---

### Data Acqusition 
Please select the following link:

| Vendor | Instrument | Version | Revision Date| Method Files|
|:---:|:---:|:---:|:---:|:---:|
|Thermo|QExactive - [Link](msmschooserdataacquisitionQE.md)|v1.0|Sept 4, 2019| [Link](https://massive.ucsd.edu/ProteoSAFe/dataset.jsp?task=5e567bd3eb1e40ad975a25dac3f5bf11)|
|-|-|-|-|-|
|-|-|-|-|-|

---

### Post-Data Acqusition 
1. It is recommended to completely dry all solutions.

    > Notes: <br>
      - Evaporation of the liquid can be done using the following techniques: Nitrogen gas evaporation or Low pressure evaporation system (Centrivap systems are recommended). <br>
  
2. Place plates into a -20C freezer.
3. Convert raw data to .mzXML (see table at end of this section).
4. Create a GNPS/MassIVE Dataset <br>
    - Upload the files to your GNPS account using an FTP client (preferred clients are WinSCP, CoreFTP, and CoffeeCup Free FTP)
    - Name the MassIVE data set using the following format: “GNPS - MSMS-Chooser - [insert barcodes]”
    - Upload all .raw files into the RAW folder and all .mzXML files into the PEAKS folder
    - Upload the **MSMS-CHOOSER Submission** file (.tsv) from the NAS folder, download as .tsv, place in SUPPLEMENTAL folder
    - Make data public

| Vendor | Instrument | Recommended Conversion Software | Settings |
|:---:|:---:|:---:|:---:|
|Thermo|QExactive|MSconvert - [Link](http://proteowizard.sourceforge.net/tools.shtml)| mzXML and binary encoding precision as 32-bit|
|-|-|-|-|
|-|-|-|-|

---

## MSMS-Chooser (v1.0) Workflow at GNPS

1. Navigate to ProteoSAFe - [link here](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22MSMS-CHOOSER%22%7D).
2. Select all .mzXML files from MassIVE (positive and negative mode should be selected into the same folder).
3. Select the **"MSMS-Chooser Submission"** file (.tsv) from MassIVE (or uploaded via the drag-and-drop method in the 2nd tab over in the selection UI).
4. The default mass error tolerance is 10 ppm. This value should be adjusted according to the instrumentation and experimental conditions used to collect the mass spectrometry data.
5. Launch the Job.

### Basic Information about MSMS-Chooser
This workflow selects MS/MS spectra, specifically product ion scans, based on precursor *m/z* (within 10 ppm error by default). Retention time is not taken into consideration given the provided MSMS-Chooser workflow method uses flow-injection. Several adducts are considered in the positive and negative mode for each chemical (tabulated below). If additional adducts are required, please contact us.

| Ionization Mode | Adducts Supported |
|:---:|:---:|
|Positive|[M+H]+, [M+Na]+, [M+K]+, [2M+H]+, [2M+Na]+, [2M+K]+, [M-H2O+H]+, [M-2H2O+H]+|
|Negative|[M-H]-, [2M-H]-, [2M-2H+Na]-|

---

## Interpretation and Validation of MSMS-Chooser (v1.0) Results
![img](img/MSMSChooserResults.png)

The results can be accessed by clicking the "View Output Batch Table" link and the "View Spectrum" button on the left-hand side of the table for each chemical. **review of all data is strongly encouraged** <br>
1. After review, if all look acceptable
    - click the “Next Step: Batch Anotation Validator on GNPS” and run the validation workflow.
    - Once complete, email Morgan (ccms-web@cs.ucsd.edu) and send her the completed job from above.
2. After review, if you would like to remove MS/MS for any reason
    - Download the “Download Output Batch Table” and delete the rows you would like to exclude.
    - You should then follow the “[Batch Upload of Annotated Spectra](https://ccms-ucsd.github.io/GNPSDocumentation/batchupload/)" documentation (you will need to reselect the files and upload the modified “output batch table” in the “Annotation Table” option).
    - Once complete, email Morgan (ccms-web@cs.ucsd.edu) and send her the completed job from above.

---

## FAQs

**"What if I alreadly have data collected, can MSMS-Chooser help me?"**
  - Yes! MSMS-Chooser can be used as a shortcut and help you perform the steps of finding the MS/MS spectra in your files and format the data for inclusion in the GNPS MS/MS reference library. However, this was not the original intent of the MSMS-Chooser workflow. You should create a copy and completely fill the **"MSMS-Chooser Sample Template"** tab, download it, and include it with the files in the MSMS-Chooser workflow. The MSMS-Chooser workflow will go through your data and select a MS/MS spectrum for every chemical as indicated in the Sample Template. We have used MSMS-Chooser to help create the [BILELIB19](https://gnps.ucsd.edu/ProteoSAFe/gnpslibrary.jsp?library=BILELIB19) library in GNPS.
    > Notes: <br>
      - **ALL** data should be reviewed for accuracy. If chemical separation is performed prior to analysis, then special attention should be given to the MS/MS spectrum and retention time. MSMS-Chooser only matches on accurate mass (currently) and isobaric compounds eluting at different times might be confused. <br>
      
**"Can I use this method to run isolated, possibly impure, chemicals?"**
   - Yes! GNPS MS/MS spectral libraries allow any contribution even if the structure or identification is not fully confirmed. The GNPS community will help correct any inaccuracies over time with provenance of all edits and updates.

---

## Issues and Suggestions
  - Please submit any issues or suggestions via GitHub - [link here](https://github.com/CCMS-UCSD/GNPS_Workflows).
  - The use of the GNPS forum - [link here](https://groups.google.com/forum/#!forum/molecular_networking_bug_reports) is encouraged.

---

## Data Availability
All public MS/MS spectra are avaliable for download and browsing in GNPS.

---

## Citation
Vargas, F, Weldon, KC, Sikora, N, et al. Protocol for Community‐created Public MS/MS Reference Spectra Within the Global Natural Products Social Molecular Networking Infrastructure. Rapid Commun Mass Spectrom. 2020. https://doi.org/10.1002/rcm.8725

---

## Contacts
  - Morgan Panitchpakdi(mpanitch@ucsd.edu) <br>
  - Mingxun Wang (miw023@ucsd.edu) <br>
  - Alan Jarmusch (ajarmusch@ucsd.edu) <br>

---

## Page Contributions
Alan K. Jarmusch (UCSD)
