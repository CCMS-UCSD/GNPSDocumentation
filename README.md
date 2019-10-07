
![logo](docs/img/GNPS_logo_original.png)

# GNPS Documentation GitHub Repository

### Introduction to GNPS
Global Natural Products Social Molecular Networking (GNPS, [http://gnps.ucsd.edu/](https://gnps.ucsd.edu/ProteoSAFe/static/gnps-splash2.jsp)) is a web-based mass spectrometry ecosystem that aims to be an open-access knowledge base for community-wide organization and sharing of raw, processed or identified tandem mass (MS/MS) spectrometry data. GNPS aids in identification and discovery throughout the entire life cycle of data; from initial data acquisition/analysis to post publication.

### Migration to the New Documentation

The GNPSDocumentation can be found at [https://ccms-ucsd.github.io/GNPSDocumentation/](https://ccms-ucsd.github.io/GNPSDocumentation/).

### Contributing to the New Documentation

Help us improving GNPS Documentation !

- For informations/feature request, please open an "Issue" [on the present GitHub repository](https://github.com/CCMS-UCSD/GNPSDocumentation/issues).
- To contribute to the GNPS documentation, fork the [*CCMS-UCSD/GNPSDocumentation*]((https://github.com/CCMS-UCSD/GNPSDocumentation)) repository, and make a "Pull Request" with your edits.

### GNPS Workflows

GNPS Workflows are available on the following repository: [https://github.com/CCMS-UCSD/GNPS_Workflows](https://github.com/CCMS-UCSD/GNPS_Workflows)

### GNPS and MassIVE uptime 

Visualize the status of all GNPS Workflows: [https://stats.uptimerobot.com/Am4PLUWn3](https://stats.uptimerobot.com/Am4PLUWn3)

### Development Setup for Local Development

1. Install miniconda3 (https://docs.conda.io/en/latest/miniconda.html)
2. Create conda environment

```conda create -n mkdocs```

3. Install requirements

```
conda install -c conda-forge mkdocs
conda install -c conda-forge mkdocs-material
pip install mkdocs-minify-plugin
```

4. Serve locally

```mkdocs serve```

5. Deploy to github pages

```mkdocs gh-deploy```


### Citation

Wang, M. et al. Sharing and community curation of mass spectrometry data with Global Natural Products Social Molecular Networking. Nat. Biotechnol. 34, 828–837 (2016). [https://www.nature.com/articles/nbt.3597](https://www.nature.com/articles/nbt.3597)
