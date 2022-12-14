# Hurricane-ETL-Project

The purpose of this project is to extract data from the internet and transform it in a pandas notebook in order to load it into another program where it can be analyzed. Our group chose to look into the historical data of tropical storms/hurricanes passing through Orlando. We found two sources of data on the web. The first is a list of storms showing the name, year, date range & categorization of each one. The second is a weather API that we used to gather weather data between the date range of each storm. The specific sources are listed at the bottom of this page.

We were able to find a version of the hurricane data that could easily be copied into Excel and formatted as a CSV (Data/storm_data) that could be read into pandas. After pulling that data into pandas and creating a dataframe (main.py), we had to convert the start and end dates to UNIX timestamps so they would matchup with the data needed to make API calls for each of our storms. Once we converted the dates, we used them to call the API and pulled the weather conditions between each date. We were limited by the data in the API because the weather data was only available from 1979 to the present. After pulling data about the storms from 1979 and onward, we converted the dataframe into a CSV (Data/Orlando Hurricane Data) and a sqlite file (Data/orlando_hurricane) so that it could be manipulated using SQL queries.

![Hurricane Tracks](Images/hurricane_tracks.png?raw=true "Title")

Hurricane data from NOAA: https://coast.noaa.gov/hurricanes/#map=6.65/28.487/-81.368&search=eyJzZWFyY2hTdHJpbmciOiJPcmxhbmRvLCBPcmFuZ2UgQ291bnR5LCBGbG9yaWRhLCBVU0EiLCJzZWFyY2hUeXBlIjoiZ2VvY29kZWQiLCJvc21JRCI6IjExMjgzNzkiLCJjYXRlZ29yaWVzIjpbIkg1IiwiSDQiLCJIMyIsIkgyIiwiSDEiLCJUUyIsIlREIiwiRVQiXSwieWVhcnMiOltdLCJtb250aHMiOltdLCJlbnNvIjpbXSwicHJlc3N1cmUiOnsicmFuZ2UiOlswLDExNTBdLCJpbmNsdWRlVW5rbm93blByZXNzdXJlIjp0cnVlfSwiYnVmZmVyIjo2MCwiYnVmZmVyVW5pdCI6WyJOYXV0aWNhbCBNaWxlcyJdLCJzb3J0U2VsZWN0aW9uIjp7InZhbHVlIjoieWVhcnNfbmV3ZXN0IiwibGFiZWwiOiJZZWFyIChOZXdlc3QpIn0sImFwcGx5VG9BT0kiOnRydWUsImlzU3Rvcm1MYWJlbHNWaXNpYmxlIjp0cnVlfQ==

Weather data from OpenWeatherAPI: https://openweathermap.org/history

Link to presentation: https://docs.google.com/presentation/d/1YVzW4m_vkuwkOfeiOYcrvAfOeQlAPdqb-RVLhVZObQk/edit?usp=sharing
