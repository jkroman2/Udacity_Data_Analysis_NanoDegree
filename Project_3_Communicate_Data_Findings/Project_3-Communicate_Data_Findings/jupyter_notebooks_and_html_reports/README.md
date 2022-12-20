# San Francisco - Bay Area Bike Share
## by Jason Kannemeyer


## Dataset

> Bay Area Bike Share began in August 2013 and features a fleet of 700 bicycles and 70 stations along the San Francisco peninsula. Specially designed, durable bikes are locked into a network of docking stations and can be rented from and returned to any station in the system. The bike share system operates year-round, 24 hours a day, with stations in San Francisco, Redwood City, Palo Alto, Mountain View, and San Jose.

> Bike sharing allows Bay Area residents and visitors an additional, cost-effective transportation option. It offers many public health benefits, such as reducing the amount of harmful vehicle emissions released into the air. The program’s network is efficiently linked to public transit and numerous docking stations, providing many possible route combinations.

> Since January 1, 2016, the Metropolitan Transportation Commission has been in charge of overseeing the Bay Area Bike Share Program.

> My Analysis will focus on data from 2020 - 2022, 202205 dataset it gives errors and even with error checking The data is still in a non readable format - All data from 201801-202003 is excluded since the dataset columns are not the same format and number of columns

> **Column name meanings:**
* start_lat	= Start Latitude
* start_lng	= Start Longitude
* end_lat	= End Latitude
* end_lng   = End Longitude

> **Columns to be renamed:**

* rideable_type = Bike Types
* member_casual = Membership Types

> **Bike Share Data Source:**
* https://s3.amazonaws.com/baywheels-data/index.html
- The data from the datasource includes data from 2018, my analysis only takes data from 202004-202210 since all the columns and data are in the same format, except for 202205 which is excluded from the analysis because it introduces errors when merging the dataset with all the other datasets


## Summary of Findings

> Following an investigation of the dataset for ytears 2020-2022, the following conclusions were reached. Most rides were recorded in October, from futher research it shows that events and tourist tend to go to SF during october for the Fall season red/orange environments. the from the top 10 start and end destinations the top 4 seem to be the the same destinations - it might also be possible that those are related because when I did a comparison and found that from the whole dataset 541962 start and end stations had the same values, but from looking at the rows I found that there might have been some outliers, because some of the rows start time were more then the end time which gave a negative value in the duration column. The average trips taken weekly mostly occured on a Saturday or Friday, but breaking it down I found that most of the the trips happened during the morning and afternoon rush, meaninig either when commuters went to work, or when they returned from work. There was some points of interest - trips that happened in 3:00 am you could say they were outliers or that these were occasions when events ended. From the ammount of different bikes I found that the bikes with the lowest numbers actually accounted for the highest trip durations, the docked bikes only made up 10.087% of the total bikes but had the higest average trip durations. From the members and casual users I found that there were more members then casual users, but that casual users clocked more hours then the members. 


## Key Insights for Presentation

1. Rides seems to be higher during the normal morning traffic rush hours, and flattens during the day but picks up again later at night when people return from work.
2. Casual drivers seems to last longer then that of members, even though the number of members are more than that of casual drivers
3. I also found that the number of bikes does not necesarily mean the durations will be longer, because what I saw from the comparison between the types of bikes - even though Docked bikes only accounts for 10.087% of the total bikes, their trip durations are higher then that of the bikes with higher numbers
4. From the data that I used you can see that people tend to use the service more on Saturday and Friday, and October seems to be the time when more trips are recorded then any other month - could be because of tourists traveling more to the bay area in October.