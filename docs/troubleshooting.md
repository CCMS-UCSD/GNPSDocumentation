# Overview

This section addresses some common issues with the analysis workflows at GNPS. If you run into any of these common issues, hopefully this page will give you actionable steps to address them. If this page cannot help you, please refer to the [forum](https://groups.google.com/forum/#!forum/molecular_networking_bug_reports) to help answer your questions.

## Molecular Networking

### Failed Job

"Empty MS/MS". - This means that your input data has no MS/MS spectra. This could mean one of several things

1. The file format input is incorrect. Please make sure it is a [supported file format](fileconversion.md) for GNPS.
2. The mass spectrometry files do not contain MS/MS spectra. These files cannot be analyzed by GNPS.
3. The filtering criteria are too aggressive. Please use an appropriate preset for your data.

"spectral library search exceeded memory" - This means that the spectral library search step used too much memory and had to be terminated. This is likely caused by changing the set of spectral libraries used in search. It is not recommended to change the set of libraries included unless you are an advanced users. Please remove all libraries except for the default "speclibs" and rerun.

"Missing filename in Metadata" - The metadata file included for networking is formatted incorrectly. Please refer to metadata formatting to correct this.

### Results Incorrect

#### No attributes or groups in output

Make sure the metadata file includes the appropriate columns and attributes are prefixed with ATTRIBUTE_ and that the metadata file is a tab separated text file.

## Library Search (Dereplication)

### No Results

1. Check that the parameters are OK...
2. Make sure you have the right format
3. Make sure you have MS/MS spectra in your data

## Single Spectrum Search

A common error is missing intensities for masses. Simply masses are insufficient, intensities are also required.
