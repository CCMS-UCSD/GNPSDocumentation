# GNPS API Overview

## GNPS Library Spectra

### All Public Library Spectra at GNPS

This gets you all spectra but without peaks. 

```
https://external.gnps2.org/gnpslibraryjson
```

### All Public Library Name List at GNPS

```
https://external.gnps2.org/gnpslibrary.json
```

Browse all spectra

```
https://external.gnps2.org/gnpslibrary
```

Download as JSON

```
https://external.gnps2.org/gnpslibrary/ALL_GNPS.json
```

??? info "Example JSON Format"

    ``` JSON
    [
        {
            "spectrum_id": "CCMSLIB00000579358",
            "source_file": "Training_001.mgf",
            "task": "03c206430208430c887ca025ea6c3641",
            "scan": "1",
            "ms_level": "2",
            "library_membership": "CASMI",
            "spectrum_status": "1",
            "peaks_json": "[[164.033997,32294.500000],[179.057495,129907.101562]]",
            "splash": "null-null-null-null",
            "submit_user": "lfnothias",
            "Compound_Name": "Theophyllin",
            "Ion_Source": "LC-ESI",
            "Compound_Source": "Commercial",
            "Instrument": "Orbitrap",
            "PI": "CASMI",
            "Data_Collector": "CASMI2016",
            "Adduct": "M-H",
            "Scan": "-1",
            "Precursor_MZ": "179.057",
            "ExactMass": "0.0",
            "Charge": "1",
            "CAS_Number": "N/A",
            "Pubmed_ID": "33919",
            "Smiles": "CN1C2=C(NC=N2)C(=O)N(C)C1=O",
            "INCHI": "\"InChI=1S/C7H8N4O2/c1-10-5-4(8-3-9-5)6(12)11(2)7(10)13/h3H,1-2H3,(H,8,9)\"",
            "INCHI_AUX": "N/A",
            "Library_Class": "1",
            "SpectrumID": "CCMSLIB00000579358",
            "Ion_Mode": " Negative",
            "create_time": "2016-05-24 18:27:20.0",
            "task_id": "03c206430208430c887ca025ea6c3641",
            "user_id": "null",
            "InChIKey_smiles": "ZFXYFBGIUFBOJW-UHFFFAOYSA-N",
            "InChIKey_inchi": "None",
            "Formula_smiles": "C7H8N4O2",
            "Formula_inchi": "",
            "url": "https://gnps.ucsd.edu/ProteoSAFe/gnpslibraryspectrum.jsp?SpectrumID=CCMSLIB00000579358",
            "annotation_history": [
                {
                    "Compound_Name": "Theophyllin",
                    "Ion_Source": "LC-ESI",
                    "Compound_Source": "Commercial",
                    "Instrument": "Orbitrap",
                    "PI": "CASMI",
                    "Data_Collector": "CASMI2016",
                    "Adduct": "M-H",
                    "Scan": "-1",
                    "Precursor_MZ": "179.057",
                    "ExactMass": "0.0",
                    "Charge": "1",
                    "CAS_Number": "N/A",
                    "Pubmed_ID": "33919",
                    "Smiles": "CN1C2=C(NC=N2)C(=O)N(C)C1=O",
                    "INCHI": "\"InChI=1S/C7H8N4O2/c1-10-5-4(8-3-9-5)6(12)11(2)7(10)13/h3H,1-2H3,(H,8,9)\"",
                    "INCHI_AUX": "N/A",
                    "Library_Class": "1",
                    "SpectrumID": "CCMSLIB00000579358",
                    "Ion_Mode": " Negative",
                    "create_time": "2016-05-24 18:27:20.0",
                    "task_id": "03c206430208430c887ca025ea6c3641",
                    "user_id": "lfnothias"
                }
            ]
        }
    ]
    ```

As MGF

```
https://external.gnps2.org/gnpslibrary/ALL_GNPS.mgf
```

??? info "Example MGF Format"
    ```
    BEGIN IONS
    PEPMASS=407.186
    CHARGE=1
    MSLEVEL=2
    SOURCE_INSTRUMENT=LC-ESI-qTof
    FILENAME=Plate1_1_20_GG1_01_16488.mzXML
    SEQ=*..*
    IONMODE=Positive
    ORGANISM=GNPS-SELLECKCHEM-FDA-PART2
    NAME=Bortezomib (Velcade) [M+Na]
    PI=Dorrestein
    DATACOLLECTOR=Garg_Neha
    SMILES=C1=CN=CC(=N1)C(N[C@H](C(N[C@H](B(O)O)CC(C)C)=O)CC2=CC=CC=C2)=O
    INCHI=N/A
    INCHIAUX=N/A
    PUBMED=N/A
    SUBMITUSER=negarg
    LIBRARYQUALITY=1
    SPECTRUMID=CCMSLIB00000077995
    SCANS=1211
    95.886879	236.0
    131.058121	188.0
    144.823196	204.0
    ...
    1402.281494	144.0
    END IONS
    ```

