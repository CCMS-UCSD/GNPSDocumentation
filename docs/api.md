# GNPS API Overview

## GNPS Library Spectra

### All Public Library Spectra at GNPS

```https://gnps-external.ucsd.edu/gnpslibraryjson```

### All Public Library Specta at GNPS with Peaks and Annotation History

```https://gnps-external.ucsd.edu/gnpslibrary/ALL_GNPS.json```

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

```https://gnps-external.ucsd.edu/gnpslibrary/ALL_GNPS.mgf```

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

```https://gnps-external.ucsd.edu/gnpslibrary/ALL_GNPS.msp```


### Single Library Spectrum

```https://gnps.ucsd.edu/ProteoSAFe/SpectrumCommentServlet?SpectrumID=<Library Accession>```

[Example](https://gnps.ucsd.edu/ProteoSAFe/SpectrumCommentServlet?SpectrumID=CCMSLIB00005463737)

## GNPS Jobs

### Job Results API

GNPS job results page in JSON format:

```https://gnps.ucsd.edu/ProteoSAFe/result_json.jsp?task=<task id>&view=<view name>```

[Example](https://gnps.ucsd.edu/ProteoSAFe/result_json.jsp?task=1ad7bc366aef45ce81d2dfcca0a9a5e7&view=view_all_annotations_DB)

## Structure Conversion

### Conversion to Smiles

```https://gnps-structure.ucsd.edu/smiles?inchi=<inchi string>```

[Example](https://gnps-structure.ucsd.edu/smiles?inchi=InChI=1S/C8H10N4O2/c1-10-4-9-6-5(10)7(13)12(3)8(14)11(6)2/h4H,1-3H3)

### Conversion to InChI

```https://gnps-structure.ucsd.edu/inchi?smiles=<smiles string>```

[Example](https://gnps-structure.ucsd.edu/inchi?smiles=Cn1c(=O)c2c(ncn2C)n(C)c1=O)

### Conversion to InChIKey

```https://gnps-structure.ucsd.edu/inchikey?smiles=<smiles string>```

[Example](https://gnps-structure.ucsd.edu/inchikey?smiles=Cn1c(=O)c2c(ncn2C)n(C)c1=O)

### Conversion to exact mass

```https://gnps-structure.ucsd.edu/structuremass?smiles=<smiles string>```

[Example](https://gnps-structure.ucsd.edu/structuremass?smiles=Cn1c(=O)c2c(ncn2C)n(C)c1=O)

### Conversion to formula

```https://gnps-structure.ucsd.edu/formula?smiles=<smiles string>```

[Example](https://gnps-structure.ucsd.edu/formula?smiles=Cn1c(=O)c2c(ncn2C)n(C)c1=O)

### Structure Classyfire

If you have Smiles

```https://gnps-structure.ucsd.edu/classyfire?smiles=<smiles string>```

[Example](https://gnps-structure.ucsd.edu/classyfire?smiles=Cn1c(=O)c2c(ncn2C)n(C)c1=O)

If you have InChI

```https://gnps-structure.ucsd.edu/classyfire?inchi=<InChI string>```

[Example](https://gnps-structure.ucsd.edu/classyfire?inchi=InChI=1S/C8H10N4O2/c1-10-4-9-6-5(10)7(13)12(3)8(14)11(6)2/h4H,1-3H3)

If you have InChI Key

```https://gnps-classyfire.ucsd.edu/entities/<InChI Key>.json```

[Example](https://gnps-classyfire.ucsd.edu/entities/RYYVLZVUVIJVGH-UHFFFAOYSA-N.json)

Additionally, in case the inchikey is not classified, you can provide ```smiles``` or ```inchi``` arguments for 
us to push to the Wishart servers to classify. 


### Structure Image

```https://gnps-structure.ucsd.edu/structureimg?smiles=<smiles string>```

[Example](https://gnps-structure.ucsd.edu/structureimg?smiles=Cn1c(=O)c2c(ncn2C)n(C)c1=O)


## ReDU

### Per File Sample Information Query

```https://redu.ucsd.edu/filename?query=<File full path in MassIVE>```

[Example](https://redu.ucsd.edu/filename?query=f.MSV000082048/ccms_peak/Plate_28/30_84.mzML)

## GNPS Continuous ID Data

If you want to download all public datasets that have been processed by GNPS. You can find a dump of all these files in this dataset [MSV000084314](https://gnps.ucsd.edu/ProteoSAFe/result.jsp?task=25cc4f9135c6428aabe1f41a9e54c369&view=advanced_view). 

This includes:

1. Clustered MGFs for each dataset
1. Identifications for clustered spectra
1. Mapping of clusters back to original files and scans
1. Molecular Networks for each dataset
