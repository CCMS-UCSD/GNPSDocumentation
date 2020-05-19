
## Data Privacy

!!! info "Is the data I upload to analyze publicly visible?"
    Data you upload to analyze at GNPS will remain private unless you explicitly make it public. The two ways to make your data public are to create MassIVE datasets that make entire datasets public or add individual annotated MS/MS spectra to GNPS spectral libraries.

!!! info "Will MassIVE datasets that I create be public by default?"
    No, when creating a MassIVE dataset, it is not public by default. On the input form page, you are able to set a password to access the MassIVE dataset. There is a Make Public link to make your dataset open to the public and documentation can be found here here. Such a feature is very useful because users can create a MassIVE dataset prior to publication submission that is private and password protected. The MassIVE dataset link can be provided to reviewers along with the password so to provide better transparency and increase probability of manuscript acceptance.

## Data Organization

!!! info "How does the MassIVE data differ from the GNPS spectral libraries?"
    MassIVE datasets consist of raw data. GNPS spectral libraries consist of spectra that have been individually assigned an identification.

## Spectral Libraries

!!! info "How do I get access to the public spectral libraries?"
    On the select input files popup, click on the shared files tab, and enter speclibs as an import share.

    ![Screenshot](img/faq/shared_libs.png)

!!! info "Can I create my own private spectral libraries?"
    Yes, but it is not recommended and we create these private libraries as a path to making them public. Please [contact](contact.md) administrators for further details.

## Analyzing Data

!!! info "Can I select more than one file at a time for each group in molecular networking?"
    Yes. Within each group you can select multiple files, even folders of spectra. Simply highlight the multiple files/folders you want to select and then add to the appropriate group.

## Mass Spectrometry Types

!!! info "Does GNPS support data independent acquisition (DIA) data types such as MSe and SWATH?"
    GNPS natively does not support these types of data with large isolation windows. We recommend that these data be preprocessed so that individual molecule fragmentation can be deconvoluted with tool such as [DIA-Umpire](http://diaumpire.sourceforge.net/) or Progenesis QI (MSe) and you can find our documentation [here](featurebasedmolecularnetworking-with-progenesisQI.md).

## Browser Support

!!! info "What Browsers Does GNPS Support"
    We officially test on the latest Chrome browser. Other browsers, e.g. Firefox, Internet Explorer, Opera, Edge, are not officially supported but likely will not have any issues with GNPS.

Page Authors: {{ git_page_authors }}