As MSP

```
https://external.gnps2.org/gnpslibrary/ALL_GNPS.msp
```

### All GNPS Spectra and Structure as a Table

```
https://external.gnps2.org/gnpslibraryfornpatlastsv
```

### Single Library Spectrum

```
https://gnps.ucsd.edu/ProteoSAFe/SpectrumCommentServlet?SpectrumID=<Library Accession>
```

[Example](https://gnps.ucsd.edu/ProteoSAFe/SpectrumCommentServlet?SpectrumID=CCMSLIB00005463737)


### Experimental or Library Spectrum by USI

Access a JSON or csv version of a spectrum by any Universal Spectrum Identifier.

```
https://metabolomics-usi.gnps2.org/json/?usi1=<USI HERE>
https://metabolomics-usi.gnps2.org/csv/?usi1=<USI HERE>
```

[json example for mzspec:GNPS:GNPS-LIBRARY:accession:CCMSLIB00000579622](https://metabolomics-usi.gnps2.org/json/?usi1=mzspec%3AGNPS%3AGNPS-LIBRARY%3Aaccession%3ACCMSLIB00000579622)

[csv example for mzspec:GNPS:GNPS-LIBRARY:accession:CCMSLIB00000579622](https://metabolomics-usi.gnps2.org/csv/?usi1=mzspec%3AGNPS%3AGNPS-LIBRARY%3Aaccession%3ACCMSLIB00000579622)

## GNPS Jobs

### Job Results API

GNPS job results page in JSON format:

```
https://gnps.ucsd.edu/ProteoSAFe/result_json.jsp?task=<task id>&view=<view name>
```

[Example](https://gnps.ucsd.edu/ProteoSAFe/result_json.jsp?task=1ad7bc366aef45ce81d2dfcca0a9a5e7&view=view_all_annotations_DB)

### Job Status API

GNPS job status page in JSON format:

```
https://gnps.ucsd.edu/ProteoSAFe/status_json.jsp?task=<task id>
```

### Job Parameters

GNPS job parameters page in XML format:

```
https://gnps.ucsd.edu/ProteoSAFe/ManageParameters?task=<task id>
```

## Structure Conversion

### Conversion to Smiles

```
https://structure.gnps2.org/smiles?inchi=<inchi string>
```

[Example](https://structure.gnps2.org/smiles?inchi=InChI=1S/C8H10N4O2/c1-10-4-9-6-5(10)7(13)12(3)8(14)11(6)2/h4H,1-3H3)

### Conversion to InChI

```
https://structure.gnps2.org/inchi?smiles=<smiles string>
```

[Example](https://structure.gnps2.org/inchi?smiles=Cn1c(=O)c2c(ncn2C)n(C)c1=O)

### Conversion to InChIKey

```
https://structure.gnps2.org/inchikey?smiles=<smiles string>
```

[Example](https://structure.gnps2.org/inchikey?smiles=Cn1c(=O)c2c(ncn2C)n(C)c1=O)

### Conversion to fingerprint

```
https://structure.gnps2.org/structurefingerprint?smiles=<smiles string>
```

[Example](https://structure.gnps2.org/structurefingerprint?smiles=Cn1c(=O)c2c(ncn2C)n(C)c1=O)

### Conversion to exact mass

```
https://structure.gnps2.org/structuremass?smiles=<smiles string>
```

### Compare to Adduct m/z

```
https://structure.gnps2.org/adductcalc?smiles=<smiles string>&mz=<experimental mz>
```

[Example](https://structure.gnps2.org/adductcalc?smiles=Cn1c(=O)c2c(ncn2C)n(C)c1=O&mz=195.08765155999998)

### Conversion to formula

```
https://structure.gnps2.org/formula?smiles=<smiles string>
```

[Example](https://structure.gnps2.org/formula?smiles=Cn1c(=O)c2c(ncn2C)n(C)c1=O)

### Structure Classyfire

If you have Smiles

```
https://structure.gnps2.org/classyfire?smiles=<smiles string>
```

[Example](https://structure.gnps2.org/classyfire?smiles=Cn1c(=O)c2c(ncn2C)n(C)c1=O)

If you have InChI

```
https://structure.gnps2.org/classyfire?inchi=<InChI string>
```

[Example](https://structure.gnps2.org/classyfire?inchi=InChI=1S/C8H10N4O2/c1-10-4-9-6-5(10)7(13)12(3)8(14)11(6)2/h4H,1-3H3)

If you have InChI Key

```
https://gnps-classyfire.ucsd.edu/entities/<InChI Key>.json
```

[Example](https://gnps-classyfire.ucsd.edu/entities/RYYVLZVUVIJVGH-UHFFFAOYSA-N.json)

Additionally, in case the inchikey is not classified, you can provide ```smiles``` or ```inchi``` arguments for 
us to push to the Wishart servers to classify. 

!!! note "ClassyFire" 
    ClassyFire is tool from the Wishart Lab - check it out [here](https://jcheminf.biomedcentral.com/articles/10.1186/s13321-016-0174-y). Here is the recommended citation: 
    Feunang, Yannick Djoumbou, Roman Eisner, Craig Knox, Leonid Chepelev, Janna Hastings, Gareth Owen, Eoin Fahy et al. "ClassyFire: automated chemical classification with a comprehensive, computable taxonomy." Journal of cheminformatics 8, no. 1 (2016): 61.

### Structure Natural Product Classifier (NP Classifier)

If you have Smiles

```
https://npclassifier.gnps2.org/classify?smiles=<smiles string>
```

[Example](https://npclassifier.gnps2.org/classify?smiles=Cn1c(=O)c2c(ncn2C)n(C)c1=O)

??? info "Example JSON Output"
    ```
    {
        class_results: [
            "Purine alkaloids"
        ],
        superclass_results: [
            "Pseudoalkaloids"
        ],
        pathway_results: [
            "Alkaloids"
        ],
        isglycoside: false,
        fp1: [
            0,
            0
            ...
        ],
        fp2: [
            0,
            0,
            ...
        ]
    }
    ```

!!! note "NPClassifier" 
    NPClassifier is A Deep Neural Network-Based Structural Classification Tool for Natural Products - check it out [here](https://npclassifier.gnps2.org/). For citation: Kim, Hyun Woo, Mingxun Wang, Christopher A. Leber, Louis-Félix Nothias, Raphael Reher, Kyo Bin Kang, Justin JJ van der Hooft, Pieter C. Dorrestein, William H. Gerwick, and Garrison W. Cottrell. "NPClassifier: A deep neural network-based structural classification tool for natural products." Journal of Natural Products (2020). [https://doi.org/10.1021/acs.jnatprod.1c00399](https://pubs.acs.org/doi/abs/10.1021/acs.jnatprod.1c00399?casa_token=MRiUf8bJSAcAAAAA:2543Xv_7W0c-AyhntroXm62ccn0QL6c8CpxT0U6NnDoj3JpB1T6Wlr5G96Rfucmnoi2yR0XFgbp2Sw). Checkout the tool index for a large scale workflow for batch classification. 


### Structure Image

```
https://structure.gnps2.org/structureimg?smiles=<smiles string>
```

[Example](https://structure.gnps2.org/structureimg?smiles=Cn1c(=O)c2c(ncn2C)n(C)c1=O)


### Structure Similarity

```
https://structure.gnps2.org/structuresimilarity?smiles1=<smiles string>&smiles2=<smiles string>
```

[Example](https://structure.gnps2.org/structuresimilarity?smiles1=Cn1c(=O)c2c(ncn2C)n(C)c1=O&smiles2=Cn1c(=O)c2c(ncn2C)n(C)c1=O)

!!! warning
    Please make sure you are URL encoding your SMILES/InChI strings or else the web server on the other end won't understand your request. 

### Structure External Resource information

```
https://external.gnps2.org/structureproxy?smiles=<smiles string>
```
[Example - Caffeine](https://external.gnps2.org/structureproxy?smiles=CN1C(N(C)C(N%3DCN2C)%3DC2C1%3DO)%3DO&inchi=InChI%3D1S%2FC8H10N4O2%2Fc1-10-4-9-6-5(10)7(13)12(3)8(14)11(6)2%2Fh4H%2C1-3H3)
    
!!! note "Chemical Translation Service" 
    This API uses the Chemical Translation Service made by the Fiehn Lab - check it out [here](http://cts.fiehnlab.ucdavis.edu/). For citation: Gert Wohlgemuth, Pradeep Kumar Haldiya, Egon Willighagen, Tobias Kind, Oliver Fiehn, The Chemical Translation Service—a web-based tool to improve standardization of metabolomic reports, Bioinformatics, Volume 26, Issue 20, 15 October 2010, Pages 2647–2648, [https://doi.org/10.1093/bioinformatics/btq476](https://doi.org/10.1093/bioinformatics/btq476).

!!! warning
    Please make sure you are URL encoding your SMILES/InChI strings or else the web server on the other end won't understand your request. 


## ReDU

### Per File Sample Information Query

```
https://redu.ucsd.edu/filename?query=<File full path in MassIVE>
```

[Example](https://redu.ucsd.edu/filename?query=f.MSV000082048/ccms_peak/Plate_28/30_84.mzML)


## Page Contributions

{{ git_page_authors }}
