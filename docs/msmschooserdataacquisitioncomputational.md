# Computational Preparation for Data Acquisition and MSMS-Chooser to Create Spectral Libraries

---

## Summary

These tools comprise an open-source protocol to empower the community to collect MS/MS reference data and contribute to the public MS/MS reference library.

Here are the steps that aid in the creation of the proper templates to acquire data that is definitely compatible with MSMS-Chooser as well as templates to go directly into the MSMS-Chooser workflow. 

!!! info
	**This is a community effort and welcome everyone to participate!**
	- We encourage individuals to implement the protocols in their own laboratory. <br>
	- Individuals with chemical standards without access to instrumentation are encouraged to contact the Dorrestein lab to inquire about running standards in collaboration (see contact information on the [MSMSChooser page](msmschooser.md)).

---

## Step-by-Step Instructions

### Completion of MSMS-Chooser Preparation Template - [Link Here](https://docs.google.com/spreadsheets/d/1C6bpcaC2b4KpXaimkpslH4whlqKlN4T9DB-BKNYshjQ/edit?usp=sharing)
- Make a copy of the **MSMS-Chooser Preparation Template** by selecting “File” and then “Make a copy”. We **strongly encourage** users to continue working in Google Sheets as the formatting will be maintained.
- Fill out the MSMS-Chooser Template in the **"MSMS-Chooser Sample Template"** tab.

!!! info
    - The first tab describes what should be entered as well as an example and additional information is in documentation (GitHub). **Important: You must record the position of each chemical in the 96-well plate.**
    - Only columns H-Q need to be complete if submitting samples to Dorrestein Lab - approval required before submitting samples.
    - **Please complete one row for each chemical in the positive mode and then copy and paste rows below and update the “IONMODE” column from “Positive” to “Negative”.** 
  
- Download a copy of the **MSMS-Chooser Submission File** tab as a .tsv file by selecting "File", "Download", and then "Tab-separated value (.tsv, current sheet)."

!!! info
    The MSMS-Chooser File required for submission is automatically generated in the "MSMS-Chooser Submission" tab.

- Download a copy of the applicable Sequence Table using the **Sequence Table Generator** tab as a .csv file from Google Sheets by selecting "File", "Download", and then "Comma-separated value (.csv, current sheet)."

!!! info
    Please double check the chemicals and well position indicated in the submission file match the sequence table.

---
!!! info "List of Suggested Materials for Sample Preparation"
	- HPLC grade solvents in all sample preparation steps (highly encouraged)
	- 96-well plates and corresponding well plate covers (autosampler compatible)
	| Manufacturer | Item Number | Item | Recommended Pairing |
	|:------------- |:-------------:|:-----:|:------:|
	| Eppendorf       | 951040048 | Microplate 96/U-PP with white border | 1 |
	|-|-|-| 1 |
	| Thermo Scientific | 12565368 | Microplate U96 PP-0.5ml, natural | 2 |
	| Thermo Scientific | 12565560 | 96 well cap, natural | 2 |

### Sample Preparation - Protocol
-  Generate a solution of your sample (standard) at a concentration of 10 µM.

!!! note
    The amount of material needed for detection is not universal and will vary by chemical. The value is a suggested starting place.
      
- Transfer 10 µL of your sample (standard) into a well in the 96 well plate recording the well position and chemical added.

!!! warning
    One sample should be added per well.

- Repeat transfer of 10 µL into wells
- Record plate number, well position, etc. in the sample submission template.
- Once all standards have been added to the 96-well plate, completely dry all solutions.

!!! info
    Evaporation of the liquid can be done using the following techniques: Nitrogen gas evaporation or low pressure evaporation system (Centrivap systems are recommended).

- Seal plate using the previously mentioned 96 well plate cover.
- If analysis is to be performed in your laboratory, then we suggest storing the material dried in the 96 well plate, covered, at -20 °C prior to analysis. If you desired to collaborate with the Dorrestein lab, then the material **must be dried in a 96 well plate and covered** for shipping and should be stored at -20 °C.

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
- It is recommended to completely dry all solutions.

!!! info
    Evaporation of the liquid can be done using the following techniques: Nitrogen gas evaporation or Low pressure evaporation system (Centrivap systems are recommended).
  
- Place plates into a -20C freezer.
- Convert raw data to .mzXML

!!! info
	| Vendor | Instrument | Recommended Conversion Software | Settings |
	|:---:|:---:|:---:|:---:|
	|Thermo|QExactive|MSconvert - [Link](http://proteowizard.sourceforge.net/tools.shtml)| mzXML and binary encoding precision as 32-bit|
	|-|-|-|-|
	|-|-|-|-|

- Create a GNPS/MassIVE Dataset
	- Upload the files to your GNPS account using an FTP client (preferred clients are WinSCP, CoreFTP, and CoffeeCup Free FTP)
	- Name the MassIVE data set using the following format: “GNPS - MSMS-Chooser - [insert barcodes]”
 	- Upload all .raw files into the RAW folder and all .mzXML files into the PEAKS folder
	- Upload the **MSMS-CHOOSER Submission** file (.tsv) and place in SUPPLEMENTAL folder
	- Make data public
- Run MSMS-Chooser workflow at GNPS to find the reference spectra in your data. See [here](msmschooser.md) for more details. 

!!! warning
    **ALL** data should be reviewed for accuracy. If chemical separation is performed prior to analysis, then special attention should be given to the MS/MS spectrum and retention time. MSMS-Chooser only matches on accurate mass (currently) and isobaric compounds eluting at different times might be confused.
    
---

## FAQs

!!! question "What if I alreadly have data collected, can MSMS-Chooser help me?"
	- **Yes!** MSMS-Chooser can be used as a shortcut and help you perform the steps of finding the MS/MS spectra in your files and format the data for inclusion in the GNPS MS/MS reference library. However, this was not the original intent of the MSMS-Chooser workflow. You should create a copy and completely fill the **"MSMS-Chooser Sample Template"** tab, download it, and include it with the files in the MSMS-Chooser workflow. The MSMS-Chooser workflow will go through your data and select a MS/MS spectrum for every chemical as indicated in the Sample Template. We have used MSMS-Chooser to help create the [BILELIB19](https://gnps.ucsd.edu/ProteoSAFe/gnpslibrary.jsp?library=BILELIB19) library in GNPS.     

!!! question "Can I use this method to run isolated, possibly impure, chemicals?"
	- **Yes!** GNPS MS/MS spectral libraries allow any contribution even if the structure or identification is not fully confirmed. The GNPS community will help correct any inaccuracies over time with provenance of all edits and updates.

## Page Contributions
{{ git_page_authors }}
