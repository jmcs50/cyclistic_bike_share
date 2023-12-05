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


#### 6. Top three recommendations \

Marketing strategies to convert casual riders into member riders should focus on:\

1. The summer months of June, July and August.
2. Station locations Streeter Dr & Grand Ave., DuSable Lake Shore Dr. & Monroe St., DuSable Lake Shore Dr. & North Blvd. and Wells St. & Concord Ln.
3. Saturday and Sunday and with 5pm used for live marketing events.

Promotion options should include first time subscriber promotions, weekend discount memberships, summer time specials and weekend in-person marketing events at the station locations.\
\

\
\

## Clean Data

Installed tidyverse and dplyr packages and running packages using **library()**:
install.packages("tidyverse")
install.packages("dplyr")
```{r library}
library(tidyverse)
library(dplyr)
```

Converted January through September 2023 into an individual data frame
using **read.csv()**:
```{r readcsv}
jan2023 <- read.csv("C://Users/mirro/Desktop/Bike-Share/202301-divvy-tripdata.csv")
feb2023 <- read.csv("C://Users/mirro/Desktop/Bike-Share/202302-divvy-tripdata.csv")
march2023 <- read.csv("C://Users/mirro/Desktop/Bike-Share/202303-divvy-tripdata.csv")
april2023 <- read.csv("C://Users/mirro/Desktop/Bike-Share/202304-divvy-tripdata.csv")
may2023 <- read.csv("C://Users/mirro/Desktop/Bike-Share/202305-divvy-tripdata.csv")
june2023 <- read.csv("C://Users/mirro/Desktop/Bike-Share/202306-divvy-tripdata.csv")
july2023 <- read.csv("C://Users/mirro/Desktop/Bike-Share/202307-divvy-tripdata.csv")
august2023 <- read.csv("C://Users/mirro/Desktop/Bike-Share/202308-divvy-tripdata.csv")
september2023 <- read.csv("C://Users/mirro/Desktop/Bike-Share/202309-divvy-tripdata.csv")
```

Use **colnames()** to verify all column names match for each month:
```{r colnames}
colnames(jan2023)
colnames(feb2023)
colnames(march2023)
colnames(april2023)
colnames(may2023)
colnames(june2023)
colnames(july2023)
colnames(august2023)
colnames(september2023)
```

Combined January through September 2023 data frame using **rbind()**:
```{r 2023year}
jan_sep_2023_trips <- rbind(jan2023,feb2023,march2023,april2023,may2023,june2023,july2023,august2023,september2023)
```

Confirmed data type of all columns using **str()**:
```{r datatype}
str(jan_sep_2023_trips)
```

Create column called month that provides name of month only using
**months()** and **as.date()**:
```{r month}
jan_sep_2023_trips$month <- months(as.Date(jan_sep_2023_trips$started_at))
```

Create column called weekday that provides day of the week only using
**weekdays()** and **as.date()**:
```{r weekday}
jan_sep_2023_trips$weekday <- weekdays(as.Date(jan_sep_2023_trips$started_at))
```

Create column called date that can be used to extract year from using
**as.date()**:
```{r date}
jan_sep_2023_trips$date <- as.Date(jan_sep_2023_trips$started_at) 
```

Create column called year that provides the year only using **format()**
and **as.date()**:
```{r year}
jan_sep_2023_trips$year <- format(as.Date(jan_sep_2023_trips$started_at), "%Y")
```

Create new column called duration that calculates difference between
start date/time and end date/time in minutes using **difftime()** and
**units 'mins'**:
```{r duration minutes}
jan_sep_2023_trips$duration_minutes <-difftime(jan_sep_2023_trips$ended_at, jan_sep_2023_trips$started_at, units='mins')
```

Create ride_length column with duration_minutes changed to a numeric number using **as.numberic()** and **as.character()**:
```{r numeric}
jan_sep_2023_trips$ride_length <- as.numeric(as.character(jan_sep_2023_trips$duration_minutes))
```

