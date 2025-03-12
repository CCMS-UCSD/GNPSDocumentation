# Metabolomics Spectrum Resolver

You can find the Metabolomics Spectrum Resolver at [https://metabolomics-usi.gnps2.org/](https://metabolomics-usi.gnps2.org/).

## Universally Resolve MS/MS Data

This tool is meant to be able to show USIs from various sources. It will achieve the following goals:

1. Enable creation of embeddable images in publications that will link out to viewable/interactable spectrum plots.
2. 3rd party embedding for visualization of spectra that exist in repositories (e.g. MassIVE, PRIDE, PeptideAtlas).
3. 3rd party embedding of QR code.

### Data Sources

### Universal Spectrum Identifier

The following are supported

1. GNPS Molecular Networking Clustered Spectra
2. GNPS Spectral Libraries
3. ProteoXchange Repository Data
4. MS2LDA Reference Motifs
5. MassBank Library Spectra
6. MetaboLights Dataset Spectra
7. Metabolomics Workbench Dataset Spectra

Full details on formats of the identifiers can be found at [Link](Github Link). 

## Customization of Visualization

- `mz_min`: Minimum m/z value.
- `mz_max`: Maximum m/z value.
- `annotate_peaks`: Defines which peaks in which spectrum (top or bottom) will be annotated. The parameters is a list of lists of m/z values of the peaks to be annotated. For a single spectrum plot it should be a single nested list (i.e. `[[m1, m2]]`), for a mirror plot it should be two nested lists for the top spectrum and the bottom spectrum (i.e. `[[s1m1,s1m2],[s2m1,s2m2]]`).

## Web API Endpoints

1. /png/
1. /svg/
1. /json/
1. /api/proxi/v0.1/spectra
1. /csv/
1. /qrcode/
1. /spectrum/
1. /mirror/
1. /svg/mirror
1. /png/mirror

## Source Code

Checkout the source code and contribute at [GitHub](https://github.com/mwang87/MetabolomicsSpectrumResolver).

## Page Contributors

{{ git_page_authors }}
