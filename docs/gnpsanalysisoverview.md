This highlights all the current production analysis tools at GNPS as well as some exciting up and coming tools in development.

## Recommended Analysis Tools

### [Molecular Networking](networking.md)

Molecular networks are visual displays of the chemical space present in tandem mass spectrometry (MS/MS) experiments. This approach groups sets of spectra from related molecules (known as molecular families) even when the spectra themselves are not identified (do not match to any known compounds).

Molecular networks in GNPS represents each spectrum as a node, and spectrum-to-spectrum alignments as edges (similar fragmentation implying similar structure) between nodes. Nodes can be supplemented with metadata, including library matches matches or information that is provided by the user, e.g. abundance, origin of product, hydrophobicity, etc. These metadata attributes can be reflected in a node’s size or color.

### [Spectral Library Search](librarysearch.md)

MS/MS data is searched against reference GNPS spectral libraries in a high throughput manner, scaling up to hundreds of files at a time. The spectral library search can be configured to either match exactly to known molecules or utilize variable dereplication to identify putative analogs of known compounds.

### [MetBLAST](metblast.md)

Query a single MS/MS spectrum across all public GNPS datasets. The mass spectrometry equivalent of NCBI BLAST helps to put the query spectrum in context of where else it occurs as well as search a single MS/MS spectrum against all public spectral libraries.

## Advanced Analysis Tools

### [Dereplicator](dereplicator.md)

The Insilico Peptidic Natural Products Dereplicator is a bioinformatic tool that allows the annotation of known peptidic natural products in MS/MS data using in silico fragmentation tree.

### [Network Annotation Propogation](nap.md)

Network Annotation Propagation (NAP) uses spectral networks to propagate information from spectral library matching, in order to improve in silico fragmentation candidate structure ranking.

## Analysis Tools in Active Development

### [Feature Based Molecular Networking](featurebasedmolecularnetworking.md)

Feature Based Molecular Networking relies on feature detection to determine molecule abundances and aligns these abundances across a cohort of samples into consensus features. Corresponding MS/MS spectra are assigned to each consensus feature and analyzed with spectral library search and molecular networking. This approach enables

1. More accurate quantification of molecules
2. Resolution of isomeric compounds
3. Reduction of redundancy of MS/MS molecules

### [MS2LDA](ms2lda.md)

MS2LDA is a method for the decomposition of sets of molecular fragment data derived from large metabolomics experiments. Check out the MS2LDA website [here](http://ms2lda.org/). At GNPS, we have worked with the MS2LDA team to curate a set of motifs that can help to annotate your MS/MS spectra.
