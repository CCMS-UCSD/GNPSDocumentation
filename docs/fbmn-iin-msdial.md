# IIN with MS-DIAL

## Introduction

In MS-DIAL can process LC-MS/MS data performed in non-targeted mode, but also in MSE and now with Ion Mobility Spectrometry. After the processing the Supplementary Pairs file can be exported and used for IIN.

## Development and Installation

Download the latest version of MS-DIAL software at [http://prime.psc.riken.jp/Metabolomics_Software/MS-DIAL](http://prime.psc.riken.jp/Metabolomics_Software/MS-DIAL).

## Citations

This work builds on the efforts of our many colleagues, please cite their work:

**For IIMN**: Schmid R., Petras D., Nothias LF, et al. [Ion Identity Molecular Networking for mass spectrometry-based metabolomics in the GNPS Environment](https://www.nature.com/articles/s41467-021-23953-9). Nat. Comm. 12, 3832 (2021).

**For FBMN**: Nothias, L.-F., Petras, D., Schmid, R. et al. [Feature-based molecular networking in the GNPS analysis environment](https://www.nature.com/articles/s41592-020-0933-6). Nat. Methods 17, 905–908 (2020).

**For GNPS**: Wang, M. et al. [Sharing and community curation of mass spectrometry data with Global Natural Products Social Molecular Networking](https://doi.org/10.1038/nbt.3597). Nat. Biotechnol. 34, 828–837 (2016).

**For MS-DIAL** 1): Tsugawa, H., Cajka, T., Kind, T., Ma, Y., Higgins, B., Ikeda, K., Kanazawa, M., VanderGheynst, J., Fiehn, O. & Arita, M. [MS-DIAL: data-independent MS/MS deconvolution for comprehensive metabolome analysis.](http://dx.doi.org/10.1038/nmeth.3393) Nature Methods 12, 523-526 (2015).

**For MS-DIAL** 2): Lai, Z., Tsugawa, H., Wohlgemuth, G., Mehta, S., Mueller, M., Zheng, Y., Ogiwara, A., Meissen, J., Showalter, M., Takeuchi, K., Kind, T., Beal, P., Arita, M. & Fiehn, O. [Identifying metabolites by integrating metabolome databases with mass spectrometry cheminformatics.](http://dx.doi.org/10.1038/nmeth.4512) Nature Methods 15, 53-56 (2018).

## Running the FBMN IIN workflow with MS-DIAL

The integration of MS-DIAL and IIN is supported since version 4.1 and support for FBMN from version 2.99. After a standard processing data with MS-DIAL, the “Alignment results” can be exported for IIN analysis.

**Step 1**: Process your non-targeted LC-MS/MS data with MS-DIAL following the [FBMN documentation guidelines](featurebasedmolecularnetworking-with-ms-dial.md).

**Step 2**: After processing your data export the Supplementary Annotation/Pairs files from the "Alignement results" using the option “GNPS export” and “Export GNPS edge files”.

**Step 3**: Run a FBMN job and add the Supplementary Pairs file following the [main IIN documentation](fbmn-iin.md)
[See an example of job with IIN job with MS-DIAL](https://gnps.ucsd.edu/ProteoSAFe/status.jsp?task=ae661056ca1d4b119c0be48d83ec8150)

For visualizing results in Cytoscape. Please refer to the [main FBMNxIIN documentation](fbmn-iin.md).

## Tutorials

See our [MS-DIAL tutorial](tutorials/americangut-ms-dial.md) on using Feature Based Molecular Networking for the American Gut Project sample.


## TO DO NOTES
- Screenshots when new release available
- Batch file for the export ?
- Cytoscape documentation
- Tutorial IIN

## Acknowledgements

This integration was made possible by Hiroshi Tsugawa (Riken).

## Page Contributions

{{ git_page_authors }}
