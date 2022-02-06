# Increasing profits by converting casual members to annual members

![Image: Getty Images/iStock](https://raw.githubusercontent.com/CharlesIvia/cyclistic/main/images/bike.jpg)

<!-- badges open -->
<!-- 
![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/v/release/navendu-pottekkat/awesome-readme?include_prereleases)
: This badge shows the version of the current release.

![GitHub last commit](https://img.shields.io/github/last-commit/navendu-pottekkat/awesome-readme)
: I think it is self-explanatory. This gives people an idea about how the project is being maintained.

![GitHub issues](https://img.shields.io/github/issues-raw/navendu-pottekkat/awesome-readme)
: This is a dynamic badge from [**Shields IO**](https://shields.io/) that tracks issues in your project and gets updated automatically. It gives the user an idea about the issues and they can just click the badge to view the issues.

![GitHub pull requests](https://img.shields.io/github/issues-pr/navendu-pottekkat/awesome-readme)
: This is also a dynamic badge that tracks pull requests. This notifies the maintainers of the project when a new pull request comes.

![GitHub All Releases](https://img.shields.io/github/downloads/navendu-pottekkat/awesome-readme/total): If you are not like me and your project gets a lot of downloads(*I envy you*) then you should have a badge that shows the number of downloads! This lets others know how **Awesome** your project is and is worth contributing to.

![GitHub](https://img.shields.io/github/license/navendu-pottekkat/awesome-readme)
: This shows what kind of open-source license your project uses. This is good idea as it lets people know how they can use your project for themselves.
-->
<!-- badges end -->

This repository serves as the "all-in-one" area for my Google Data Analytics Capstone project's code and report. The README file is a summary of the file that houses the full report along with the code. The project can also be found on my portfolio here: www.kevinwong-ds.github.io.

---

## Table of Contents (TOC)[](#table-of-contents)
- [[1] Project Description](#[1]project-description)
    - [[1.1] About the company](#[1.1]about-the-company)
    - [[1.2] Business task](#[1.2]business-task)
- [[2] Methods used](#[2]methods-used)
    - [[2.1] Data Preparation](#[2.1]data-preparation)
    - [[2.2] Data Processing](#[2.2]data-processing)
    - [[2.3] Data Analysis](#[2.3]data-analysis)
- [[3] Summary](#[3]summary)
- [[4] Running Instructions](#[4]running-instructions)
- [[5] Future updates to be made](#[5]updates-to-be-made)
- [Usage](#usage)
- [Development](#development)
- [Contribute](#contribute)
    - [Sponsor](#sponsor)
    - [Adding new features or fixing bugs](#adding-new-features-or-fixing-bugs)
- [License](#license)
- [Footer](#footer)

## [1] Project description 

### [1.1] About the company

Cyclistic is a bike-sharing service launched in 2016 with a fleet of 5,824 bicycles and a network of 692 stations across Chicago. The 3 types of bikes they offer are electric, classic, and "docked" bikes; docked bikes are bikes that have been locked to public bike rack or pole. "Casual riders" are those that use the single and full-day passes and those that have annual memberships are Cyclistic "members".

The pricing plans they offer are (in USD): 

    - single-ride passes: $3.30/trip (up to 30 minutes, $0.15/min after))
    - full-day passes: $15/day (unlimited 3 hour rides in a 24-hour period)
    - annual memberships: $9/month which is billed $108 upfront (Unlimited 45 minute rides, $0.15/min after)

### [1.2] Business task

The financial analysts at Cyclistic have determined that converting casual members to annual members will maximize the long-term success of the company by increasing revenue. The marketing analyst team has been tasked with finding out how annual and casual members use Cyclistic's bike share service differently to help the marketing strategy team devise a media campaign to convert more casual members to Cyclistic members. The recommendations provided from the analysis will be reviewed by the Cyclistic executives. 

## [2] Prepare, process, analyze, visualize data
- inferential stats (would need to add to actual project)
- descriptive stats

### [2.1] Data Preparation
[(Back to TOC)](#table-of-contents)

We will be using data collected by Divvy (Cyclistic is the made-up name for this project) and made available by Motivate International Inc. under the license located here (https://www.divvybikes.com/data-license-agreement). Using the R programming language, 12 CSV files were aggregated with the first file starting from November 2020 and the last file was October 2021, approximately 1-year of data. Each month is used only once to remove bias towards a certain month and possibly a certain season. Note - No personal information stored and each ride is given a unique ride ID. 

Data integrity is the accuracy, consistency, reliability, and security of the data.

Since the data was collected by Divvy with their own GPS trackers on each bike, the accuracy, consistency, reliability of the data would be quite reliable. However, with any piece of technology, there is bound to be some errors and inconsistencies:
- GPS tracker it not calibrated correctly and location data is now inaccurate
- Errors during the data transfer (i.e. connection interruptions)from the bike to the cloud servers causing loss of data or corrupted files
- Error during the connection between the bike and the users phone causing potential errors/corruption in the data

The data is stored in Divvy's own servers and the customer's information is not recorded in the files. Thus, there isn't much of a concern for the security of the data and any data breach of sensitive information. However, any other sensitive information collected from the user's account details in other servers will not be related to this analysis.  

Thus, the credibility and integrity of the data is valid.

### [2.2] Data Processing
[(Back to TOC)](#table-of-contents)

The data was cleaned by:

    - deleting incomplete rows as cells were missing data which could be due to data transfer error from the bike to Cyclistic's cloud servers
    - searching for duplicate rows, none were found
    - removing rows where the station was for testing or repair purposes
    - removing "docked bike" rows as those bikes were locked to poles or public bike racks, and aren't useful for our analysis
    
The data was manipulated by:

    - adding a column calculating the ride length ("ride_length"). Negative durations were removed. 
    - Adding columns for when the day of the week, the month, the year, as well as the time of the day the ride was
    - ordering the days and months by chronological order for visualization purposes 

**The full data cleaning process can be found in a separate file under [Cyclistic Report].(docs/cyclistic-report)**

### [2.3] Data Analysis
[(Back to TOC)](#table-of-contents)

The full code for the following statistical analysis and visualizations can be found in a separate file under [Cyclistic Report].(.docs/cyclistic-report)    .

As mentioned earlier, Cyclistic's financial analysts have concluded that annual members, labeled "members" in the dataset, are the key to the company's long-term success as they are more profitable.

From the following visualization, we can see that annual members take more trips than casual members. 

<a href="/Report visualizations/Num_trips_per_type.JPG"><img src="/Report visualizations/Num_trips_per_type.JPG" style="width:45%;height:45%"/></a>

---

The following visualization shows the **number of trips by member type** (Casual vs. Annual member) based on the **hour of the day**. 

The following observations were made:
- Annual members still make more trips than casual members
- Assuming common work hours are between 9am-5pm, we can see a large number of annual members using the service between 6am-10am. At 4pm, annual member's number of trips increase dramatically with the peak at 5pm and declining afterwards. It appears that these spikes in usage are from annual members commuting to work.  
- After 11am, casual member's number of trips steadily increase until 7pm. As casual member trips are up to 30-minutes, they could be for leisure or commuting from point A to B.
 
<a href="/Report visualizations/Num_trips_per_type_BY_HOUR.JPG"><img src="/Report visualizations/Num_trips_per_type_BY_HOUR.JPG" style="width:50%;height:50%"/></a>

---

The next plot shows the **number of trips by member type** (Casual vs. Annual member) based on the **day of the week**. 

Significant observations include:
- Monday to Thursday have the lowest number of trips per day for the casual members and Friday, Saturday, Sunday having a significant spike in usage. Considering the previous visualization, this could be due to casual members mainly using Cyclistic for leisure purposes. Finding the time on the weekend and after work on Friday to enjoy a nice bike ride.
- Annual members usage are quite consistent throughout the week with the highest usages during the weekdays. Since they have unlimited rides, they could use it for commuting to work, business breakfast/lunch/dinner meetings, or even grocery shopping. We could confirm this by analyzing where the rider's are starting and ending their rides. However, there are missing station names in the dataset which would not give us an accurate understanding of how the service is used based on location.
    
We can see from the table below the plot that for casual members on the weekend, the average duration of their trips are much higher than the weekdays. Supporting the observation that they may use the service for leisure purposes. 

<a href="/Report visualizations/Num_trips_per_type_BY_DAY.JPG"><img src="/Report visualizations/Num_trips_per_type_BY_DAY.JPG" style="width:50%;height:50%"/></a>

---

The bar-chart below shows the number of trips by member trip (Casual vs. Annual member) based on the month of the year, from November 2020 to October 2022. 

Significant observations include:
- The typical cold months of the winter season include November, December, Janurary, and Feburary. We can see from the plot that those months have the lowest usage for both types of members.
- Casual member usage peaks in July but noticeably declines until October. A deeper analysis would be needed to fully understand why this happened. However, we can make the following hypotheses can be made: going back to school; going on vacation; decreasing tempertures causing a decrease in usage.
- Annual members usage is consistent throughout the summer months. The nicer weather may want them to use bikes instead of public transportation or their personal vehicle.

<a href="/Report visualizations/Num_trips_per_type_BY_MONTH.JPG"><img src="/Report visualizations/Num_trips_per_type_BY_MONTH.JPG" style="width:50%;height:50%"/></a>

---

__**Summary Statistics**__


## [3] Summary

The visuals for supporting the findings have been generated in the code chunks of the Analyze step. The most important findings are summarized below:

Casual riders tend to take much longer rides than member riders.
Casual riders take more rides during weekends than during weekdays, while member riders take similar number of rides throughout the week.
Both casual and member riders take more rides during summer than during winter.
Casual riders take fewer but longer rides in the winter.
Nearly all docked bikes are used by casual riders for longer rides, whereas member riders don't use docked bikes.
Casual riders often use stations at or near popular tourist destinations.
Act
The business task of this project is to convert casual riders to member riders. My recommendations are based upon creating or increasing the incentives of the annual membership that might look attractive to casual riders.

Make the pricing plan for casual riders scale with the ride length (i.e., longer rides higher prices), while keeping the pricing plan for members constant with the ride length (i.e., same price for any ride length).
Make the pricing plan for casual riders dependent on day of week (i.e., higher prices on weekends), while keeping the prices for members constant with the day of week.
Develop and provide to members, free of charge, a smartphone app based on Google Maps, that provides, in addition to real-time bike traffic information and destination recommendations, many other functionality such as vital monitoring, health tracker, calories burned, gas money saved, bike buddies and professional trainers to chat with.
Increase the number of bikes at stations around popular tourist destinations, especially on weekends during the summer.
Increase the prices for docked bikes.
- document conclusions and recommendations
## [4] Running instructions
[(Back to TOC)](#table-of-contents)

-how to run/replicate

<!-- *You might have noticed the **Back to top** button(if not, please notice, it's right there!). This is a good idea because it makes your README **easy to navigate.*** 

The first one should be how to install(how to generally use your project or set-up for editing in their machine).

This should give the users a concrete idea with instructions on how they can use your project repo with all the steps.

Following this steps, **they should be able to run this in their device.**

A method I use is after completing the README, I go through the instructions from scratch and check if it is working. -->

<!-- Here is a sample instruction:

To use this project, first clone the repo on your device using the command below:

```git init```

```git clone https://github.com/navendu-pottekkat/nsfw-filter.git``` -->

## [5] Updates to be made
[(Back to TOC)](#table-of-contents)

The following are some things I would like to add to this project for a deeper analysis:

    - Sample size calculation to determine the exact number of annual memberships needed to convert for maximum success 
    - Inferential stats (in section 2): One sample test of difference/One sample hypothesis test, Confidence Interval, Contingency Tables and Chi Square Statistic, T-test or Anova, Pearson Correlation, Bi-variate Regression, Multi-variate Regression.
    - Predictive analysis: using machine learning models on historical data to optimize marketing campaign
    
# License
[(Back to TOC)](#table-of-contents)

<!-- Adding the license to README is a good practice so that people can easily refer to it.

Make sure you have added a LICENSE file in your project folder. **Shortcut:** Click add new file in your root of your repo in GitHub > Set file name to LICENSE > GitHub shows LICENSE templates > Choose the one that best suits your project!

I personally add the name of the license and provide a link to it like below. -->

[GNU General Public License version 3](https://opensource.org/licenses/GPL-3.0)

# Footer
[(Back to TOC)](#table-of-contents)

<!-- Let's also add a footer because I love footers and also you **can** use this to convey important info.

Let's make it an image because by now you have realised that multimedia in images == cool(*please notice the subtle programming joke). -->

Leave a star in GitHub if you liked this!

<!-- Add the footer here -->

<!-- ![Footer](https://github.com/navendu-pottekkat/awesome-readme/blob/master/fooooooter.png) -->
