# Evaluating-Changes-in-the-Annual-Emissions-Across-Calgary-Between-2019-and-2023---Jessamyn-Dawson
## Project Overview
This project analysed the changed in the emissions of carbon monoxide (CO), nitrogen dioxide (NO2), fine particulate matter (PM2.5), sulphur dioxide (SO2), and volatile organic compounds (VOCs) across Calgary, Alberta between 2019 and 2023. Emissions data for each pollutant from the Government of Canada's Open Government portal was filtered to only include emissions for Calgary, Alberta and duplicate entries were removed. The emissions data was for each pollutant were interpolated for each year (2019-2023) and then clipped to the City of Calgary boundary. The boundaries for each community in Calgary were then overlayed onto each interpolation to show what the emissions were for each community. These five pollutants were included in this analysis because high concentrations of these pollutants are known to have a significant influence on the health of both humans and the environment. 

## Folder Structure
The "Data" folder contains five zipped folders: "City_Boundary", "Community_District_Boundaries", "Interpolated_Emissions_Rasters", "Processed_Emissions_Data", and "Raw_Emissions_Data". The "City_Boundary" zipped folder contains the unaltered shapefile of the city boundary for Calgary from The City of Calgary's Open Data Portal. The "Community_District_Boundaries" zipped folder contains the unalterd shapefile of the community boundaries in Calgary from The City of Calgary's Open Data Portal. The "Interpolated_Emissions_Rasters" zipped folder contains five sub-folders, each sub-folder contains the interpolated emissions rasters for each of the pollutants for a single year. The "Processed_Emissions_Data" zipped folder also contains five sub-folders, each sub-folder contains the emissions data for a single year stored as five separate CSV files (one file for each pollutant). Lastly, the "Raw_Emissions_Data" zipped folder contains the original emissions datasets from the Government of Canada's Open Government portal. There are five datasets in this folder, one for each year, stored as Excel spreadsheets. The metadata for these datasets is in a sheet inside each of the Excel files. 

The "Final_Maps" folder contains five JPEG files. Each JPEG file is the final map layout for a single pollutant, which visualizes the change in the emissions of the pollutant across Calgary between 2019 and 2023.

## Coordinate Reference System
Calgary 3TM WGS 1984 W114

## Data Sources
#### Emissions Data:
Government of Canada. (2025). Single year data tables by facility – releases, transfers and disposals. [Dataset]. Open Government Portal. Retrieved September 21, 2025, from https://open.canada.ca/data/en/dataset/1fb7d8d4-7713-4ec6-b957-4a882a84fed3.

#### City of Calgary Boundary Layer:
The City of Calgary. (2025a). City Boundary. [Dataset]. Open Calgary. Retrieved October 1, 2025, from https://data.calgary.ca/Base-Maps/City-Boundary/7t9h-2z9s.

#### Community Boundaries in Calgary Layer:
The City of Calgary. (2025b). Community Boundaries. [Dataset]. Open Calgary. Retrieved September 21, 2025, from https://data.calgary.ca/Base-Maps/Community-Boundaries/ab7m-fwn6.

## Processing Steps
The emissions data from the Government of Canada was filtered to only include the emissions of CO, NO2, PM2.5, SO2, and VOC for Calgary, Alberta. Each of the filtered datasets were then carefully reviewed to identify and remove the duplicate entries. Once these datasets had been filtered and had duplicate entries removed, the emissions data for each pollutant were separated into individual sheets in Excel for each year. The datasets were then converted into points in ArcGIS Pro. The emissions point layers, the community boundaries layer, and the boundary of Calgary layer were all projected into the “Calgary 3TM WGS 1984 W114” projected coordinate system. A new polygon layer was created in ArcGIS Pro which encompassed Calgary and the surrounding area. The emissions points were clipped to this polygon so that points just outside of Calgary would be included in the interpolations. The clipped points for each pollutant were then interpolated for each year. The interpolated rasters were then clipped to the city boundary layer for Calgary.

## Contact
If you have any questions or concerns please email me at jessamyn.dawson@ucalgary.ca.
