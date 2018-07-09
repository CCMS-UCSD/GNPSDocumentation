GNPS supports the analysis of tandem mass (MS/MS or MS2) data. Below are additional guidelines that describe the kinds of data that GNPS's analysis tools and shared knowledgebase handle.

<!-- To check whether your data file is appropriate for GNPS, check out our [GNPS QC Checker](TODO). -->

## Ionization Type

GNPS supports data from soft ionization sources, e.g. electro spray ionization (ESI), Atmospheric-pressure chemical ionization (APCI), Matrix-assisted laser desorption/ionization (MALDI).

## Fragmentation

GNPS only accepts data dependent acquisition data (DDA), i.e. molecules were fragmented with collision induced dissociation (CID), Higher-energy collisional dissociation (HCD), or Electron-transfer dissociation (ETD). This produces tandem mass spectra (MS/MS) that can be identified via spectral library search and organized into families of molecules with molecular networking.

## Data Sizes

GNPS was designed to process MS/MS datasets of entire LC/MS runs. Many of the analysis tools were meant for datasets with at least hundreds of MS/MS spectra. While it is feasible to analyze a small amount of MS/MS spectra, certain capabilities (e.g. Molecular Networking) will not be effective at such small scales.

For extremely small datasets (e.g. single MS/MS spectra), we recommend utilizing our [single spectrum search](singlespectrum.md) tool and not molecular networking.

For datasets that at least include an entire LC/MS run of MS/MS spectra, all workflows will accept. For molecular networking, please refer to the parameters and [presets](networking.md#Parameter Presets).

## File Formats

Mass spectrometry files must be converted from proprietary vendor formats to open file formats. GNPS currently support .mzXML, .mzML, and .mgf formats for analysis. To convert, please see our [conversion guide](fileconversion.md).

Our tools do NOT support .mzData, .xml, .raw, .RAW, .wiff, .scan, .d, and .cdf formats.
