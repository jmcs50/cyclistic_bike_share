# cyclistic_bike_share

## How do annual members and casual riders use Cyclistic bikes differently?

\

#### 1. Business task \
How do members and casual riders use Cyclistic bikes differently.\
\
● **What is the problem you are trying to solve?** \
How are casual and member riders using Cyclistic services and how can this information be used to provide visual media opportunities to influence causal riders to become members.\
Analyze how casual riders are using Cyclistic services to provide visual media opportunities that will influence these riders to become members.
\
● **How can your insights drive business decisions?** \
Insights can narrow down the best locations, time of year, day of the week and time of day to utilize marketing opportunities to casual riders.\

\

#### 2. Description of all data sources used \
The data being used has been made available by Motivate International Inc. under data license agreement: <https://divvybikes.com/data-license-agreement>. The time frame being analyzed is January 1, 2023 through September 30, 2023.\
\
**● Where is the data located?** \
Data is located on local Desktop that was obtained as .csv zip files from https://divvy-tripdata.s3.amazonaws.com/index.html
\
\
**● How is the data organized?** \
Data for each month is organized into individual months into 13 columns: ride_id, rideable_type, started_at, ended_at, start_station_name, start_station_id, end_station_name, end_station_id, start_lat, start_lng, end_lat, end_lng and member_casual.\
\
**● Are there issues with bias or credibility in this data?** \
The original data source can be confirmed, but it is missing some values which
may be key to answering the question being asked by business. The data
is current and update to date.\
**Reliability :** Data is incomplete and missing from start station name and end station name. Started at and ended at data's are also inaccurate as for some values the end date or time is before the start date or time.\
**Originality :** Data is being directly collected from Motivate International Inc. under data license agreement: <https://divvybikes.com/data-license-agreement>.\
**Comprehensive :** Dataset contains multiple fields for rideable type, started at date/time, ended at date/time, start station names, end station names and member types.\
**Current :** Data is being updated monthly and date range being analyzed is from January 2023 through end of September 2023.\
**Cited :** Original source is from reliable organization that is directly collecting data.\

\
\
**● How are you addressing licensing, privacy, security, and accessibility?** \
The data has been made available by Motivate International Inc. under data license agreement:
<https://divvybikes.com/data-license-agreement> \
\
**● How did you verify the data's integrity?** \
By reviewing each month from January 2023 through September 2023\
\
**● How does it help you answer your question?** \
The data provide dates, times, stations and member type which are essential to narrowing down how casual riders are using the Cyclistic service.\
\
**● Are there any problems with the data?** \
Values are missing from columns such as start_station_name, start_station_id, end_station_name and end_station_id. The started_at and ended_at also contains values where the start date value is after the end date value, which results in a negative trip duration.\

\

#### 3. Documentation of any cleaning or manipulation of data \
**● What tools are you choosing and why?** \
I am using R to clean and analyze the data and using Tableau to visualize the data. I picked R as it provided me with the opportunity to use R Markdown and document the steps I took with cleaning and analyzing data. I picked Tableau to visual the data as I was interested in creating a dashboard.\
\
**● Have you ensured your data’s integrity?** \
Yes, I have removed data that did not make sense such as starting times beginning after ending times.\
\
**● What steps have you taken to ensure that your data is clean?** \
I have reviewed the data type it is saved as and removed data that was incomplete, missing or incorrect such as dates not matching up or negative ride trips lengths.\
\
**● How can you verify that your data is clean and ready to analyze?** \
By running the max and min of numeric columns.\
\
**● Have you documented your cleaning process so you can review and share those results?** \
The cleaning and analysis process has been documented in R Markdown.\

\

#### 4. Summary of analysis
**● How should you organize your data to perform analysis on it?** \
Data is combined and organized into columns.\
\
**● Has your data been properly formatted?** \
Data has been properly formatted with column data types corrected to match field values.\
\
**● What surprises did you discover in the data?** \
The type of data was missing or incorrect. For example the start date of trips beginning after the end dates. I did not expect to see negative values.\
\
**● What trends or relationships did you find in the data?** \
I found that both casual and member riders favor the summer months, 5 pm as their main activity time and Electric bicycles.\
\
**● How will these insights help answer your business questions?** \
These insights will narrow down the locations and time that marketing opportunities should focus on in order to maximize ROI.\
\

Both casual riders and member riders prefer to use the Electric bicycle with 5 PM being the most popular time that both rider types use Cyclistic services. Both rider types also enjoy summer time with casual riders and member riders taking the majority of their trips in June, July and August.

Casual riders prefer to use Cyclistic during the weekend with Saturday being the favorite day with 357,669 riders, followed by Sunday with 276,450 riders. Streeter Dr & Grand Ave. and DuSable Lake Shore Dr. & Monroe St. are were the majority of casual riders begin their travels from with 40,966 and 26,464 trips beginning here. DuSable Lake Shore Dr. & North Blvd. is where overwhelmingly casual rider choose to end their trips with 21,637 trips ending at this locations, followed by Wells St. & Concord Ln with 10,214 trips ending there.

Member riders like to use Cyclistic during the work week with Thursday being the favorite day with 459,777 riders, but closely followed by Wednesday with 454,737 riders. Member riders favor Wells St. & Concord Ln., Streeter Dr. & Grand Ave. and DuSable Lake Shore Dr. & North Blvd. at their starting locations with 16,987, 14,956 and 13,862 trips starting at these three locations. When it is time to end their trips member riders almost evenly distribute their ending locations between Clinton St. & Washington Blvd with 20,450 trips, Kingsbury St. & Kinzie St. with 20,224 trips and Clark St. & Elm St. with 19,489 trips.\

\

#### 5. Supporting visualizations and key findings
**● Were you able to answer the question of how annual members and casual riders use Cyclistic bikes differently?** \
I was able to verify using the data provided that their are differences with how the two rider types use Cyclistic services.\
\
**● What story does your data tell?** \
My data story tells what are the frequent stations, dates and times that casual riders are utilizing Cyclistic's services as the highest rate in order to direction for marketing opportunities.\
\
**● How do your findings relate to your original question?** \
I was able to determine what common uses casual and members have with the Cyclistic ride share and where they differ.\
\
**● Who is your audience? What is the best way to communicate with them?** \
The main audience is the marketing team and executive team.\
\
**● Can data visualization help you share your findings?** \
Data Visualization is able to paint a picture that clearly identifies trends, commonaliities and differences between member and casual riders.\
\
**● Is your presentation accessible to your audience?** \
Presentation is in a Tableau dashboard format, HTML and also powerpoint.\
\
\
Both casual riders and member riders prefer to use the Electric bicycle with 5 PM being the most popular time that both rider types use Cyclistic services. Both rider types also enjoy summer time with casual riders and member riders taking the majority of their trips in June, July and August.\
