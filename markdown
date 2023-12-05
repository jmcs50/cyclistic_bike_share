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


