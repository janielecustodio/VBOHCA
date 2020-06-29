# VBOHCA
Online Supplement -- Spatiotemporal Data Set for Out-of-Hospital Cardiac Arrests (Custodio and Lejeune, 2020)

## How to use these files
The files provided in this repository are the online supplement to the paper *Spatiotemporal Data Set for Out-of-Hospital Cardiac Arrests (Custodio and Lejeune, 2020)*. The files have been generated to cover OHCA incidents recorded by the city of Virginia Beach from January 1, 2017 to June 30, 2019. However, the SAS program provided in this repository can be used to process data for different time periods, depending on the files uploaded to the folder *input*.

## Folders
### auxiliary
Stores auxiliary SAS data files.
### input
Stores input data files, obtained from the [Open VB data portal](https://data.vbgov.com/). Users must download three data files, which should be saved as .xslx: EMS_Calls_For_Service, Fire_Calls_For_Service, and Police_Calls_For_Service. These files are processed in the SAS program, which generates the OHCA occurrences for a given time period. Details of the analysis can be found in the aforementioned paper (Custodio and Lejeune, 2020)

### Random Sample
Contains a random sample generated using the MATLAB code available with this package.
### Shortest Paths
The folder "Shapefiles" shapefiles used to calculate the shortest paths using the road distances. Input files were obtained from the [VB Open GIS portal](https://gis.data.vbgov.com/) and [US Census Bureau](https://data.gov/organization/census-gov/). The QGIS Project VBOHCA contains the map used in the analysis.

## Random Sample Generation
The MATLAB file test_cases.m can be used to generate random instances from the VBOHCAR data set.

## Virginia Beach OHCA Dispatch Data Set (VBOHCAR)
The Excel file VBOHCAR.xlsx contains the final data set of all OHCAs registered in the city of Virginia Beach from January 1, 2017, until June 30, 2019. 
- OHCAs: contains the spatiotemporal information about all dispatches made by either the EMS, Fire or Police department for the city of Virginia Beach that were initially classified as an OHCA.
- Base_Stations: contains the spatial information for all the first-responder stations in the city of Virginia Beach.
- Distances: contains both the Haversine and the road distances for each OHCA-Base station pair.

## Data Processing
The SAS file data_consolidation.sas was used to clean and analyze the raw input data sets and to generate the list of OHCAs and response times, as well as spatial information for each OHCA occurrence.



