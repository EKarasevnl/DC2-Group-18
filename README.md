# DC2-Group-18

## Datasets

'barnet.csv': Burglary data from police.uk.

'barnet.geojson': LSOA boundaries for the borough of Barnet.

'granular_pois.csv': Contains information about points of interest(POI), including their latitude, longitude, and category.

'sunlight_updated.csv': Average daily sunlight hours aggregated per month.

'Copy of hou01tables2021.xlsx': Household data for the UK.

## POI analysis.ipynb

### Functionality

Data Loading: The code reads the POI data ('granular_pois.csv'), crime data ('barnet.csv'), and LSOA boundaries ('barnet.geojson').

South Barnet LSOA Selection: A list of LSOA codes for South Barnet is created, including specific codes and those matching certain LSOA name patterns.

POI per LSOA: Points of interest are spatially joined with LSOA boundaries to determine which POIs fall within each LSOA.

Crime Count per LSOA: Crime counts are calculated per LSOA and year based on the crime data.

Visualization: The code generates an interactive map using folium. It includes a choropleth map to represent crime counts in different LSOAs in South Barnet. Additionally, selected POIs (such as gyms, parks, 

groceries, and cafes) are marked on the map as circle markers.

### Usage

Ensure that the required data files (granular_pois.csv, barnet.csv, and barnet.geojson) are present in the same directory as this code file.

Install the necessary dependencies (pandas, geopandas, and folium).

Run the code to perform the data analysis and generate the map.

## random_forest.ipynb

### Functionality

Data Loading: The code reads crime data ('barnet.csv'), LSOA boundaries ('barnet.geojson'), housing data ('hou01tables2021.xlsx'), sunlight data ('sunlight_updated.csv').

Calculates correlations between the crime count and other variables (e.g., percentage of 1-bedroom houses, sunlight hours).

Builds an XGBoost regression model to predict the crime count and provides model evaluation.

Visualization: The code generates an interactive map using folium. It includes a choropleth map to represent crime counts/predictions in different LSOAs in Barnet.

### Usage

Ensure that the required data files (barnet.csv, barnet.geojson, hou01tables2021.xlsx, sunlight_updated.csv).

Install the necessary dependencies (pandas, geopandas, matplotlib, folium, geojson, xgboost, shapely, scikit-learn, numpy).

Run the code to train the model, perform evaluation and generate the map.
