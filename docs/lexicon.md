## GNPS Lexicon

### Molecular Networking

**Molecular networking** : a method that computes pairwise spectral similarity between fragmentation spectra (using a modified cosine score) and visualizes the results as a network. Spectra are represented as &quot;nodes&quot;, and these nodes are connected by &quot;edge&quot; when their pairwise similarities are above a similarity threshold. Groups of connected nodes form a &quot;molecular family&quot;. Two methods exist to generate molecular networks 1) classical molecular networking that is built on the fragmentation spectra level only, and the 2) feature-based molecular networking that is coupled with LC-MS feature detection and alignment.

To disambiguate with the feature-based molecular networking, this method is also called &quot; **classical molecular networking**&quot;.

**Spectral similarity** : refers to the quantitative measurement of the similarity degree between fragmentation spectra. In GNPS, this is done with the cosine score computation between nodes.

**Cosine score** : refers to a normalized dot-product, a mathematical measure of spectral similarity between two fragmentation spectra. A cosine score of 1 represents identical spectra while a cosine score of 0 denotes no similarity at all.

**MS-Cluster** : an algorithm used by GNPS to collapse nearly identical MS spectra with the same precursor ion m/z into a single &quot;consensus&quot; or &quot;clustered&quot; spectrum.

**Spectral cluster:** refers to a fragmentation spectra resulting from the clustering of identical fragmentation spectra. They are also called &quot;clustered&quot;, or &quot;consensus&quot; or &quot;representative&quot; spectrum in the GNPS environment. This is not to be confused with &quot;molecular network cluster&quot; that indicates a molecular or spectral family.

**Molecular family:** a group of fragmentation spectra that have a high similarity degree. In the molecular network, they correspond to group/cluster of connected nodes.

