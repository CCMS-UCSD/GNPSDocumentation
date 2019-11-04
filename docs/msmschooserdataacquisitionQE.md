# MSMS-Chooser: Data Acquisition - QExactive (v1.0)

## Summary
 **This document details an open-source protocol for the Thermo QExactive mass spectrometer coupled to the Thermo Vanquish UHPLC** used to combination with [MSMS-Chooser](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22MSMS-CHOOSER%22%7D), a GNPS workflow and open-source protocol to empower the community to collect MS/MS reference data and contribute to the public MS/MS reference library.

1-5 μL of sample is introduced into a flow of MeOH-Water (1:1) with ~0.1% formic acid at 0.5 mL/min via injection from the autosampler. The needle is washed for 3 s prior to injection, flow rate of 10 μL/sec. Data acquisition for each injection is 0.3 minutes with the majority of the sample arriving ~0.05 - 0.1 min after injection. Data-dependant acquisition is used to collect data on the top 5 precursors at a resolution of 35,000. MS/MS data are collected using an isolation width of m/z 1.7 and stepped normalized collision energy of 20, 30, and 40. Separate positive and negative ionization mode methods were created with differences in the ionization source parameters. Further details can be found in the method files.

Data acquisition takes 0.3 min followed by 0.3 - 0.4 min of needle washing and drawing of the next sample before the next sample. The total processes taking ~45 - 50 s for one injection sequence. The flow continues during the needle washing and drawing time, effectively flushing the line for ~30 s in between samples. 

## Required Materials
1. Vanquish UHPLC
    * Solvent A - water (HPLC grade) w/ ~0.1% formic acid (v/v) = 4 L of water (HPLC grade) + 4 mL of formic acid using glass syringe, mix by inverting bottle 15 times.
     * Solvent B - methanol (HPLC grade) w/ ~0.1% formic acid (v/v) = 4 L of methanol (HPLC grade) + 4 mL of formic acid using glass syringe, mix by inverting bottle 15 times.
   * Associated fittings and tubing
2. QExactive
3. Syringe pump and required fitting for instrument calibration (see instrument calibration SOP)
4. MS calibration solution specific to calibration protocol
5. MS tune and MS method files can be downloaded from [MassIVE](https://massive.ucsd.edu/ProteoSAFe/dataset.jsp?task=5e567bd3eb1e40ad975a25dac3f5bf11).

## Step-by-Step Instructions
### Data Acquisition
1. Create a folder on the local computer following this standard “D:\SOPGNPSChemicaltoLibrary\[insert barcode]”
2. Obtain the **MSMS-Chooser sequence table** and copy it to a folder on the local computer.
   * If you are analyzing more than one plate, open the corresponding .csv files and copy and merge  them together in a spreadsheet editor. You will need to change the plate positions.
3. Double check the barcode, the number of samples, and the plate position used (e.g. “red”; “RA1”).
4. Calibrate the QExactive following instrument manufacturer directions in both negative and positive ion modes (using the appropriate tune file and source position).
5. After calibration passes, load the “20190520_SOP_chemicalreferencetoGNPSlibrary_positive.meth”.
   * the path to the tune file may need to be updated in the methods
6. Place Solvent A and Solvent B onto the LC and purge the lines.
7. Check all other solutions (e.g. needle wash) and ensure solvent level is sufficient.
8. Place a zero-dead volume union (stainless steel) in the column compartment.
9. Turn the instrument from “standby” to “on”.
10. Flow the solvent 50% Solvent A and 50% Solvent B @ 0.5 mL / min.
    * The backpressure was observed to be between 30-50 bar depending on the temperature of the column compartment.
11. Import the appropriate sequence table (.csv) into Xcalibur, and double check the following:
    * The barcode matches
    * The amount of rows in the sequence table matches the number of wells.
    * The plate is positioned in the correct tray, (e.g. red if the injection position starts with “R:”)
    * Ensure that the positive and negative mode methods are appropriately selected.
12. Save the sequence file and start data collection

## Issues and Suggestions
Please submit any issues or suggestions via [GitHub](https://github.com/CCMS-UCSD/GNPS_Workflows). The use of the [GNPS forum](https://groups.google.com/forum/#!forum/molecular_networking_bug_reports) is encouraged.

## Page Contributions
Alan K. Jarmusch (UCSD)
