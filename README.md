
### How to run

`streamlit run app.py`

-----
<h2 align='center'>dataset</h2>

### Other Dataset

**1. Temperature changes:** Data set [here](https://www.kaggle.com/sevgisarac/temperature-change?select=Environment_Temperature_change_E_All_Data_NOFLAG.csv) shows the changes in temperature in each country from 1961 to 2019. The data is also split up into each month, so that you can compare January vs January, and by season. The changes go anywhere from 9&deg;C cooler to 11&deg;C warmer.<br/><br/> 

**2. CO2 Emissions:** Temperature fluctuations can be caused by many different events, one of which is CO2 emissions. Each country produces different amounts of CO2 dependent on their access to electricity, the total population, the urban population and other factors. We used the data from https://ourworldindata.org/co2-and-other-greenhouse-gas-emissions and you can find the dataset [here](./static/data/CO2_emission.csv)

**3. Country demographics:** Since the CO2 emissions can be influenced by the demographics of the country, the dashboard includes current demographics, as of May 2021, so that as you are reviewing the charts, you can see how the demographics might play a role. The demographics were scraped from three different websites using Beautiful Soup. After scraping the websites, the data was pushed into the sqlite database as an additional table and also saved as a csv file.<br><br>

- a. __Flags__ - https://www.worldometers.info/geography/flags-of-the-world/<br>
- b. __Population__ - https://www.worldometers.info/world-population/population-by-country/<br>
- c. __Latitude and Longitude coordinates__ - https://developers.google.com/public-data/docs/canonical/countries_csv<br><br>

**4. GeoJson:** For the map, we used Leaflet and geoJson files for the boundaries of each country. You can find the full geoJson file here https://opendata.arcgis.com/datasets/2b93b06dc0dc4e809d3c8db5cb96ba69_0.geojson. 

**5. Kaggle:** https://www.kaggle.com/code/andrewmahandrew/temperature-map/notebook

### NASA Dataset

https://github.com/IvyQwinn/GlobalTemperatureAnalysis/tree/main

https://data.giss.nasa.gov/gistemp/tabledata_v4/GLB.Ts+dSST.csv 

> GLOBAL Land-Ocean Temperature Index in 0.01 degrees Celsius   base period: 1951-1980

https://data.giss.nasa.gov/gistemp/tabledata_v3/NH.Ts+dSST.csv

> The GISS Surface Temperature Analysis (GISTEMP) is an estimate of global surface temperature change

https://data.giss.nasa.gov/gistemp/tabledata_v3/SH.Ts+dSST.csv

> The GISS Surface Temperature Analysis (GISTEMP) is an estimate of global surface temperature change.
