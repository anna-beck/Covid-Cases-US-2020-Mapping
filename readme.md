# COVID-19 Cases and Case Rates in the United States (2020)
by Anya Beck

## Project Overview
This project presents two interactive web maps visualizing county-level COVID-19 data for the United States in 2020. The maps explore both the **intensity of COVID-19 spread relative to the population** (case rates) and the **total spread by numbers** (total case counts), using appropriate thematic mapping techniques for each data type.

The project was created using Mapbox GL JS to make both a choropleth and proportional symbol map with interactive, clickable elements.

---

## The Maps
- **Choropleth Map – COVID-19 Case Rates (per 1,000 residents)**  
  `map1.html`  
  https://[your_github_username].github.io/[your_repository_name]/map1.html

- **Proportional Symbol Map – Total COVID-19 Cases**  
  `map2.html`  
  https://[your_github_username].github.io/[your_repository_name]/map2.html

---

## Screenshots of Maps

/img/choro_map.png
/img/prop_map.png


---

## Map Design and Functionality

### Map 1: Choropleth Map (Case Rates)
- Displays COVID-19 **case rates per 1,000 residents** by county.
- A choropleth map is used to show how different counties compare to one another relative their population size. The variations are clear when presented in this format, and it becomes easier to understand how the spread of COVID interacted with different communities.
- Counties are symbolized using graduated color scale to show intensity (darker colors = higher case rate).
- Interactive popups shows county name and case rate when clicked.

### Map 2: Proportional Symbol Map (Total Cases)
- Displays **total COVID-19 case counts** by county using proportional circles.
- Circle size was scaled using interpolate for the radius.
- Scaling was adjusted to accommodate a highly skewed distribution, where majority counties fell between 500–50,000 cases, but some very large counties (LA county especially with over 700,000 cases) exceed 200,000 cases.
- Interactive popups display county name and total case count when clicked.

---

## Libraries and Tools Used
- **Mapbox GL JS v2.8.1** – interactive web mapping library
- **Mapshaper** – data preprocessing, attribute filtering, and geometry simplification
- **HTML / CSS / JavaScript** – structure, styling, and interactivity
- **GitHub Pages** – web hosting

---

## Data Processing and Projection
The data was processed using Mapshaper. The shapefiles were uploaded (as well as corresponding data) and then simplified, and exported into json files. The attribute fields were then filtered (-filter-fields) to include only relevant data (county and case counts or case rates). This was to ensure the map was simple to understand and conveyed only what it's setting out to do. 

The data was reprojected into Albers Equal Area so that it could represent accurate geometric areas for the counties.

---

## Data Sources
- **COVID-19 case data (2020):**  
  The New York Times COVID-19 Data  
- **Population data:**  
  American Community Survey (ACS) 2018 5-year estimates  
- **County boundaries:**  
  U.S. Census Bureau TIGER/Line Shapefiles  

---

## Credits and Acknowledgments

For functions and features that I didn't know very well, I referenced mapbox docs including:
https://docs.mapbox.com/style-spec/reference/layers/#paint-circle-radius
https://docs.mapbox.com/mapbox-gl-js/guides/styles/work-with-layers/
https://docs.mapbox.com/style-spec/reference/layers/#circle
https://docs.mapbox.com/style-spec/reference/expressions/#interpolate
https://docs.mapbox.com/mapbox-gl-js/api/events/#mapmouseevent

Data downloaded from Professor Zhao!

