# GNPS API Overview

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

### Structure Image

```https://gnps-structure.ucsd.edu/structureimg?smiles=<smiles string>```

[Example](https://gnps-structure.ucsd.edu/structureimg?smiles=Cn1c(=O)c2c(ncn2C)n(C)c1=O)
