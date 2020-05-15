# GNPS Tool Index

This is a global tool index for GNPS. Throughout this documentation we have very detailed information for how to use way more tools than we though we'd have, but its a good problem to have!

However, we recognize it might be difficult for people to simply see what all is availble in GNPS as tool and web services. This table is always evolving and hope to make it easier for people to navigate. 

Please help us fill in more completely!

Last changed: {{ git_revision_date }}

## GNPS Workflows

| Category  | Workflow  | GNPS Link  | Beta Link  | Documentation | Source Code | Citation | 
|---|---|---|---|---|---|---|
| Networking | Molecular Networking  | [Workflow](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22METABOLOMICS-SNETS-V2%22,%22library_on_server%22:%22d.speclibs;%22%7D)  | [Workflow](https://proteomics2.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22METABOLOMICS-SNETS-V2%22,%22library_on_server%22:%22d.speclibs;%22%7D) | [Documentation](networking.md) | [Github](https://github.com/CCMS-UCSD/GNPS_Workflows/tree/master/metabolomics-snets-v2) | [Citation](https://www.nature.com/articles/nbt.3597) |
| Networking | Feature-Based Molecular Networking  | [Workflow](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22FEATURE-BASED-MOLECULAR-NETWORKING%22,%22library_on_server%22:%22d.speclibs;%22%7D)   | [Workflow](https://proteomics2.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22FEATURE-BASED-MOLECULAR-NETWORKING%22,%22library_on_server%22:%22d.speclibs;%22%7D) |
| Networking | Merge Polarity Networks  | [Workflow](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22MERGE_NETWORKS_POLARITY%22%7D)   | [Workflow](https://proteomics2.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22MERGE_NETWORKS_POLARITY%22%7D) | 
| Networking | MS2LDA Motif DB  | [Workflow](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22MS2LDA_MOTIFDB%22%7D)   | [Workflow](https://proteomics2.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22MS2LDA_MOTIFDB%22%7D) | [Documentation](ms2lda.md) |  [Github-ms2lda](https://github.com/sdrogers/lda), [Github-ms2ldaviz](https://github.com/sdrogers/ms2ldaviz)  | [Citation-ms2lda](https://www.pnas.org/content/113/48/13738), [Citation-ms2ldaviz](https://academic.oup.com/bioinformatics/article/34/2/317/4158166) |
| Networking | MolNetEnhancer / MetaboDistTree  | [Workflow](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22MOLNETENHANCER%22%7D)   | [Workflow](https://proteomics2.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22MOLNETENHANCER%22%7D) | [Documentation](molnetenhancer.md)|  [Github-MolNetEnhancer](https://github.com/madeleineernst/pyMolNetEnhancer), [Github-MetaboDistTrees](https://github.com/madeleineernst/MetaboDistTrees) | [Citation](https://www.mdpi.com/2218-1989/9/7/144) |
| Data Analysis | MASST  | [Workflow](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22SEARCH_SINGLE_SPECTRUM%22,%22library_on_server%22:%22d.speclibs;%22%7D)   | [Workflow](https://proteomics2.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22SEARCH_SINGLE_SPECTRUM%22,%22library_on_server%22:%22d.speclibs;%22%7D) |[Documentation](https://ccms-ucsd.github.io/GNPSDocumentation/masst/)|---|[Citation](https://www.nature.com/articles/s41587-019-0375-9)|
| Data Analysis | Microbiome-Metabolomics Association - mmvec  | [Workflow - Inactive](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22MMVEC%22%7D)   | [Workflow](https://proteomics2.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22MMVEC%22%7D) |---|
| Annotation | Large Scale Library Search  | [Workflow](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22MOLECULAR-LIBRARYSEARCH-V2%22,%22library_on_server%22:%22d.speclibs;%22%7D)   | [Workflow](https://proteomics2.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22MOLECULAR-LIBRARYSEARCH-V2%22,%22library_on_server%22:%22d.speclibs;%22%7D) |---| 
| Annotation | Library Search/Molecular Networking GC  | [Workflow](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22MOLECULAR-LIBRARYSEARCH-GC%22%7D)   | [Workflow](https://proteomics2.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22MOLECULAR-LIBRARYSEARCH-GC%22%7D) |
| Annotation | Network Annotation Propogation (NAP) | [Workflow](https://proteomics2.ucsd.edu/ProteoSAFe/?params=%7B%22workflow%22:%22NAP_CCMS2%22%7D) | --- | [Documentation](nap.md) | [GitHub](https://github.com/DorresteinLaboratory/NAP_ProteoSAFe/) | [Citation](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1006089) |
| Annotation | Sirius - Bocker Lab | [Workflow](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22SIRIUS%22%7D)   | [Workflow](https://proteomics2.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22SIRIUS%22%7D) |
| Annotation | Qemistree | [Workflow](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22QEMISTREE%22%7D)   | [Workflow](https://proteomics2.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22QEMISTREE%22%7D) |
| Annotation | Dereplicator | --- | --- |
| Annotation | Dereplicator+ | --- | --- |
| Annotation | MetaMiner | --- | --- |
| Data Processing | MSHub-GC Deconvolution  | [Workflow](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B"workflow":"MSHUB-GC"%7D)   | [Workflow](https://proteomics2.ucsd.edu/ProteoSAFe/index.jsp?params=%7B"workflow":"MSHUB-GC"%7D) | 
| Data Processing | OpenMS Feature Detector for FBMN - Future Feature  | [Workflow]()   | [Workflow]() |---|
| Data Processing | LC - MZMine2 | [Workflow](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22LC_MZMINE2%22%7D) | [Workflow](https://proteomics2.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22LC_MZMINE2%22%7D) |
| Data Processing | MSMS-Chooser  | [Workflow](https://gnps.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22MSMS-CHOOSER%22%7D)   | [Workflow](https://proteomics2.ucsd.edu/ProteoSAFe/index.jsp?params=%7B%22workflow%22:%22MSMS-CHOOSER%22%7D) |[Documentation](https://ccms-ucsd.github.io/GNPSDocumentation/msmschooser/)| [Github](https://github.com/CCMS-UCSD/GNPS_Workflows/tree/master/msms-chooser) |[Citation](https://onlinelibrary.wiley.com/doi/abs/10.1002/rcm.8725)| 


## GNPS Web Tools


| Tool  | Documentation | Source Code | Citation |
|---|---|---|---|
| [ReDU](https://redu.ucsd.edu/) | [Documentation](https://mwang87.github.io/ReDU-MS2-Documentation/) | [GitHub](https://github.com/mwang87/ReDU-MS2-GNPS) | [Citation](https://www.biorxiv.org/content/10.1101/750471v1)|
| [GNPS Structure Server](https://gnps-structure.ucsd.edu/) | Structure processing worker | TODO! |
| [GNPS Quickstart/Batch Validator](https://gnps-quickstart.ucsd.edu) | TODO | TODO |
| [GNPS Cytoscape](https://gnps-cytoscape.ucsd.edu) | TODO | TODO |
| [GNPS MASST](https://masst.ucsd.edu) | [Documentation](https://ccms-ucsd.github.io/GNPSDocumentation/masst/) | TODO | [Citation](https://www.nature.com/articles/s41587-019-0375-9)|
| [Metabolomics Spectrum Resolver](https://metabolomics-usi.ucsd.edu) | TODO | TODO |
| [Qemistree Dashboard](https://qemistree.ucsd.edu) | TODO | TODO |
| [GNPS Networking URL Formatter](https://gnps-urlworkflow.herokuapp.com/) | TODO | TODO |
| [GNPS Task Esquisse Server (Beta)](http://dorresteintesthub.ucsd.edu:8347/) | TODO | TODO |
| [GNPS Result View Esquisse Server (Super Beta)](http://dorresteintesthub.ucsd.edu:8359/) | TODO | TODO |
| [GNPS Text Esquisse Server (Super Beta)](https://gnps.shinyapps.io/text_entry/) | TODO | TODO |
| [GNPS Library Dash Explorer](http://dorresteinappshub.ucsd.edu:6546/) | TODO | TODO |
| [GNPS Mass Spec Calculator](https://gnps-masscalculator.herokuapp.com/) | TODO | TODO |

## Community Tools GNPS Interfaces with

| Tool  | Publication |
|---|---|
| [MS2LDA.org](http://ms2lda.org/) | [Citation](https://academic.oup.com/bioinformatics/article/34/2/317/4158166) |
| [NPAtlas](https://www.npatlas.org/joomla/) | [Citation](https://pubs.acs.org/doi/10.1021/acscentsci.9b00806) |
| [MIBiG](https://mibig.secondarymetabolites.org/) | [Citation](https://academic.oup.com/nar/article/48/D1/D454/5587631) |
| [ClassyFire](http://classyfire.wishartlab.com/) | [Citation](https://jcheminf.biomedcentral.com/articles/10.1186/s13321-016-0174-y) |
| [SMART NMR](http://smart.ucsd.edu) | [Citation](https://pubs.acs.org/doi/abs/10.1021/jacs.9b13786) |
| MassBank | [Citation](https://onlinelibrary.wiley.com/doi/full/10.1002/jms.1777?casa_token=Wr51kpu9hCgAAAAA%3AERBV24GFextLVnW0J4SDcdJAskSYG2eqf2tgh8AUBeowVLnKBErbLqJxEzOQJUz2MqrI5dKr47zSVXw) | 

## GNPS Tools Interoperability Graph

[![](https://mermaid.ink/img/eyJjb2RlIjoiZ3JhcGggVERcblx0QShMQyBNUy9NUyBWZW5kb3IgTWFzcyBTcGVjdHJvbWV0cnkgRGF0YSkgLS0-IEJbTVNDb252ZXJ0XVxuXHRBIC0tPiBDW0dOUFMgUXVpY2tzdGFydF1cblx0QyAtLT4gRChPcGVuIG16TUwgRm9ybWF0KVxuXHRCIC0tPiBEXG5cdEQgLS0-IEVbR05QUyBDbGFzc2ljYWwgTW9sZWN1bGFyIE5ldHdvcmtpbmddXG5cdEQgLS0-IEZbTVptaW5lMiBGZWF0dXJlIEZpbmRpbmddXHRcdFx0XHQiLCJtZXJtYWlkIjp7InRoZW1lIjoiZGVmYXVsdCJ9LCJ1cGRhdGVFZGl0b3IiOmZhbHNlfQ)](https://mermaid-js.github.io/mermaid-live-editor/#/edit/eyJjb2RlIjoiZ3JhcGggVERcblx0QShMQyBNUy9NUyBWZW5kb3IgTWFzcyBTcGVjdHJvbWV0cnkgRGF0YSkgLS0-IEJbTVNDb252ZXJ0XVxuXHRBIC0tPiBDW0dOUFMgUXVpY2tzdGFydF1cblx0QyAtLT4gRChPcGVuIG16TUwgRm9ybWF0KVxuXHRCIC0tPiBEXG5cdEQgLS0-IEVbR05QUyBDbGFzc2ljYWwgTW9sZWN1bGFyIE5ldHdvcmtpbmddXG5cdEQgLS0-IEZbTVptaW5lMiBGZWF0dXJlIEZpbmRpbmddXHRcdFx0XHQiLCJtZXJtYWlkIjp7InRoZW1lIjoiZGVmYXVsdCJ9LCJ1cGRhdGVFZGl0b3IiOmZhbHNlfQ)
