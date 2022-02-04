# Bikesharing
 Analysis of Citi Bike data for New York City on Tableau.

 ## Overview of Bikesharing Data
 Impressed after using the Citi Bike for visiting various landmarks in New York City. We want to start a similar Bike share business in Des Moines. So, analysis of the Citi Bike data on tableau is a great choice as the purpose of this analysis is to find out what are the factors which make the Citi Bike in NYC a great experience , finding out the best times , top stations , demography, type  of the users etc. to draw a proposal for Bike share in Des Moines for a presentation to an angel investor.

 ## Resources
 * Data: 201908-citibike-tripdata.csv
 * Software: Tableau 2021.4, Jupyter Notebook

## Bikeshare Analysis Results:

### Converting tripduration from int64 to datetime:
* Using Python and Pandas functions, we create a jupyter notebook [NYC_Citibike_Challenge]() we convert the "tripduration" column from an integer to a datetime datatype to get the time in hours, minutes, and seconds (00:00:00) and create a new column called sec_tripduration, then export the DataFrame as a CSV file as[new201908_citibike_tripdata](). Later the sec_tripduration is renamed in tripduration in HMS inside tableau.

Your final results should look similar to the following image:
[sec_trioduration]()


The data in the "tripduration" column is converted to a datetime datatype and has the correct time format.
The DataFrame is exported as a new file without the index column.

Next, we use tableau to connect csv file and start making visualizations. The visualizations can be viewed at [Bike sharing](https://public.tableau.com/app/profile/sucharita.bhattcharjee/viz/Bikesharing_16440041248210/BikeshareStory?publish=yes)
### Average trip duration by age:
* Area charts in Tableau are essentially line charts that are filled in below the line. we will make one by dragging the Birth Year dimension into the Columns section, and the Tripduration measure into the Rows section. 

* We will get the average duration of a bike ride, by age. This will help us set expectations for trip duration in Des Moines.

* We can infer that young people tend to ride for more time on the basis of this data.

![avg_trip_duration_by_age](?raw=true)

### Peak Hours August
* Bar charts help us to compare the hours, we'll put  at the "Starttime" dimension, as this is a good indicator of when customers tend to begin their bike rides in  "Rows" section. We will put the generated field, count of tripdata in columns.
* August can be a good month to visit New York City,so the peak hours for bike trips during the month of August will help our investors get a ballpark estimate of how many bikes we might need in Des Moines.
* We can infer that peak hours can be 8AM to 10AM and 5PM to 7PM. So, this might be people going or coming back from work.

![peak_hours_august](?raw=true)

### Checkout Times for Users
* There is a line graph displaying the number of bikes checked out by duration for all users, and the graph can be filtered by the hour. It clould be filtered by the hour.
* This will help us know the average trip duration for the most number of trips that were done. 
* We can infer that most of the bikes were checked out for a duration of 20 mins or less. There is some demand till 40 mins and hardly much after an hour.

![checkout_times_for_users](?raw=true)

### Checkout Times by Gender
* There is a line graph displaying the number of bikes that are checked out by duration for each gender by the hour, and the graph can be filtered by the hour and gender.
* This will help us know who made the most number of trips by the hour males, females or unknown.
*  We can infer that most of the bikes were checked out predominantly by males then females and least by unknown. 

![checkout_times_by_gender](?raw=true)

### Trips by Weekday for each Hour
* A heatmap is created showing the number of bike trips for each hour of each day of the week.
* This will help us to know which days in the week and hours of the week are the busiest and bike utilization is highest.
* We can infer that most of the bikes were checked out on thursday, followed by Tuesday and Monday. 

![trips_by_weekday_for_each_hour](?raw=true)

### Trips by Gender (Weekday per Hour)
* A heatmap is created showing the number of bike trips by gender for each hour of each day of the week, and the heatmap can be filtered by gender.
* This will help us know which gender needs the most bikes on days of week as well as hours in a day.
* We can infer that the demand for bikes is highest on Thursdays, followed by Tuesday and Monday by the males and is generally not very high for females or unknown on any of the days.
 
![trips_by_gender](?raw=true)
### User Trips by Gender (Weekday per Hour)
* A heatmap is created showing the number of bike trips for each type of user and gender for each day of the week, and you can only filter by user and gender.
* This will help us know how does the demand for bike vary between subscribers and customers.
* We can infer that the demand is higher by subscribers in case of males and females but less for the unknown.

![usertrips_by_gender](?raw=true)

## Summary of Bikeshare Analysis:
The Bikeshare Analysis can be summarized as follows:
1. Young people tend to ride for more time on the basis of this data. We need to focus on the youth as one of the primary customers.
2. Peak hours can be 8AM to 10AM and 5PM to 7PM. We need the maximum number of bikes during these hours which coincide with timing when people go to/ get back from work.
3. Most of the bikes will be checked out for less than an hour. So, apart from peak hours only a minimum number of bikes need to be there which can be rotated and  will cause less wear and tear.
4. Most of the bikes are checked out by males. So, we need to focus on men as one of the primary customers.
5. Most of the bikes are used on Thursdays, followed by Tuesday and Monday. This needs to be further explored as maybe there are some events that happen on those days or maybe happy hours at nearby food/beverage joints which amp up the demand.
6. Most of the males use the bikes heavily on Thursdays, followed by Tuesday and Monday. So, some activity/ discount etc. might be happening nearby which interest males more. ALso, in many companies employees can work from home but turn up to office on one/two days which may be Tuesdays and Thursdays.
7. Males are most loyal subscribers and tend to use the services the most.

### Two additional Visualizations
* For two additonal visualizations, it makes sense to check out which station ids are most popular on the basis on age and population so that when we set up bike stations we can focus on the primary customers.

* We will  map the Start Station Latitude and Start Station Longitude. These measures will provide the geographic location of the bike rental starting points. We will size the stations based on bikeid and thus figure out the Top Stations

1. Top stations based on Age.
* We put an additional Map layer with data layer as Age to find out the age of people in zipcodes near the Top starting stations.
* We can infer that Top starting stations are areas with zipcode belonging to people less than 40.

![top_start_station_age](?raw=true)

2. Top stations based on Population.
* We put an additional Map layer with data layer as Age to find out the population density of zipcodes near the Top starting stations.
* We can infer that Top starting stations are areas with zipcode having more than 18000 people.

![top_start_station_population](?raw=true)