**Feature-based molecular networking (FBMN):** an advanced method for molecular networking that provides accurate ion abundance for statistical analysis and provides support for isomer resolution or ion mobility. FBMN requires the processing of the LC-MS/MS with tools such as MZmine or XCMS, prior to performing molecular networking. More information at: [https://ccms-ucsd.github.io/GNPSDocumentation/featurebasedmolecularnetworking/](featurebasedmolecularnetworking.md).

**Ion Identity Networking:** a workflow that complements the molecular networking (FBMN workflow) by grouping fragmentation spectra using peak shape correlation analysis in addition to spectral similarity. This creates ion identity molecular families by adding new edges. More information at: [https://ccms-ucsd.github.io/GNPSDocumentation/fbmn-iin/](fbmn-iin.md)

**Cytoscape:** a software for network visualization and analysis. Molecular networks from GNPS can be imported in Cytoscape for interpretation. See the following page: [https://ccms-ucsd.github.io/GNPSDocumentation/cytoscape/](cytoscape.md).

**Node table:** a table summarizing molecular network node information (i.e m/z, retention time).

**Edge table:** a table summarizing molecular network edge information (cosine score, delta m/z)

### Data processing - Feature-based molecular networking.

**Data conversion:** the process of converting the mass spectrometry data from a format to another. Many data processing and annotation tools require first to convert vendor format to an open source. More information at: [https://ccms-ucsd.github.io/GNPSDocumentation/fileconversion](fileconversion.md)

**Raw data:** Rawrefers to the &quot;unprocessed&quot; mass spectrometry data, although the spectra are often centroided. These include vendor specific formats (i.e. .raw, .d format) and open format (i.e. mzML).

**Processed data** : refers to data processed with either MS-Cluster in classical molecular networking or when feature detection/alignment was performed with tools such as MZmine/XCMS/OpenMS.

**LC-MS feature** : in the context of LC-MS processing, corresponds to the automated detection of a signal(s) for an ion/compound eluting from the chromatographic separation system and detected by the mass spectrometer. These are empirically referred to as chromatographic peaks.

**Feature detection** : the process of detecting signal(s) of a molecule from mass spectrometry data. In LC-MS/MS, it includes chromatographic peak detection, isotopic grouping, and peak quantification (area under the curve or peak height), and indexing associated fragmentation spectra.

**Feature alignment** : the process of aligning a set of LC-MS features across multiple samples for dataset-wide analysis.

**Feature quantification table:** a table summarizing for each mass spectrometry feature the qualitative (m/z, retention time, adduct type, etc.) and quantitative information (area under the curve, peak height, spectral count).

**Metadata table:** a table summarizing qualitative and experimental information associated with each sample. This table is a prerequisite for using many tools on GNPS. Additional information can be found [here](metadata.md).

### Annotation of fragmentation spectra

**Spectral library search:** the process of matching an experimental fragmentation spectrum (query spectrum) against reference spectra in public or commercial libraries. See more information on GNPS [https://ccms-ucsd.github.io/GNPSDocumentation/librarysearch/](librarysearch.md).

**Passatutto:** a method for estimating false discovery rate (FDR) of spectral match annotation against spectral libraries. More information at[https://www.nature.com/articles/s41467-017-01318-5](https://www.nature.com/articles/s41467-017-01318-5).

**DEREPLICATOR tools:** a dereplication algorithm designed for the annotation of known small peptidic molecules from fragmentation spectra. DEREPLICATOR VarQuest is a variant that can search for novel derivatives of known molecules that are differing by one amino acid residue. More information at: [https://ccms-ucsd.github.io/GNPSDocumentation/dereplicator/](dereplicator.md).

**Network Annotation Propagation (NAP)**: an annotation method for fragmentation spectra that relies on 1) an silico annotation tools (MetFrag), and 2) molecular networks topology, to rerank the list of candidates proposed by MetFrag. More information at: [https://ccms-ucsd.github.io/GNPSDocumentation/nap/](nap.md).

**MS2LDA** : a tool that decomposes molecular fragmentation data derived from large metabolomics experiments into annotated Mass2Motifs. Mass2Motifs refers to fragmentation patterns of co-occurring mass fragment peaks and/or neutral losses that often represent molecular substructures. More information at: [https://ccms-ucsd.github.io/GNPSDocumentation/ms2lda/](ms2lda.md).

**ClassyFire** : a tool that adds chemical class information to structures using a manually curated and hierarchical ontology. More information can be found here: [http://classyfire.wishartlab.com](http://classyfire.wishartlab.com/).

**MolNetEnhancer** : a workflow that combines the outputs from molecular networking and in-silico annotation tools such as MS2LDA, NAP, DEREPLICATOR, and ClassyFire. MolNetEnhancer provides a comprehensive chemical overview by annotating chemical classes for molecular families whilst summarizing structural details for each fragmentation spectrum in the molecular network. More information at **:** [https://ccms-ucsd.github.io/GNPSDocumentation/molnetenhancer/](molnetenhancer.md)

**Metaminer** : a metabologenomic pipeline which integrates fragmentation spectra analysis and biosynthetic gene cluster analysis to identify novel Ribosomally synthesized and Post-translationally modified Peptides (RiPPs) and the biosynthetic gene clusters encoding them. More information at [https://ccms-ucsd.github.io/GNPSDocumentation/metaminer/](metaminer.md).

**Qemistree:** a method that generates a tree of metabolites from fragmentation spectra analysis for enhanced comparison of chemical profiles using chemically-informed distance metrics. More information at: [https://ccms-ucsd.github.io/GNPSDocumentation/qemistree/](qemistree.md)

**ClassyTree** : a chemically-informed distance metric that uses ClassyFire chemical class information for enhanced comparison of chemical profiles. A tree of the annotated metabolites is constructed based on the hierarchy of their respective chemical classes. Using the UniFrac metric, the chemical structural relatedness of the annotated molecules in each sample is thus considered when comparing multiple samples. Samples that contain similar chemical class profiles will end up closer to each other even if the individual molecules are slightly different. The method is not published yet but more information can be found here [[https://ccms-ucsd.github.io/GNPSDocumentation/molnetenhancer/](molnetenhancer.md)] and here [[https://github.com/madeleineernst/MetaboDistTrees](https://github.com/madeleineernst/MetaboDistTrees)].

**MotifTree** : a chemically-informed distance metric that uses MS2LDA substructure information for enhanced comparison of chemical profiles. The substructures found in molecules of each sample are considered when comparing multiple samples, by constructing a tree of metabolites based on shared substructures. Samples that contain similar substructure profiles will end up closer to each other even if the individual molecules are slightly different. The method is not published yet but more information can be found here [[https://ccms-ucsd.github.io/GNPSDocumentation/molnetenhancer/](molnetenhancer.md)] and here [[https://github.com/madeleineernst/MetaboDistTrees](https://github.com/madeleineernst/MetaboDistTrees)].

### GC-MS on GNPS

**GNPS-GC:** anenvironment for GC-MS data processing and annotation on GNPS.

**GC molecular network:** molecular network of &quot;deconvoluted&quot; or &quot;pure&quot; electron ionisation (EI) spectra. It uses a modified version of the cosine score employed in molecular networks for LC-MS/MS.

**GC-MS Deconvolution:** data processing for GC-MS data obtained in electron ionisation (EI) mode. More information at: [https://ccms-ucsd.github.io/GNPSDocumentation/gc-ms-deconvolution/](gc-ms-deconvolution.md).

**MSHub:** a deconvolution algorithm that conducts dataset-wide deconvolution across all provided samples.

### SIRIUS

**SIRIUS:** a software dedicated to the annotation of ions from fragmentation spectra. First, SIRIUS computes candidate molecular formula (MF) by 1) matching the MS1 experimental spectra against the predicted isotopic pattern and 2) establishing how much the fragmentation spectra can be explained by the candidate MFs using fragmentation trees. SIRIUS integrates other algorithms or models such as: ZODIAC for improved MF prediction; CSI:FingerID for putative annotation of structure and COSMIC for establishing the confidence in the match; or CANOPUS for putative chemical class annotation. SIRIUS has an advanced graphical user interface or the tools can be run in command line mode. More informations at: [https://bio.informatik.uni-jena.de/software/sirius/](https://bio.informatik.uni-jena.de/software/sirius/)

**Fragmentation tree (FT): a** method explaining the fragment ions formula in a fragmentation spectrum via fragmentation cascades. SIRIUS uses the FT method for molecular formula prediction. More informations at: [https://jcheminf.biomedcentral.com/articles/10.1186/s13321-016-0116-8](https://jcheminf.biomedcentral.com/articles/10.1186/s13321-016-0116-8)

**Fingerprint:** a vector encoding the chemical or structural properties for a molecule or a fragmentation spectrum. It can be computed directly from the molecular structure with RDKit or CDK libraries.

**CANOPUS:** a method that is part of SIRIUS and that can predict the most likely chemical class for a fragmentation spectrum.

**ZODIAC:** an algorithm for improved _de novo_ (database independent) molecular formula prediction in SIRIUS. More information in the preprint: [https://www.biorxiv.org/content/10.1101/842740v1](https://www.biorxiv.org/content/10.1101/842740v1)

**COSMIC:** a method for computing the significance of the structure proposed by CSI:FingerID annotation. The method is experimental and not published yet.

### The GNPS environment

**GNPS:** a web-based mass spectrometry ecosystem for the processing, annotation, and interpretation of nontargeted metabolomics data. See [https://gnps.ucsd.edu/](https://gnps.ucsd.edu/).

**MassIVE:** a community resource to promote the exchange of mass spectrometry data. See [https://massive.ucsd.edu](https://massive.ucsd.edu/ProteoSAFe/static/massive.jsp) **.** Data from MassIVE can be directly imported into the GNPS environment.

**Proteomics2:** the beta-test server for workflow in development at GNPS. See [proteomics2.ucsd.edu](https://proteomics2.ucsd.edu/)

**ProteoSAFe:** the workflow manager for job scheduling on the cluster from Center of Computational Mass Spectrometry (CCMS) hosting GNPS and MassIVE.

**Quickstart interface:** a simplified web-interface of GNPS that accelerates GNPS job preparation for molecular networking, FBMN, and data conversion/deposition. See [https://gnps-quickstart.ucsd.edu/featurebasednetworking](https://gnps-quickstart.ucsd.edu/featurebasednetworking).

**Continuous identification:** an automatic workflow on GNPS that periodically reanalyses public datasets for novel matches between fragmentation spectra and new spectral library entries. More information at [https://ccms-ucsd.github.io/GNPSDocumentation/continuousid/](continuousid.md).

**Metabolomics Spectrum Identifier Resolver:** a web-server that facilitates the accession and visualization of a defined fragmentation spectrum on a public repository, including GNPS. See [https://metabolomics-usi.ucsd.edu/](https://metabolomics-usi.ucsd.edu/).

**GNPS tags** : refers to community-curated tags associated to a fragmentation spectra in GNPS spectral libraries entries. More information at [https://ccms-ucsd.github.io/GNPSDocumentation/tag\_info/](tag_info.md).

### Datasets wide analysis tools

**ReDU:** an interface for meta-analysis of spectral matches of fragmentation spectra from public datasets available on GNPS.More information at: [https://ccms-ucsd.github.io/GNPSDocumentation/ReDU/](ReDU.md).

**MASST** : a mass spectrometry equivalent of NCBI BLAST. MASST enables querying a given fragmentation spectrum against all fragmentation spectra in public datasets. More information at [https://ccms-ucsd.github.io/GNPSDocumentation/masst/](masst.md).

### Data analysis and multiomics integration

**MetaboAnalyst** : a web-platform that offers a variety of commonly used procedures for metabolomic data processing, normalization, multivariate statistical analysis, as well as data annotation. More information at: [https://www.metaboanalyst.ca/](https://www.metaboanalyst.ca/).

**mmvec:** a method for estimating the conditional probability that each molecule is present given a specific micro-organism or DNA sequence. The method was published in [https://www.nature.com/articles/s41592-019-0616-3](https://www.nature.com/articles/s41592-019-0616-3).

**Qiita** : an open-source web-based platform that enables to carry out microbiome analyses and meta-analyses easily using standardized pipelines such as QIIME2 and GNPS. More information at: [https://qiita.ucsd.edu/](https://qiita.ucsd.edu/).

**Molecular cartography** : a method for the visualization of metabolomics data onto a 3D model. See [https://doi.org/10.1038/nprot.2017.122](https://doi.org/10.1038/nprot.2017.122).

### Molecular Networks Statistics

**Number of Nodes** : After applying the MS-Cluster algorithm and creating different consensus MS2 spectra, each consensus spectra is represented as a node inside the network.

**Number of pairs** : Number of edges or connections inside a network. (Suggest changing for number of edges)

**Number of ID&#39;s clusternodes** : Number of nodes with a consensus mass spectra that has a match with a reference compound found in LC-MS or GC-MS libraries. (Suggest changing for number of annotated nodes)

**Number of ID&#39;s clusternodes not in components:** Number of singlets (nodes without connection) that have a match with a reference compound found in LC-MS or GC-MS libraries. (Suggest changing for number of singlets)

**Number of unidentified neighbors:** Taking as a reference each ID node inside a subnetwork, is the total amount of connected nodes without a match with a reference compound found in LC-MS or GC-MS libraries.

**Number of connected components not single:** Number of subnetworks (spectral families) found in a job. (Suggest changing for number of subnetworks)

**Number of clusternodes in network:** Number of nodes connected to other nodes (not singlets). (Suggest changing for number of nodes inside a subnetwork)

**Number of connected components identified:** Number of subnetworks (spectral families) that have at least one node that have a match with a reference compound found in LC-MS or GC-MS libraries. (Suggest changing for number of subfamilies with at least one annotation)

**Number of clusternodes in identified components:** Total sum of nodes found in the subnetworks (spectral families) that have at least one node that have a match with a reference compound found in LC-MS or GC-MS libraries. (Suggest changing for number of nodes inside a subnetwork that has at least one annotation)

**Number of spectra in consideration:** The total number of fragmentation mass spectra extracted from a GNPS job obtained from LC-MS or GC-MS platforms.

**Number of spectra in network:** The total number of spectra clustered as different nodes inside the network.

**Number of ID&#39;s spectra:** Number of spectra that has a match with a reference compound found in LC-MS or GC-MS libraries.

**Number of ID&#39;s spectra not in components:** Number of spectra clustered as singlets (nodes without connection) that have a match with a reference compound found in LC-MS or GC-MS libraries.
