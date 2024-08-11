# Project Theme: Commercial Flight Delays

# Datasets used: 
https://www.kaggle.com/datasets/oleksiimartusiuk/bts-january-2024-commercial-flights-data?select=T_ONTIME_MARKETING.csv
https://www.geoapify.com/ [API]

# Project Description
The dataset above catalogs data concerning commercial flights in the US in the month of January 2024, obtained from the Bureau of Transportation Statistics. This data includes origin and destination cities, along with distances between them; times for departure, taxi, wheels-off and on, and arrival, with associated delays, the causes of delays, and whether each flight was canceled or diverted. Our goal with this data would be to look at the following for five cities with international airports: 

Comparison of reason for delay
Visual: Bar chart
Delay Types: All 5 (NAS & Other)

Time of delay (length)
Binned to different intervals (0-15 min., 15-30 min., 30-1 hr., 1+ hrs.)
Departures from target city & Arrivals to target city
Visual: Stacked Bar chart

Cancellations vs. delays vs. diverted vs. early/on time
Visual: Pie chart
*Note that canceled and diverted may be too small to have separate; combine into one if necessary

Geoapify full dataset for location data
Visual: Geoapify heat map

Compiled report of city vs. city for data questions

# Notable Sources
https://stackoverflow.com/questions/24251219/pandas-read-csv-low-memory-and-dtype-options (read_csv error clearing)
https://www.geeksforgeeks.org/replace-nan-values-with-zeros-in-pandas-dataframe/ (NaN data filling)
https://aspm.faa.gov/aspmhelp/index/Types_of_Delay.html [explanation for presentation]

# Contributions
This project was a collaborative effort of the following individuals: Andrew Pohle, Bryan Thomas, Caitlin McMahill, Jessica Maranto, and Lauren Graves. 
The code files contained in the folder labeled "Code_Files" were written as a collaboration amongst this group. The code may be altered or have slight differences based on the individual's data set. Caitlin M. created the code for our GeoApify heat map and visual. All other visualizations were the result of each individual's code and data. Andrew P. wrote our analysis and conclusion based on collaborative findings with his peers. Please reference our dataset resources and presentation resources for the source of additional information we obtained and used during the presentation. 

# Files
The coding files can be found in the folder labeled "Code_Files". Each is labeled with the city that the code explores for flight data.
The visualizations are in a folder labeled "Visualizations". 
The slide presentation used is in the folder labeled "Presentation". 
The data set csv file is labeled "Resources.zip". 

# Project1 Data Analysis

For this analysis, we narrowed down our main questions with airport delays into 3 main questions, which would then dictate what data would be analyzed from the database we obtained. First, how many delays or canceled flights occur in a typical month, which would analyze the reliability of flights in and out of each analyzed airport. Secondly, how frequently do certain categories of issues occur, which could identify shortcomings within certain airports’ operations. And finally, how long are flights usually delayed for, to give patrons and airports estimations on the impact that these delays can have.

# Data Observations
- Atlanta seems to be a clear leader among the various international airports surveyed. 64.4% of the recorded flights to and from Atlanta were marked as having no delays, and despite having nearly as many recorded flights as Chicago *(52703 flights to Chicago’s 57769)*, the counted delay types and lengths are among the lower half of the cities studied. Atlanta also barely beats out Chicago for the lowest percentage of canceled/diverted flights by 0.1%, and only has .4% more arrival delays than Denver. The only notable problem that the charts show is a rate of weather delays that’s much lower than Chicago, but still has more than 300 instances over Denver’s 610 recorded delays.
- Denver, having the second-highest rate of non-delayed flights among the study group, also has a few notable insights revealed by the data. The flight status charts show that Denver has the highest percentage of canceled and diverted flights among the airports surveyed. In addition, the flight status chart shows a notable weight difference between departure and arrival delays, correlated by the delay lengths chart showing more departure delays for each category bin than arrival delays. Lastly, the delay types chart reveals a notable increase in security-based delays over other cities polled.
- Chicago, fittingly for the Windy City, has a major problem with weather-based delays. The recorded instances of weather-based delays for Chicago is 2276, more than double the second-highest city in Atlanta, and also has NAS delays marked as their highest recurring delay reason - as non-extreme weather conditions are one of the problems under that category, it seems appropriate. These high weather conditions seem to impact the flight delay times most of all, as the most busy airport of our study grouping *(57769 flights recorded)* is also the city with the highest combined count of moderate-to-severe delays compared to the cities polled *(30-60 min., 1-2 hrs., and 2+ hours)*.
- Dallas, Texas has some of the odder data sets of the 5 cities studied, with distributions and percentages that are noticeably different at a passing glance, such as for the delay lengths chart. This may be due to the total size of the Texas-based data block compared to the other international airports studied *(12704 flights recorded, compared to LA in 4th place with 30674)*, whose larger datasets could be the contributing factor in their comparatively more even distributions.
- Los Angeles has the worst flight record of the 5 cities studied, with only 27.8% of flights having no delays at all. More than 2/3rds of the recorded data has some instance of recorded delays, but the majority of these delays are minor affairs, as reflected in the delay lengths chart for LA; of the cities charted, LA has the largest data concentration of minor delays, with the most in the first category *(0-15 min.)*, and in a close race with Denver and Chicago for the second category *(15-30 min.)*.
- On a more general note, the size of the unknown data columns in the delay types charts dwarfs the other listed reasons by at least 1.5 times, at minimum. This implies that the recordkeeping for delay reasons is not comprehensive enough to cover every cause for delay.
- The large majority of delay lengths appear to be minor, less than 15 minutes at max, and trends to having less instances the longer delays become.

# Conclusions
The large majority of flight delays only last for a few minutes, so perhaps the majority of airports see delay elimination as not valuable enough for the investment it would take. However, for cities with a statistically high percentage of delayed flights, such as Los Angeles, money should be spent to improve the efficacy of their airline operations on all aspects. Meanwhile, other airlines have more specific issues to address, such as Denver’s departure-based delays and security updates.
