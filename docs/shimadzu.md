## Shimazdu Gotchas

### Conversion using machine software
1. Select files needing to be converted
2. Right click on files and select convert. This will open a window allowing you to choose the file type you want to change them to (e.g. mzML for later GNPS deconvolution)

If this does not work, try the solution below

### Conversion

1. OpenChrom convert to mzXML
1. MSConvert mzXML to mzML

This gets around an issue where Shimazdu likes to write retention times in milliseconds and pymzML does not read it. 
