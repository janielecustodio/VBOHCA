# VBOHCA
Virginia Beach OHCA -- Online Supplement

## Folders
### auxiliary
Stores auxiliary SAS data files.
### input
Stores input data files, obtained from the [Open VB data portal](https://data.vbgov.com/).
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
