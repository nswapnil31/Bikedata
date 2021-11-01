# 2019 Bay Wheels Ride Data Exploration and Visualization
## by Swapnil


## Dataset

[Bay Wheels](https://en.wikipedia.org/wiki/Bay_Wheels) (previously known as Ford GoBike) is a regional public bike sharing system in the San Francisco Bay Area, California. Bay Wheels is the first regional and large-scale bicycle sharing system deployed in California and on the West Coast of the United States. As of January 2018, the Bay Wheels system had over 2,600 bicycles in 262 stations across San Francisco, East Bay and San Jose.[1] On June 28, 2017, the system officially re-launched as Ford GoBike in a partnership with Ford Motor Company.[4] After Motivate's acquisition by Lyft, the system was subsequently renamed to Bay Wheels in June 2019.[5] The system is expected to expand to 7,000 bicycles around 540 stations in San Francisco, Oakland, Berkeley, Emeryville, and San Jose.[6] The dataset used for this exploratory analysis consists of [monthly individual trip data](https://www.lyft.com/bikes/bay-wheels/system-data) from January 2019 to December 2019 in CSV format covering the greater San Francisco Bay area.

##### Data wrangling process:
- fix multiple fields that are not in the correct dtype, i.e. `start_time`, `end_time` should be datetime type, `user_type`should be categorical data type, etc
- add new columns for trip duration in minute, trip start date in yyyy-mm-dd format, trip start hour of the day, day of week and month
- cast 'start_dayofweek' to category dtype
- cast 'start_month' to category dtype for easy plotting
- filter out outlier trip records where the duration was very long


## Summary of Findings

The number of trips peaked around 8-9am and 18-19pm during a day, there were more trips on work days (Mon-Fri) compared to weekends. Summar time was the most popular season of a year, likely due to the weather. The riding trips tend to be shorter on Monday through Friday compared to weekends. It indicates a pretty stable and efficient usage of the bike sharing system on normal work days, while more casual flexible use on weekends.

There are a lot more subscriber usage than customers overall. The riding habit/pattern varies a lot between subscribers and customers. Subscribers use the bike sharing system for work commnute thus most trips were on work days (Mon-Fri) and especially during rush hours (when going to work in the morning and getting off work in the afternoon), whereas customers tend to ride for fun in the afternoon or early evenings over weekends. Subscriber usage peaks out on typical rush hours when people go to work in the morning and getting off work in the afternoon, which strengthened their usage purpose and goal of riding. Similar pattern was not observed among customers who tend to ride most in the afternoon or early evening for a different purpose than the subscribers.


## Key Insights for Presentation

Different usage pattern/habit between the two type of riders are seen from the exploration. Subscribers use the system heavily on work days i.e. Monday through Friday whereas customers ride a lot on weekends, especially in the afternoon. Many trips concentrated around 8-9am and 6-7pm on work days for subscribers, yet customers tend to use more in the late afternoon around 17pm Monday to Friday. The efficient/short period of usage for subscribers corresponds to their high concentration on rush hours Monday through Friday, indicating the use is primarily for work commute. The more relaxing and flexible pattern of customer use shows that they're taking advantage of the bike sharing system quite differently from the subscribers, heavily over weekends and in the afternoon, for city tour or leisure purpose probably.
