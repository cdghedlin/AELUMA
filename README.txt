 
WHAT THIS IS

AELUMA (Automated Event Location Using a Mesh of Arrays) is a detection and location method, developed by de Groot-Hedlin and Hedlin (2015).
 
This algorithm allows division of a sufficiently dense network such as the Transportable Array (TA) component of the USArray/EarthScope project into a mesh of three-element arrays (triads). The data is usually processing incoherently, that is, using envelopes rather than waveform data. The code has been recently updated to allow analysis of arrays, ie where stations are dense enough that they can be processed coherently. The update also allows for multiple frequencies to be processed at once.


HOW TO USE IT

The code requires MATLAB to run it
PACKAGES:
    MATLAB: https://www.mathworks.com/
       - this bundle was tested under MATLAB R2020a

how to install
	unzip the AELUMAcode_repository.zip file
	************ the main codes are in the /bin folder ******************

The AELUMA approach is a two step approach

for network-only data
Triad_detections(requestedYear,requestedJulDay) detects signals
Triad_locateSources(requestedYear,requestedJulDay) does event association and finds sources

for array-only data
Array_detections(requestedYear,requestedJulDay) detects signals at arrays
Array_locateSources(requestedYear,requestedJulDay) does event association and finds sources

or, to combine network and array detections, do the following:
Triad_detections(requestedYear,requestedJulDay)
Array_detections(requestedYear,requestedJulDay) detects signals at arrays
LocateSources(requestedYear,requestedJulDay) does event association and finds sources

**************************************************************************************************
**************************************************************************************************


NOTE: the code has been set up so that in a matlab window, and in the /bin directory, type
run_Triads		% this will download DMC data and process it. See output in /data folder

**************************************************************************************************
**************************************************************************************************


TO UNDERSTAND IT BETTER 

see AELUMA_userManual.pdf 

REFERENCES:
*******  application to infrasound data *******
- Catherine D. de Groot-Hedlin and Michael A.H. Hedlin, 2015, A method for detecting and locating geophysical events using groups of arrays, 
  Geophys. J. Int. 2015 203: 960-971,doi:10.1093/gji/ggv345.

*******  application to seismic data *******
de Groot-Hedlin, C. D. & Hedlin, M. A., 2018. A new automated approach to detecting and locating seismic events using data from a large network, Bull. Seism. Soc. Am., DOI: 10.1785/0120180072.

*******  application to seismic surface wave data *******
Fan, W., de Groot-Hedlin, C.D., Hedlin, M.A.H.,, Zhitu M., 2018, Using surface waves recorded by a large mesh of three-element arrays to detect and locate disparate seismic sources, Geophys. J. Int., 215, 942-958,  https://doi.org/10.1093/gji/ggy316. 
