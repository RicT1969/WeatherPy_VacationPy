# WeatherPy_VacationPy
# WeatherPy-and-VacationPy
<p><b>Data Analysis Bootcamp Challenge 6: API<b></p>
<p>This project consists of two files:<ul><li>WeatherPy which looks at the weather conidtions in a number of cities from around the world and examines the relationship between the weather conditions and latitude.</li><li>VacationPy looks at which of these cities would be a pleasant place to stay given certain preferences for weather conditions and the availbility of hotels</li></ul></p>
<p><b>WeatherPy:</b></p><ul><li>imports the details of a large number of cities from around the world with their longitude and latitude using the CitiPy library and stores them in a DataFrame. The choice of city is random and will change each time the code is run.</li><li>An API call is then made to OpenWeatherMap to get deatils of prevailing wether conidtions: maximum temperature and average humidity, wind speed and cloudiness. These together with the details of the cities are stored in a DataFrame for analysis</li><li>To test if there is a relationship between latitude and the selected weather conditions a scatter plot is produced for each weather condition plotting all the cities by weather variable and latitude. the cities are then divided betwen those in the northern hempisphere and in the southern, in order to undergo regression analysis for each variable. This is necessary as latitude increases to a maximum of 90' north of the equator, and to a minimum of -90' south of the equator. meaning that the northern hemispere measurements will produce a negative correlation, whereas the southern will produce a positive correlation.</li><li>the conclusion is that there is a strong correlation with temperature, with temperatures falling the further away one travels from the equator; however, there is little evidence of the other weather conditions being influenced by latitude, most likely owing to the number of variables that can affect these conditions: land mass, terrain, distance form the sea, altitude and vegetation cover.</li></ul></p>
<p><b>VacationPy:</b></p><ul><li>Imports the list of cities and weather conditions from a csv file formed as part of the output from the WeatherPy routine. The cities are stored in a DataFrame and then plotted as points on a world map, sized according to the level of humidity of each city.</li><li>The DataFrame is then filtered to choose only those cities with climates that fall within a range of preferences: temperatures between 20'C and 28"C, wind speed of not more than 4.5 m/s and a cloudiness score of 0.</li><li>The results then form the basis of an API call to the GeoApify website to retieve the first hotel result that falls within a 10,000m radius of the coordinates of each City. The results are then plotted on a map with the details available by hovering the mosue over each City point.</li></ul></p>
<p><b>Sources</b></p><li>https://apidocs.geoapify.com/docs/places/#categories</li><li>https://openweathermap.org/api/statistics-api</li><li>https://stackoverflow.com/questions/75155189/formatting-hover-text-when-plotting-with-hvplot</li><li>https://stackoverflow.com/questions/41655706/pandas-scatter-plots-with-x-labels-and-aesthetically-pleasing-formats</li><li>https://stackoverflow.com/questions/59829077/how-to-display-r-squared-value-on-my-graph-in-python</li><li>https://discuss.streamlit.io/t/how-do-i-display-a-geoviews-map-or-is-there-any-way-to-customize-st-map-with-more-detailed-information-about-the-data/4274</li><li>https://stackoverflow.com/questions/67967721/select-values-in-pandas-groupby-series-less-than-and-subsequently-greate-than</li></ul></p>
