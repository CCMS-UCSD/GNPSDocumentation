
![logo](docs/img/GNPS_logo_original.png)

# GNPS Documentation GitHub Repository

### Introduction to GNPS
Global Natural Products Social Molecular Networking (GNPS, [http://gnps.ucsd.edu/](https://gnps.ucsd.edu/ProteoSAFe/static/gnps-splash2.jsp)) is a web-based mass spectrometry ecosystem that aims to be an open-access knowledge base for community-wide organization and sharing of raw, processed or identified tandem mass (MS/MS) spectrometry data. GNPS aids in identification and discovery throughout the entire life cycle of data; from initial data acquisition/analysis to post publication.

### Contributing to the New Documentation

Help us improving GNPS Documentation !

- For informations/feature request, please open an "Issue" [on the present GitHub repository](https://github.com/CCMS-UCSD/GNPSDocumentation/issues).
- To contribute to the GNPS documentation, simply edit a page and it will prompt for an ad hoc pull request. Its as simple as that. For more advanced editing, fork the [*CCMS-UCSD/GNPSDocumentation*]((https://github.com/CCMS-UCSD/GNPSDocumentation)) repository, and make a "Pull Request" with your edits from your fork to the primary repository.

### GNPS Workflows

GNPS Workflows are available on the following repository: [https://github.com/CCMS-UCSD/GNPS_Workflows](https://github.com/CCMS-UCSD/GNPS_Workflows)

### Development Setup for Local Development

1. Install miniconda3 (https://docs.conda.io/en/latest/miniconda.html)
2. Create conda environment

```conda create -n mkdocs```

3. Install requirements

```
pip install -r requirements.txt
```

4. Serve locally

```mkdocs serve```

5. Deploy to github pages (this is unnecessary as it will automatically deploy once changes are pushed to master)

```mkdocs gh-deploy```


### Build

![](https://github.com/CCMS-UCSD/GNPSDocumentation/workflows/CI/badge.svg)

### Citation

Wang, M. et al. Sharing and community curation of mass spectrometry data with Global Natural Products Social Molecular Networking. Nat. Biotechnol. 34, 828–837 (2016). [https://www.nature.com/articles/nbt.3597](https://www.nature.com/articles/nbt.3597)
