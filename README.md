# MONTREAL-BIXI-2023-DATA-ANALYSIS
This project focuses on the Data Cleaning, Data Preprocessing, and Data Analysis processes. The original dataset is retrieved from [Bixi Montréal](https://bixi.com/en/open-data/), Trip History of 2023.

This repository includes:
* **README.md**
* **LICENSE**
* **MONTREAL-BIXI-2023-DATA-ANALYSIS.ipynb**
* png files

Guiding questions for the project:
* What are the most popular routes in 2023?
* During which time of the year, week, and day, most rides were recorded?
* What is the average ride duration throughout the year?

## Dataset Overview
* **STARTSTATIONNAME**: Text field, the names of start stations.
* **STARTSTATIONARRONDISSEMENT**: Text field, the arrondissements of the start stations.
* **STARTSTATIONLATITUDE**: Text field, the start stations' latitudes.
* **STARTSTATIONLONGITUDE**: Text field, the start stations' longitudes.
* **ENDSTATIONNAME**: Text field, the names of end stations.
* **ENDSTATIONARRONDISSEMENT**: Text field, the arrondissements of the end stations.
* **ENDSTATIONLATITUDE**: Text field, the end stations' latitudes.
* **ENDSTATIONLONGITUDE**: Text field, the end stations' longitudes.
* **STARTTIMES**: Integer field, the start time in milliseconds since epoch.
* **ENDTIMEMS**: Float field, the end time in milliseconds since epoch.
  
## The Project Summary
### 1. Data Cleaning
* Drop duplicates
* Drop null values
* Modify incorrect data
* Handle inconsistent text/categorical data

### 2. Data Preprocessing - Adding new columns to help with Data Analysis
* **STARTDATETIME**: Start Time of the ride, datetime type
* **ENDDATETIME**: End Time of the ride, datetime type
* **DURATION**: The difference between Start Time and End Time of a ride, in term of minutes
* Other time units of Start Time: **MONTH**, **DAY**, **DAYOFWEEK**, **HOUR**

### 3. Data Analysis
#### Summary
* The total number of rides recorded in 2023: 11790789 with null values.
* The total number of rides recorded in 2023: 11719684 without null values.
* The total number of minutes recorded in 2023: 197202233.75 minutes.
* The average duration of bixi rides in 2023: 16.83 minutes.

#### What are the most popular routes in 2023?
Top 10 popular routes are made up of 5 roundtrips and 5 other routes. The most popular route is the roundtrip in Métro Jean-Drapeau station.

![Métro Jean-Drapeau roundtrip was the most popular route.](https://github.com/mainguyen2911/MONTREAL-BIXI-2023-DATA-ANALYSIS/blob/main/popular-routes.png)

#### During which time of the year, week, and day, most rides were recorded?
Bixi season 2023 started on April 12, and we can see that people would ride Bixi more frequently throughout summer and fall (from May to October) when the weather is more comfortable to be active outdoors. The total number of rides will start to drop in November, and then Bixi would close most of their stations during winter, thus not many rides in December.

![Number of rides throughout each month](https://github.com/mainguyen2911/MONTREAL-BIXI-2023-DATA-ANALYSIS/blob/main/num-of-rides-month.png)

The bar plot representing the daily number of rides in 2023 displays a clearer view on the previous plot. An interesting pattern we are seeing is that from mid-July to the beginning of October, the daily count of rides fluctuates less than in other periods. It seems that when the weather is warm and nice, people would develop a more consistent habit of riding Bixi.

![Number of rides throughout each date in 2023](https://github.com/mainguyen2911/MONTREAL-BIXI-2023-DATA-ANALYSIS/blob/main/num-of-rides-date.png)

There is not much of a difference between each day of the week. The total number of rides would increase gradually throughout the week, from Monday to Friday, then slightly drop during the weekend. People would probably ride more on Friday.

![Number of rides throughout each day of the week](https://github.com/mainguyen2911/MONTREAL-BIXI-2023-DATA-ANALYSIS/blob/main/num-of-rides-week.png)

This is an interesting plot showing that people would start to ride Bixi more from the beginning of normal office hours (8 am/9 am to 5 pm). There is a small hike at 8 am (compared to the hour before and after it), and then the biggest hike at 5 pm. There is a chance that many people use Bixi as a means to travel to work.

![Number of rides throughout each hour of the day](https://github.com/mainguyen2911/MONTREAL-BIXI-2023-DATA-ANALYSIS/blob/main/num-of-rides-hour.png)

#### What is the average ride duration throughout the year?
There are a few special hikes in December. Dates in December have the highest average duration, however, the number of rides is low, only around 3,000 rides per day. Bixi season 2023 started on April 12, which is where we see a hike in the number of rides. And April 15, 2023, the first Saturday after the start of the Bixi season has recorded a high number of rides as well as the average duration.

![Average ride duration throughout the year](https://github.com/mainguyen2911/MONTREAL-BIXI-2023-DATA-ANALYSIS/blob/main/average-duration.png)
![Top 10 dates with the highest average ride duration](https://github.com/mainguyen2911/MONTREAL-BIXI-2023-DATA-ANALYSIS/blob/main/top-average-duration.png)
