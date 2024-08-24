Data set name:Dataset for spatiotemporal changes and driving mechanism of ecosystem carbon sink in karst peak cluster depression basin in southwest Guangxi based on the interaction of "water-rock-soil-air-biology"

Data set description:This dataset includes carbon sink data from the karst peak cluster depression basin in southwestern Guangxi from 2000 to 2022, as well as codes used in the exploration of driving force mechanisms. Using these data, the study on the carbon sink of the ecosystem in southwestern Guangxi based on the interaction of "water-rock-soil-air-biology" was elucidated. This dataset includes: 1. Climatic data, 2. Karst carbon sink data, 3. Driving force data, 4. Net primary productivity data, 5. Total carbon sink flux, 6. R-code, 7. Matlab code.

Repetition process:
Software: Arcmap 10.8,Rstudio,SPSS,Matlab2018b

Climate data processing work:
1. Precipitation, temperature, and evapotranspiration data are sourced from the EARTHDATA website（ https://www.earthdata.nasa.gov/ ）.
2. In the Arcmap 10.8 software, climate data was processed into annual mean temperature, total precipitation and total evapotranspiration data, and surface runoff was calculated.

Karst carbon sink calculation work:
1. Use the Maximum Potential Dissolution Model to calculate the carbon sequestration of carbonate karst.
2. Use Hartmann model to calculate the carbon sink flux of silicate karst.
3. Use the range clipping calculation results of karst and non karst areas in the research area, and then embed them into a new grid to obtain the karst carbon sink flux data within the research area.

Calculation of vegetation soil carbon sink:
1. The net primary productivity data comes from the MOD17A3H dataset on the USGS website（ https://www.usgs.gov/ ）.
2. Use net ecosystem productivity estimation methods to calculate soil respiration, soil heterotrophic respiration, and net ecosystem productivity.

Calculation of total carbon sink:
Add the net ecosystem productivity and karst carbon sink flux to obtain the total carbon sink flux.

Note: All calculation processes are uniformly carried out using the WGS1984-UTM_Zone48N coordinate system with a resolution of 1km.

Analysis of spatiotemporal trends in carbon sequestration in karst ecosystems:
1. Calculate the average values of carbonate karst carbon sink flux, silicate karst carbon sink flux, net ecosystem productivity, and total carbon sink flux data from 2000 to 2022, and calculate the temporal trend in IBM SPSS software.
2. Use Matlab2018b software to analyze the spatial variation trend of carbon sink data from 2000 to 2022. Firstly, calculate the slope of the trend line and combine it with Mann Kendall test to determine the significance of the variation trend.

Exploration of the driving force mechanism of carbon sequestration in karst ecosystems:
1. NDVI data comes from the MOD13A2 dataset on the USGS website（ https://www.usgs.gov/ ）. Subsequently, the NDVI data was processed using the maximum synthesis method.
2. Obtain SRTM DEM data provided by NASA https://dwtkns.com/srtm30m/ Generate slope data using Arcmap 10.8 software and DEM data.
3. The population density data in human activity data was obtained from WorldPop (https://hub.worldpop.org/).
4. The nighttime lighting data is sourced from the HARVARD VNet DMSP OLS like dataset (https://dataverse.harvard.edu/).
5. Process the data in IBM SPSS software and use the splits and rms packages in R language to achieve the fitting process of restricted cubic splines, fitting the threshold trend relationship between total carbon sink flux and driving force factors.

Application of threshold for driving force factor:
In Arcmap 10.8, filter the data based on the threshold using the grid calculator module in the ArcGIS toolbox.
