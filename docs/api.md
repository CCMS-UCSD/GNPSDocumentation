# GNPS API Overview

## GNPS Library Spectra

### All Public Library Spectra at GNPS

```https://gnps-external.ucsd.edu/gnpslibraryjson```

### All Public Library Specta at GNPS with Peaks and Annotation History

```https://gnps-external.ucsd.edu/gnpslibrary/ALL_GNPS.json```

As MGF

```https://gnps-external.ucsd.edu/gnpslibrary/ALL_GNPS.mgf```

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

### Conversion to monoisotopic mass

```https://gnps-structure.ucsd.edu/structuremass?smiles=<smiles string>```

[Example](https://gnps-structure.ucsd.edu/structuremass?smiles=Cn1c(=O)c2c(ncn2C)n(C)c1=O)

### Conversion to formula

```https://gnps-structure.ucsd.edu/formula?smiles=<smiles string>```

[Example](https://gnps-structure.ucsd.edu/formula?smiles=Cn1c(=O)c2c(ncn2C)n(C)c1=O)

### Structure Classyfire

If you have Smiles or InChI

```https://gnps-structure.ucsd.edu/classyfire?smiles=<smiles string>```

[Example](https://gnps-structure.ucsd.edu/classyfire?smiles=Cn1c(=O)c2c(ncn2C)n(C)c1=O)

If you have InChI Key

```https://gnps-classyfire.ucsd.edu/entities/<InChI Key>.json```

[Example](https://gnps-classyfire.ucsd.edu/entities/RYYVLZVUVIJVGH-UHFFFAOYSA-N.json)


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
