## TEAM

https://www.spaceappschallenge.org/nasa-space-apps-2024/find-a-team/404-not-found1/?tab=details

## Competition question

https://www.spaceappschallenge.org/nasa-space-apps-2024/challenges/

https://www.spaceappschallenge.org/nasa-space-apps-2024/challenges/tell-us-a-climate-story/?tab=details

---


## Project division of labor

Kay: Responsible for capturing data sets and processing data sets + processing chart data

Jimmy Liao: LLM deployment must be addressed in the near future (this part will require rewriting the story function due to changes in our page structure), and the deployment website will be online

Noflag: Integrate the entire architecture (add all current functions) + handle LLM function integration

Muhammad Shaharyar Sarwar: Responsible for program efficiency

Yuijuhn Ting: Responsible for page design and integrating all functions into the map screen display

----

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
