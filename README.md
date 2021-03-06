# VBOHCA
Online Supplement -- Spatiotemporal Data Set for Out-of-Hospital Cardiac Arrests (Custodio and Lejeune, 2020)

## How to use these files
The files provided in this repository are the online supplement to the paper *Spatiotemporal Data Set for Out-of-Hospital Cardiac Arrests (Custodio and Lejeune, 2020)*. The files have been generated to cover OHCA incidents recorded by the city of Virginia Beach from January 1, 2017 to June 30, 2019. However, the SAS program provided in this repository can be used to process data for different time periods, depending on the files uploaded to the folder *input*.

## Folders
### auxiliary
Stores auxiliary SAS data files.
### input
Stores input data files, obtained from the [Open VB data portal](https://data.vbgov.com/). Users must upload three data files, which should be saved as .xslx: *EMS_Calls_For_Service*, *Fire_Calls_For_Service*, and *Police_Calls_For_Service*. This repository includes a sample version of the *EMS_Calls_For_Service* obtained through a FOIA request. It also contains a version of the *Fire_Calls_For_Service* and the *Police_Calls_For_Service* data set, which were downloaded from the Open VB data portal. All files cover the period from January 1, 2017 until June 30, 2019. These files are processed using the SAS program, which generates the OHCA occurrences for a given time period. Details of the analysis can be found in the associated paper (Custodio and Lejeune, 2020).

### Random Sample
Contains a random sample generated using the MATLAB code available with this package.

### Shortest Paths
The folder *Shapefiles* shapefiles used to calculate the shortest paths using the road distances for the sample in the folder *Random Sample*. Input files were obtained from the [VB Open GIS portal](https://gis.data.vbgov.com/) and [US Census Bureau](https://data.gov/organization/census-gov/). The QGIS Project file *VBOHCA_Sample1* contains the map used in the analysis.

## Random Sample Generation
The MATLAB file *test_cases.m* can be used to generate random instances from the VBOHCAR data set as it is. If users choose to consider a different time period, the VBOHCAR Excel file must be adjusted so that the sheet *Distances* includes all OHCA occurrences and links to the road distances. Additionally, if a different time period is used, users must also adjust the MATLAB source code so that no errors occur when reading the data sets.

## Virginia Beach OHCA Dispatch Data Set (VBOHCAR)
The Excel file *VBOHCAR.xlsx* contains the final data set of all OHCAs registered in the city of Virginia Beach from January 1, 2017, until June 30, 2019. 
- OHCAs: contains the spatiotemporal information about all dispatches made by either the EMS, Fire or Police department for the city of Virginia Beach that were initially classified as an OHCA.
- Base_Stations: contains the spatial information for all the first-responder stations in the city of Virginia Beach.
- Distances: contains both the Haversine and the road distances for each OHCA-Base station pair.

## Data Processing
The SAS file *data_consolidation.sas* was used to clean and analyze the raw input data sets and to generate the list of OHCAs and response times, as well as spatial information for each OHCA incident. This file can be used to analyze any time period, depending on the input files uploaded to the folder *input*. Users can use the directory *C://Online_Supplement* to save the folders *input* and *auxiliary*. If using a customized directory, users must modify the libnames in the SAS source code so that the correct files are referenced.
