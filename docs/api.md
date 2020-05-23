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
    148.278381	192.0
    175.978806	172.0
    181.814117	216.0
    183.004974	172.0
    186.03038	148.0
    188.050171	172.0
    192.042465	168.0
    198.057724	204.0
    199.137619	160.0
    208.08345	180.0
    211.054138	148.0
    212.984314	180.0
    223.745422	144.0
    226.096741	304.0
    227.089355	184.0
    227.929962	168.0
    237.107498	172.0
    239.103836	180.0
    240.392059	148.0
    248.07663	424.0
    250.617554	224.0
    252.097534	232.0
    254.101929	208.0
    255.051483	176.0
    258.713684	208.0
    260.114624	216.0
    262.224701	140.0
    264.896973	188.0
    265.598755	796.0
    266.095764	308.0
    266.597198	168.0
    268.146362	152.0
    274.068237	148.0
    274.631989	172.0
    275.093262	448.0
    276.081573	316.0
    277.048462	168.0
    277.081573	240.0
    278.106934	160.0
    290.852325	172.0
    293.09906	304.0
    294.087646	180.0
    298.106873	184.0
    301.383972	224.0
    305.165588	164.0
    305.409027	180.0
    309.04776	152.0
    315.221039	192.0
    319.118256	172.0
    319.594879	160.0
    329.184082	168.0
    331.470337	144.0
    333.462769	180.0
    348.304596	196.0
    350.153595	160.0
    354.516907	152.0
    356.911926	216.0
    361.544464	172.0
    363.143311	188.0
    364.149139	160.0
    364.377045	164.0
    364.430267	176.0
    368.365875	144.0
    369.359772	152.0
    387.212524	160.0
    388.174316	1108.0
    389.173737	5696.0
    390.179474	1112.0
    390.261719	168.0
    390.792725	144.0
    391.180298	392.0
    394.737305	184.0
    405.335449	144.0
    405.372314	136.0
    405.983765	160.0
    406.188782	1956.0
    406.681885	160.0
    407.095428	212.0
    407.184631	12956.0
    407.300751	336.0
    407.737061	164.0
    408.116119	172.0
    408.187286	3008.0
    408.235748	324.0
    409.193756	636.0
    409.232056	512.0
    409.347443	156.0
    409.595337	176.0
    410.05249	156.0
    410.196716	144.0
    410.239258	232.0
    410.95401	136.0
    411.052307	96.0
    411.276581	116.0
    448.215485	152.0
    567.454041	152.0
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

If you want to download all public datasets that have been processed by GNPS. You can find the dumps here:

https://gnps.ucsd.edu/ProteoSAFe/result.jsp?task=25cc4f9135c6428aabe1f41a9e54c369&view=advanced_view

This includes:

1. Clustered MGFs for each dataset
1. Identifications for clustered spectra
1. Mapping of clusters back to original files and scans
1. Molecular Networks for each dataset
