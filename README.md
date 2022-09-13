# Google-Data-Analytics-Capstone-Repository
## The Scenario
I’ve been enrolled in the Google Data Analytics Professional Certificate since July and am currently finishing up the last course. For the last course, they recommend working on some case studies in which we can add to our portfolios. They gave us a couple of options to work on or we could also find and work on a case study of our own choosing. I chose to work with the first case study they provided, How Does a Bike-Share Navigate Speedy Success?.

For this case study, I am working as a junior data analyst in the marketing team for Cyclistic, a bike-sharing company located in Chicago. The goal of this case study is to help Cyclistic create a marketing campaign in order to maximize the number of annual memberships. We will do so by answering the following three questions: How do annual members and casual riders use Cyclistic bikes differently? Why would casual riders buy Cyclistic annual memberships? How can Cyclistic use digital media to influence casual riders to become members? In doing so, my task is to find trends and gain insights that will help the Cyclistic executive team decide on the recommended marketing program.

## Data Sources
The data used for analysis is from HERE. The data used in the previous 12 months of Cyclistic trip data from September 2020 - August 2021. The data is from a reliable source, Motivate International Inc under this license and is organized in 12 separate “.csv” files, one for each month. Each file contains 13 attributes per observation, containing rider IDs, which location they picked up the bike to when they got off, and so on. This data will be used to find trends between casual riders and annual members.

## Data Cleaning
For the cleaning process, my goal is to combine all the files into one, with a consistent format throughout the file, in terms of data structures and naming conventions and so forth. I will start the process by loading all the files into a SQL database, so I can organize, sort, filter, and clean the data. I chose to use BigQuery from the Google Cloud Platform since that is what I’ve been using throughout the course. At a quick glance of the data, I noticed that there are a bunch of nulls in various attributes that will need further inspection to see if they can be filled in as much as possible.
After loading all the files into BigQuery, I wrote a quick query to join all the files into one. At first, my query using UNION ALL did not run. So upon further inspection, it seems that Station IDs started changing formats around December 2020, where instead of just integers (ex. 639), some had letters in front (ex. TA1306000029). I decided to not include the Station IDs since we have just about the same information from the Station Names. I saved this query into another table called “all_data” to use for further data cleaning. QUERY
