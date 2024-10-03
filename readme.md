<h2 align='center'>Data</h2>

|         Format      |        Description       |
| ------------------------------ | ------------- |
| <img src="./static/Image/csv.png" alt="TP" align='left'  width="150" height="100">         |  **1. Temperature changes:** Data set found [here](https://www.kaggle.com/sevgisarac/temperature-change?select=Environment_Temperature_change_E_All_Data_NOFLAG.csv) shows the changes in temperature in each country from 1961 to 2019. The data is also split up into each month, so that you can compare January vs January, and by season. The changes go anywhere from 9&deg;C cooler to 11&deg;C warmer.<br/><br/> **2. CO2 Emissions:** Temperature fluctuations can be caused by many different events, one of which is CO2 emissions. Each country produces different amounts of CO2 dependent on their access to electricity, the total population, the urban population and other factors. We used the data from https://ourworldindata.org/co2-and-other-greenhouse-gas-emissions and you can find the dataset [here](./static/data/CO2_emission.csv). |
|         <img src="./static/Image/webScrape1.png" alt="TP" align='left'  width="150" height="100">                        |   **3. Country demographics:** Since the CO2 emissions can be influenced by the demographics of the country, the dashboard includes current demographics, as of May 2021, so that as you are reviewing the charts, you can see how the demographics might play a role. The demographics were scraped from three different websites using Beautiful Soup. After scraping the websites, the data was pushed into the sqlite database as an additional table and also saved as a csv file.<br><br>- a. __Flags__ - https://www.worldometers.info/geography/flags-of-the-world/<br>- b. __Population__ - https://www.worldometers.info/world-population/population-by-country/<br>-  c. __Latitude and Longitude coordinates__ - https://developers.google.com/public-data/docs/canonical/countries_csv<br><br>-  *You can find the scrape code [here](./country_scrape.py).*  |
|         <img src="./static/Image/Geojson.jpg" alt="TP" align='left'  width="150" height="100">                        |   **4. GeoJson:** For the map, we used Leaflet and geoJson files for the boundaries of each country. You can find the full geoJson file here https://opendata.arcgis.com/datasets/2b93b06dc0dc4e809d3c8db5cb96ba69_0.geojson.  |

<h2 align='center'>ETL</h2>

<img src="./static/Image/sqlite.png" alt="TP" align='left'  width="120" height="100"> <br/>
- Data is queried, cleaned, transformed and loaded to *SQLiteDB* using `python pandas`, `SQLAlchemy` . <br/><br/>

<img src="./static/Image/postgresql-logo.png" alt="TP" align='left'  width="110" height="95"> <br/>
- *PostresSQLDB* is used to deploy the app to Heroku. <br/>
- Find Heroku requirements and repository [here](https://github.com/divya-gh/Interactive-Climate-Change-Dashboard.git).
----
<h2 align='center'>Web Framework</h2>
<img src="./static/Image/flask_api.jpg" alt="TP" align='left'  width="110" height="100"> <br/>
- python Flask REST API is implemented to manage HTTP requests, render templates and JSON serialized data for manipulating the charts. <br/>

https://www.kaggle.com/code/andrewmahandrew/temperature-map/notebook

https://data.giss.nasa.gov/gistemp/tabledata_v4/GLB.Ts+dSST.csv 

> GLOBAL Land-Ocean Temperature Index in 0.01 degrees Celsius   base period: 1951-1980

https://data.giss.nasa.gov/gistemp/tabledata_v3/NH.Ts+dSST.csv

> The GISS Surface Temperature Analysis (GISTEMP) is an estimate of global surface temperature change

https://data.giss.nasa.gov/gistemp/tabledata_v3/SH.Ts+dSST.csv

> The GISS Surface Temperature Analysis (GISTEMP) is an estimate of global surface temperature change.

https://data.giss.nasa.gov/gistemp/tabledata_v4/GLB.Ts+dSST.csv 

> GLOBAL Land-Ocean Temperature Index in 0.01 degrees Celsius   base period: 1951-1980

https://data.giss.nasa.gov/gistemp/tabledata_v3/NH.Ts+dSST.csv

> The GISS Surface Temperature Analysis (GISTEMP) is an estimate of global surface temperature change

https://data.giss.nasa.gov/gistemp/tabledata_v3/SH.Ts+dSST.csv

> The GISS Surface Temperature Analysis (GISTEMP) is an estimate of global surface temperature change.


