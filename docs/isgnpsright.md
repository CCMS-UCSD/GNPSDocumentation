# Ionization Type

GNPS supports data from soft ionization sources, e.g. electro spray ionization (ESI), Atmospheric-pressure chemical ionization (APCI), Matrix-assisted laser desorption/ionization (MALDI).

# Fragmentation

GNPS only accepts data dependent acquisition data (DDA), i.e. molecules were fragmented with collision induced dissociation (CID), Higher-energy collisional dissociation (HCD), or Electron-transfer dissociation (ETD). This produces tandem mass spectra (MS/MS) that can be identified via spectral library search and organized into families of molecules with molecular networking.

# File Formats

Mass spectrometry files must be converted from proprietary vendor formats to open file formats. GNPS currently support mzXML, mzML, and mgf formats for analysis. To convert, please see our [conversion guide](fileconversion.md). 
