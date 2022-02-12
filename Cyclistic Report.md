<a href="/Report visualizations/Num_trips_per_type.JPG"><img src="/Report visualizations/Num_trips_per_type.JPG" style="width:40%;height:40%"/></a>

From the following bar plot, we can see that annual members take more trips than casual members showing the Cyclistic service to be useful for their needs. Although no personal information about the rider is not kept in the dataset, the following inference is made but can be confirmed by discussing the metrics with the financial analyst team. If a casual member were to make the average number of trips a day an annual member makes a day, their bill would most likely exceed the annual membership price. Thus, making the annual membership price worthwhile to purchase. The more loyal annual members Cyclistic can acquire and keep, the higher the probability of long-term success for the company by having those loyal members may refer others to join and creating a domino effect, exclusive promotions or events to keep those members to stay, etc..

---

<a href="/Report visualizations/Avg_num_trips_per_type_BY_HOUR(new).JPG"><img src="/Report visualizations/Avg_num_trips_per_type_BY_HOUR(new).JPG" style="width:50%;height:50%"/></a>

The plot above shows the **number of trips by member type** (Casual vs. Annual member) based on the **hour of the day**. 

The following observations were made:
- Annual members (in blue) 
  - They still make more trips than casual members. Evident by the taller bars in blue.
  - Let's assume common work hours are between 9am-5pm. <br>
    We can see a large number of annual members using the service between 6am-10am. <br>
    At 4pm, annual member's number of trips increase significantly with the peak at 5pm and declining afterwards. <br>
    It appears that these two spikes in usage are from annual members commuting to work.  
- Casual members (in red)
  - At 6am, casual member's number of trips steadily increasing until a peak at 6pm and then a sharp decrease until 11pm. As casual member trips are up to 30-minutes, they could be for leisure or commuting from point A to B.

---

<a href="/Report visualizations/Num_trips_per_type_BY_DAY.JPG"><img src="/Report visualizations/Num_trips_per_type_BY_DAY.JPG" style="width:40%;height:40%"/></a>

For this plot, it is the **number of trips by member type** (Casual vs. Annual member) based on the **day of the week**. 

Significant observations include:
- Monday to Thursday have the lowest number of trips per day for the casual members and Friday, Saturday, Sunday having a significant spike in usage. Considering the previous visualization (Number of trips by member trip based on the house of the day), this could be due to casual members mainly using Cyclistic for leisure purposes. Finding the time on the weekend and after work on Friday to enjoy a nice bike ride.
- Annual members usage are quite consistent throughout the week with the highest usages during the weekends. Since they have unlimited rides, they could use it for commuting to work, business breakfast/lunch/dinner meetings, or even grocery shopping. I hypothesize that on the weekends the riders would have more time to run errands and thus use the bike-share service more. We could confirm this by analyzing where the rider's are starting and ending their rides. However, there are missing station names in the dataset which would not give us an accurate understanding of how the service is used based on location.
    
We can see from the table below the plot that for casual members on the weekend, the average duration of their trips are much higher than the weekdays. Supporting the observation that they may use the service for leisure purposes. 

---

<a href="/Report visualizations/Num_trips_per_type_BY_MONTH.JPG"><img src="/Report visualizations/Num_trips_per_type_BY_MONTH.JPG" style="width:50%;height:50%"/></a>

This bar-chart shows the **number of trips by member type** (Casual vs. Annual member) based on **the month of the year, from November 2020 to October 2022.** 

Significant observations include:
- The typical cold months of the winter season include November, December, Janurary, and Feburary. We can see from the plot that those months have the lowest usage for both types of members.
- Casual member usage peaks in July but noticeably declines until October. A deeper analysis would be needed to fully understand why this happened. However, we can make the following hypotheses: <br>
  - Decline due to going back to school; going on vacation; decreasing tempertures causing a decrease in usage.
- Annual members usage is consistent throughout the summer months. The nicer weather may want them to use bikes instead of public transportation or their personal vehicle.

---
[(Back to TOC)](#table-of-contents)

__**Summary Statistics**__

From the table below, the average ride duration (in minutes) for casual and annual member's is 17.45 and 12.19, respectively. We can confirm and compare this to the plot underneath it which shows the average ride duration per member type by day.

<a href="/Report visualizations/SUMSTAT_avg_length_by_MEMBER.JPG"><img src="/Report visualizations/SUMSTAT_avg_length_by_MEMBER.JPG" style="width:20%;height:20%"/></a>

<a href="/Report visualizations/Avg_ride_length_per_type_by_DAY.JPG"><img src="/Report visualizations/Avg_ride_length_per_type_by_DAY(new).JPG" style="width:45%;height:45%"/></a>

<a href="/Report visualizations/SUMSTAT_avg_length_by_DAY.JPG"><img src="/Report visualizations/SUMSTAT_avg_length_by_DAY(new).JPG" style="width:20%;height:20%"/></a>

---

In the data cleaning process, we removed rows with the "docked_bike" variable as those bikes are normal bikes locked to public poles or racks and not at Cyclistic stations. So, the following table only has statistics for the classic and electric bike. We can subset the data to check the average ride duration based on the type of member and type of bike.

As Cyclistic's electric fleet is fairly new, there is not as much data available compare to the classic fleet. We can see that the average ride duration is slightly lower for electric bikes for both groups of members. This could be because the electric bikes are pedal-assisted and much faster than the regular bikes. So, the user can get to their destination faster which would shorten the ride length. 

<a href="/Report visualizations/SUMSTAT_avg_length_by_BIKE.JPG"><img src="/Report visualizations/SUMSTAT_avg_length_by_BIKE.JPG" style="width:35%;height:35%"/></a>