Remove negative duration from duration, duration_minutes and ride_length
columns using **abs()**:
```{r negative}
jan_sep_2023_trips$duration <- abs(jan_sep_2023_trips$duration)
jan_sep_2023_trips$duration_minutes <- abs(jan_sep_2023_trips$duration_minutes)
jan_sep_2023_trips$ride_length <- abs(jan_sep_2023_trips$ride_length)
```



## Analyzing Data

Count the number of each rideable_types for each month using
**group_by()** and **count()**:
```{r count}
jan_sep_2023_trips %>% group_by(month) %>% count(rideable_type)
```

Counted number of casual riders versus member riders for each month
using **group_by()** and **count()**:
```{r members}
jan_sep_2023_trips %>% group_by(month) %>% count(member_casual)
```

Counted most popular start station for casual riders using **filter()**
and **count()**:
```{r casual_start_station}
jan_sep_2023_trips %>% filter(member_casual == "casual") %>% count(start_station_name, sort = TRUE) %>% top_n(10)
```

Counted most popular start station for member riders using **filter()**
and **count()**:
```{r member_start_station}
jan_sep_2023_trips %>% filter(member_casual == "member") %>% count(start_station_name, sort = TRUE) %>% top_n(10)
```

Counted most popular end station for casual riders using **filter()**
and **count()**:
```{r casual_end_station}
jan_sep_2023_trips %>% filter(member_casual == "casual") %>% count(end_station_name, sort = TRUE) %>% top_n(10)
```

Counted most popular end station for member riders using **filter()**
and **count()**:
```{r member_end_station}
jan_sep_2023_trips %>% filter(member_casual == "member") %>% count(end_station_name, sort = TRUE) %>% top_n(10)
```

Calculated the ride length of casual riders versus member riders using **group_by()**, **filter()** and **count()**:
```{r ride_length}
jan_sep_2023_trips %>% group_by(month) %>% filter(member_casual == "casual") %>% count(duration_minutes)
jan_sep_2023_trips %>% group_by(month) %>% filter(member_casual == "member") %>% count(duration_minutes)
```

Top 10 starting locations grouped by month and rider type using
**group_by()**, **filter()** and **count()**:
```{r top30}
jan_sep_2023_trips %>% group_by(month) %>% filter(member_casual == "casual") %>% count(start_station_name, sort = TRUE) %>% top_n(10)
jan_sep_2023_trips %>% group_by(month) %>% filter(member_casual == "member") %>% count(start_station_name, sort = TRUE) %>% top_n(10)
```

Find the mean, median, max and min of ride length for member and casual
riders:
```{r mean}
jan_sep_2023_trips %>% filter(member_casual == "casual") %>% summarize(mean(ride_length))
jan_sep_2023_trips %>% filter(member_casual == "casual") %>% summarize(median(ride_length))
jan_sep_2023_trips %>% filter(member_casual == "casual") %>% summarize(max(ride_length))
jan_sep_2023_trips %>% filter(member_casual == "casual") %>% summarize(min(ride_length))
jan_sep_2023_trips %>% filter(member_casual == "member") %>% summarize(mean(ride_length))
jan_sep_2023_trips %>% filter(member_casual == "member") %>% summarize(median(ride_length))
jan_sep_2023_trips %>% filter(member_casual == "member") %>% summarize(max(ride_length))
jan_sep_2023_trips %>% filter(member_casual == "member") %>% summarize(min(ride_length))

```

Calculate the average ride time for each weekday using **group_by()**,
**filter()**, **summarize()** and **mean()**:
```{r average}
jan_sep_2023_trips %>% group_by(weekday) %>% filter(member_casual == "casual") %>% summarize(mean(ride_length))
jan_sep_2023_trips %>% group_by(weekday) %>% filter(member_casual == "member") %>% summarize(mean(ride_length))

```


