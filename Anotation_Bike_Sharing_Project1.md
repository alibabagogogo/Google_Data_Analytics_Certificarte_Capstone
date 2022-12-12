---
layout: "page"
title: "Google Data Analytics Certificarte Capstone"
description: "A Bike Share Program"
date: "2022-12-12"
img: assets/img/Bike_share.png
author: "Ali Kaya"
importance: 1
category: Data Analysis
output:
  md_document:
    preserve_yaml: true
---

## Scenario

You are a junior data analyst working in the marketing analyst team at
Cyclistic, a bike-share company in Chicago. The director of marketing
believes the company’s future success depends on maximizing the number
of annual memberships. Therefore, your team wants to understand how
casual riders and annual members use Cyclistic bikes differently. From
these insights, your team will design a new marketing strategy to
convert casual riders into annual members. But first, Cyclistic
executives must approve your recommendations, so they must be backed up
with compelling data insights and professional data visualizations.

## Characters and teams

-   Cyclistic: A bike-share program that features more than 5,800
    bicycles and 600 docking stations. Cyclistic sets itself apart by
    also offering reclining bikes, hand tricycles, and cargo bikes,
    making bike-share more inclusive to people with disabilities and
    riders who can’t use a standard two-wheeled bike. The majority of
    riders opt for traditional bikes; about 8% of riders use the
    assistive options. Cyclistic users are more likely to ride for
    leisure, but about 30% use them to commute to work each day.
-   Lily Moreno: The director of marketing and your manager. Moreno is
    responsible for the development of campaigns and initiatives to
    promote the bike-share program. These may include email, social
    media, and other channels.
-   Cyclistic marketing analytics team: A team of data analysts who are
    responsible for collecting, analyzing, and reporting data that helps
    guide Cyclistic marketing strategy. You joined this team six months
    ago and have been busy learning about Cyclistic’s mission and
    business goals — as well as how you, as a junior data analyst, can
    help Cyclistic achieve them.
-   Cyclistic executive team: The notoriously detail-oriented executive
    team will decide whether to approve the recommended marketing
    program.

## About the Company

In 2016, Cyclistic launched a successful bike-share offering. Since
then, the program has grown to a fleet of 5,824 bicycles that are
geotracked and locked into a network of 692 stations across Chicago. The
bikes can be unlocked from one station and returned to any other station
in the system anytime.

Until now, Cyclistic’s marketing strategy relied on building general
awareness and appealing to broad consumer segments. One approach that
helped make these things possible was the flexibility of its pricing
plans: single-ride passes, full-day passes, and annual memberships.
Customers who purchase single-ride or full-day passes are referred to as
casual riders. Customers who purchase annual memberships are Cyclistic
members.

Cyclistic’s finance analysts have concluded that annual members are much
more profitable than casual riders. Although the pricing flexibility
helps Cyclistic attract more customers, Moreno believes that maximizing
the number of annual members will be key to future growth. Rather than
creating a marketing campaign that targets all-new customers, Moreno
believes there is a very good chance to convert casual riders into
members. She notes that casual riders are already aware of the Cyclistic
program and have chosen Cyclistic for their mobility needs.

Moreno has set a clear goal: Design marketing strategies aimed at
converting casual riders into annual members. In order to do that,
however, ***the marketing analyst team needs to better understand how
annual members and casual riders differ***, why casual riders would buy
a membership, and how digital media could affect their marketing
tactics. Moreno and her team are interested in analyzing the Cyclistic
historical bike trip data to identify trends.

## Roadmap for successful data analysis deliveries:

<table>
<thead>
<tr class="header">
<th style="text-align: center;">Roadmap</th>
<th style="text-align: center;">Deliverable</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: center;">Ask</td>
<td style="text-align: center;">A clear statement of the business
task</td>
</tr>
<tr class="even">
<td style="text-align: center;">Prepare</td>
<td style="text-align: center;">A description of all data sources
used</td>
</tr>
<tr class="odd">
<td style="text-align: center;">Process</td>
<td style="text-align: center;">Documentations of any cleaning or
manipulation of data</td>
</tr>
<tr class="even">
<td style="text-align: center;">Share</td>
<td style="text-align: center;">Supporting visualizations and key
findings</td>
</tr>
<tr class="odd">
<td style="text-align: center;">Ask</td>
<td style="text-align: center;">A clear statement of the business
task</td>
</tr>
<tr class="even">
<td style="text-align: center;">Act</td>
<td style="text-align: center;">Your top three recommendations based on
your analysis</td>
</tr>
</tbody>
</table>

### Ask: A clear statement of the business task

Based on the given context about this data-driven decision making
project, we have to carefully think about business task before we
proceed to any further steps. There is a hypothesis raised by the
director of marketing, who believes “the company’s future success
depends on maximizing the number of annual memberships”. Meanwhile, “the
finance analysts have concluded that annual members are much more
profitable than casual riders”.

Accordingluy, there are mainly two ways to expand the number of annual
memberships, one is launching marketing campaigns that targets all-new
customers, the other one is converting existing casual riders into
annual members. After leveraging the pros and cons, costs and
expectations, etc., the later one ‘should’ have a higher conversion rate
with lower cost, as casual riders are already aware of the the program
and have chosen it for their mobility needs.

Thus, in order to effectively convert the existing casual riders to
annual members, it can be broken down into three main aspects:

1.  Finding out differences: How do annual members and casual riders use
    Cyclistic bikes differently?
2.  Knowing the reasoning for being an annual member: Why would casual
    riders buy Cyclistic annual memberships?
3.  Setting up effective marketing approaches: How can Cyclistic use
    digital media to influence casual riders to become members?

We will see that this project is related to the `Question 1` due to
dataset limitation mentioned in following “Prepare” step.

Before we go deeper on the dataset itself, general speaking, we should
firstly think about in what ways we can differentiate between the two
groups of users in the context of participating bike share programs.
Here are some rough ideas/gut feelings:

1.  Do casual riders use bicycles for a shorter period of time than the
    annual members on average?
2.  Do casual riders use bicycles less frequently than annual members
    within a period of time on average?
3.  Do casual riders use bicycles for a shorter distance than annual
    members on average?
4.  Do annual members usually use bicycles for commuting(Peaking period
    from 7:00-9:00 A.M. and 17-19 P.M. per day)? More in summer than
    winter?
5.  … …

> Ok, you might come up with more ideas. let’s leave them here and move
> on to the remaining phases to explore what we can do with the given
> dataset (Please keep in mind, in reality, theoretically we could do
> infinite analysis if we have ‘sufficient’ dataset. Even if we do not
> have ‘enough’ data metrics and dimensions till now, we can somehow try
> to collect them in the near future to continusly consolidate, update
> or even completely overturn the analytic results. All in all, data
> analysis is a process that requires long-term continuous revision)

### Prepare: A description of all data sources used

You can find data
[here](https://divvy-tripdata.s3.amazonaws.com/index.html) (Note: The
datasets have a different name because Cyclistic is a fictional company.
For the purposes of this case study, the datasets are appropriate and
will enable you to answer the business questions. The data has been made
available by Motivate International Inc. under this
[license](https://www.divvybikes.com/data-license-agreement).) This is
public data that you can use to explore how different customer types are
using Cyclistic bikes. But note that data-privacy issues prohibit you
from using riders’ personally identifiable information. This means that
you won’t be able to connect pass purchases to credit card numbers to
determine if casual riders live in the Cyclistic service area or if they
have purchased multiple single passes.

In prepare phase, we gonna focus on the dataset itself to
adjust/refine/compromise/finalize our analytic goals(Or the ideas we
mentioned in the ask phase). We should clarify the following aspects of
the given data.

-   Are there issues with bias or credibility in this data? Does your
    data ROCCC?
    -   Reliable: accurate, complete and unbiased information that’s
        been vetted and proven fit for use – Lyft Bikes and Scooters,
        LLC (“Bikeshare”) operates the City of Chicago’s (“City”) Divvy
        bicycle sharing service. Bikeshare and the City are committed to
        supporting bicycling as an alternative transportation option. As
        part of that commitment, the City permits Bikeshare to make
        certain Divvy system data owned by the City (“Data”) available
        to the public.
    -   Original: it is original and not collected through a second or
        third party source
    -   Comprehensive: The best data sources contain all critical
        information needed to answer the question or find the solution –
        We will answer this question in the following quesion
        `Finally, how does it help you answer your question?`.
    -   Current: Data is collected on a monthly basis. As of today, the
        latest dataset was collected in November 2022. In this analysis,
        we will be using data from December 2021 to November 2022.
    -   Cited: Who created the data set? Is it part of a credible
        organization? When was the data last refreshed? – the City of
        Chicago permits Bikeshare to make certain Divvy system data
        owned by the City (“Data”) available to the public. It is
        refreshed on a monthly basis.
-   How are you addressing licensing, privacy, security, and
    accessibility?
    -   You can find the Data License Agreement
        [here](https://ride.divvybikes.com/data-license-agreement)
-   How is the original data organized(structured)?

<table>
<thead>
<tr class="header">
<th style="text-align: center;">Attribute</th>
<th style="text-align: center;">Type</th>
<th style="text-align: center;">Sample</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: center;">ride_id</td>
<td style="text-align: center;">String</td>
<td style="text-align: center;">46F8167220E4431F</td>
</tr>
<tr class="even">
<td style="text-align: center;">rideable_type</td>
<td style="text-align: center;">String</td>
<td style="text-align: center;">electric_bike</td>
</tr>
<tr class="odd">
<td style="text-align: center;">started_at</td>
<td style="text-align: center;">String</td>
<td style="text-align: center;">2021-12-07 15:06:07</td>
</tr>
<tr class="even">
<td style="text-align: center;">ended_at</td>
<td style="text-align: center;">String</td>
<td style="text-align: center;">2021-12-07 15:13:42</td>
</tr>
<tr class="odd">
<td style="text-align: center;">start_station_name</td>
<td style="text-align: center;">String</td>
<td style="text-align: center;">Laflin St &amp; Cullerton St</td>
</tr>
<tr class="even">
<td style="text-align: center;">start_station_id</td>
<td style="text-align: center;">String</td>
<td style="text-align: center;">13307</td>
</tr>
<tr class="odd">
<td style="text-align: center;">end_station_name</td>
<td style="text-align: center;">String</td>
<td style="text-align: center;">Morgan St &amp; Polk St</td>
</tr>
<tr class="even">
<td style="text-align: center;">end_station_id</td>
<td style="text-align: center;">String</td>
<td style="text-align: center;">TA1307000130</td>
</tr>
<tr class="odd">
<td style="text-align: center;">start_lat</td>
<td style="text-align: center;">Number</td>
<td style="text-align: center;">41.85483</td>
</tr>
<tr class="even">
<td style="text-align: center;">start_lng</td>
<td style="text-align: center;">Number</td>
<td style="text-align: center;">-87.66366</td>
</tr>
<tr class="odd">
<td style="text-align: center;">end_lat</td>
<td style="text-align: center;">Number</td>
<td style="text-align: center;">41.87197</td>
</tr>
<tr class="even">
<td style="text-align: center;">end_lng</td>
<td style="text-align: center;">Number</td>
<td style="text-align: center;">87.65097</td>
</tr>
<tr class="odd">
<td style="text-align: center;">member_casual</td>
<td style="text-align: center;">String</td>
<td style="text-align: center;">member/casual</td>
</tr>
</tbody>
</table>

-   Finally, how does it help you answer your question?
    -   the dataset contain 13 attributes, most indispensable attribute
        is the one named as ‘member\_casual’, which can be used as a
        label to distinguish two groups of users
    -   start and end time are recorded so that we can calculate the
        ride length (i.e., duration = ended\_at - started\_at)
    -   start time can also be used to analyze the distribution per hour
        of using shared bikes.(Peaks and Troughs)
    -   rideable\_type can be used to analyze user preference between
        annual members and casual users
    -   <s>latitude and longitude can be used to calculate the distance
        per ride, and to draw corresponding routing on the map, which
        can be used to differentiate routing patterns between member and
        casual users</s>
    -   Time series data can also be used to analyze usage patterns in
        terms of day and night shifts, weekdays and weekends, season
        etc.

> The above-mentioned aspects will be the concrete analytic goals for
> this project. The detailed analysis processes and results will be
> given in the following sections.

### Process: Documentations of any cleaning or manipulation of data

#### Data was encapsulated in Zip format on a monthly basis. Thus, the data cleaning process will be applied to each month of data separately.

![](./image/dataonline.png)

In order to ensure data’s integrity, we should consider the following
aspects:

-   Follow consistent file-naming conventions (if needed)
    -   Since the data was well named by the provider, we don’t need to
        rename them.
-   Remove invalid data (if any, e.g. NA, empty etc.)

<!-- -->

    # import necessary libraries
    library(tidyverse)

    ## ── Attaching packages ─────────────────────────────────────── tidyverse 1.3.2 ──
    ## ✔ ggplot2 3.4.0      ✔ purrr   0.3.5
    ## ✔ tibble  3.1.8      ✔ dplyr   1.0.10
    ## ✔ tidyr   1.2.1      ✔ stringr 1.5.0
    ## ✔ readr   2.1.3      ✔ forcats 0.5.2
    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()

    library(skimr)
    library(hydroTSM)

    ## Loading required package: zoo
    ##
    ## Attaching package: 'zoo'
    ##
    ## The following objects are masked from 'package:base':
    ##
    ##     as.Date, as.Date.numeric
    ##
    ## Loading required package: xts
    ##
    ## Attaching package: 'xts'
    ##
    ## The following objects are masked from 'package:dplyr':
    ##
    ##     first, last
    ##
    ##
    ## Attaching package: 'hydroTSM'
    ##
    ## The following object is masked from 'package:tidyr':
    ##
    ##     extract

    library(geosphere)
    library(dplyr)
    library(psych)

    ##
    ## Attaching package: 'psych'
    ##
    ## The following objects are masked from 'package:ggplot2':
    ##
    ##     %+%, alpha

    library(lubridate)

    ## Loading required package: timechange
    ##
    ## Attaching package: 'lubridate'
    ##
    ## The following objects are masked from 'package:base':
    ##
    ##     date, intersect, setdiff, union

    # Read the data from CSV to Data Frame
    tripdata_202211 <- read.csv("./Case_Study_Bike_Sharing_Data/202211_tripdata.csv")
    # skim_without_charts() is an alternative to summary(), quickly providing a broad overview of a data frame
    tripdata_202211 %>% skim_without_charts()

<table>
<caption>Data summary</caption>
<tbody>
<tr class="odd">
<td style="text-align: left;">Name</td>
<td style="text-align: left;">Piped data</td>
</tr>
<tr class="even">
<td style="text-align: left;">Number of rows</td>
<td style="text-align: left;">337735</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Number of columns</td>
<td style="text-align: left;">13</td>
</tr>
<tr class="even">
<td style="text-align: left;">_______________________</td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;">Column type frequency:</td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;">character</td>
<td style="text-align: left;">9</td>
</tr>
<tr class="odd">
<td style="text-align: left;">numeric</td>
<td style="text-align: left;">4</td>
</tr>
<tr class="even">
<td style="text-align: left;">________________________</td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;">Group variables</td>
<td style="text-align: left;">None</td>
</tr>
</tbody>
</table>

Data summary

**Variable type: character**

<table style="width:100%;">
<colgroup>
<col style="width: 24%" />
<col style="width: 12%" />
<col style="width: 18%" />
<col style="width: 5%" />
<col style="width: 5%" />
<col style="width: 7%" />
<col style="width: 11%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">skim_variable</th>
<th style="text-align: right;">n_missing</th>
<th style="text-align: right;">complete_rate</th>
<th style="text-align: right;">min</th>
<th style="text-align: right;">max</th>
<th style="text-align: right;">empty</th>
<th style="text-align: right;">n_unique</th>
<th style="text-align: right;">whitespace</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">ride_id</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">16</td>
<td style="text-align: right;">16</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">337735</td>
<td style="text-align: right;">0</td>
</tr>
<tr class="even">
<td style="text-align: left;">rideable_type</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">11</td>
<td style="text-align: right;">13</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">3</td>
<td style="text-align: right;">0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">started_at</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">19</td>
<td style="text-align: right;">19</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">300238</td>
<td style="text-align: right;">0</td>
</tr>
<tr class="even">
<td style="text-align: left;">ended_at</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">19</td>
<td style="text-align: right;">19</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">300541</td>
<td style="text-align: right;">0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">start_station_name</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">49</td>
<td style="text-align: right;">51957</td>
<td style="text-align: right;">1063</td>
<td style="text-align: right;">0</td>
</tr>
<tr class="even">
<td style="text-align: left;">start_station_id</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">35</td>
<td style="text-align: right;">51957</td>
<td style="text-align: right;">1038</td>
<td style="text-align: right;">0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">end_station_name</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">49</td>
<td style="text-align: right;">54259</td>
<td style="text-align: right;">1069</td>
<td style="text-align: right;">0</td>
</tr>
<tr class="even">
<td style="text-align: left;">end_station_id</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">35</td>
<td style="text-align: right;">54259</td>
<td style="text-align: right;">1041</td>
<td style="text-align: right;">0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">member_casual</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">6</td>
<td style="text-align: right;">6</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">2</td>
<td style="text-align: right;">0</td>
</tr>
</tbody>
</table>

**Variable type: numeric**

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 11%" />
<col style="width: 16%" />
<col style="width: 8%" />
<col style="width: 5%" />
<col style="width: 8%" />
<col style="width: 8%" />
<col style="width: 8%" />
<col style="width: 8%" />
<col style="width: 8%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">skim_variable</th>
<th style="text-align: right;">n_missing</th>
<th style="text-align: right;">complete_rate</th>
<th style="text-align: right;">mean</th>
<th style="text-align: right;">sd</th>
<th style="text-align: right;">p0</th>
<th style="text-align: right;">p25</th>
<th style="text-align: right;">p50</th>
<th style="text-align: right;">p75</th>
<th style="text-align: right;">p100</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">start_lat</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">41.90</td>
<td style="text-align: right;">0.05</td>
<td style="text-align: right;">41.65</td>
<td style="text-align: right;">41.88</td>
<td style="text-align: right;">41.90</td>
<td style="text-align: right;">41.93</td>
<td style="text-align: right;">42.07</td>
</tr>
<tr class="even">
<td style="text-align: left;">start_lng</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">-87.65</td>
<td style="text-align: right;">0.03</td>
<td style="text-align: right;">-87.84</td>
<td style="text-align: right;">-87.66</td>
<td style="text-align: right;">-87.64</td>
<td style="text-align: right;">-87.63</td>
<td style="text-align: right;">-87.52</td>
</tr>
<tr class="odd">
<td style="text-align: left;">end_lat</td>
<td style="text-align: right;">230</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">41.90</td>
<td style="text-align: right;">0.21</td>
<td style="text-align: right;">0.00</td>
<td style="text-align: right;">41.88</td>
<td style="text-align: right;">41.90</td>
<td style="text-align: right;">41.93</td>
<td style="text-align: right;">42.08</td>
</tr>
<tr class="even">
<td style="text-align: left;">end_lng</td>
<td style="text-align: right;">230</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">-87.65</td>
<td style="text-align: right;">0.43</td>
<td style="text-align: right;">-87.84</td>
<td style="text-align: right;">-87.66</td>
<td style="text-align: right;">-87.65</td>
<td style="text-align: right;">-87.63</td>
<td style="text-align: right;">0.00</td>
</tr>
</tbody>
</table>

    # Based on the output of skim_without_charts(), we should clean dataset based on the following criteria
    # 1. search and delete empty rows with 'empty' tag on variables: start_station_name, start_station_id, end_station_name and end_station_id, respectively
    # 2. search and delete NA rows with 'n_missing' tag on variables: end_lat and eng_lng, respectively
    tripdata_202211 <- tripdata_202211 %>% filter(start_station_name != '', start_station_id !='', end_station_name != '', end_station_id !='') %>% filter(!is.na(end_lat), !is.na(end_lng))

-   Remove inapplicable data (if any, e.g., started\_at &gt;= ended\_at,
    this might be adjustable if we change their positions to each other.
    We don’t know whether this is caused by inapplicable transmission or
    other malfunctions, so we just simply remove them from dataset to
    achieve data integrity; Meanwhile, we suppose the
    ride\_length(ended\_at-started\_at) should be larger than 60s.
    Otherwise, this is not an ‘effective riding’)

<!-- -->

    # 1. search for and remove ineffective ride(ride_length < 60s)
    cleaned_202211 <- tripdata_202211 %>% filter(difftime(ended_at, started_at, units="secs") >= 60)

-   Create new variables to help on further analysis

<!-- -->

    # 1. create a new variable which is named as ride_length(the duration per ride calculated based on started_at and ended_at), and filter out ride_length == 0
    temp_202211 <- cleaned_202211 %>%  mutate(ride_length = difftime(ended_at, started_at, units="secs")) %>% transform(ride_length = as.numeric(ride_length)) %>% filter(ride_length != 0)

    # 2. create a new variable which names as day_of_week(the day of the week per ride based on started_at and ended_at)
    temp_202211 <- temp_202211 %>% mutate(day_of_week = '') %>% transform(day_of_week = weekdays(as.Date(started_at)))

    # 3. create a new variable which names as season, indicating the season when using the bikes
    temp_202211 <- temp_202211 %>% mutate(season = time2season(as.Date(started_at), out.fmt = "seasons"))

    # 4. create a new variable which names as distance, indicating the distance per ride. Note using Interface Between R and Google Maps will need the API Key. In order to reduce the API cost, we choose another distance calculation package to calculate the Haversine distance instead.

    prepared_202211 <- temp_202211 %>% mutate(distance = distHaversine(select(temp_202211, start_lng, start_lat), select(temp_202211, end_lng, end_lat)))
    rm(temp_202211)

-   Save cleaned data for further analysis

<!-- -->

    write.csv(prepared_202211, file = paste('./Cleaned_Data/', deparse(substitute(prepared_202211)) ,'.csv', sep="") , fileEncoding = 'UTF-8', row.names = FALSE)

> Please keep in mind we have in total 12 months data needed to be
> cleaned and prepared. We do them separately and combine them together
> into one csv for analysis.

### Analyze: Supporting visualizations and key findings

#### Let’s load and have a look at the cleaned and prepared data (Suppose we did combine cleaned 12 months data into one prepared\_all.csv. We could see after appropriate data cleaning and preparation, we totally have 4334101 records.)

    prepared_all <- read.csv("./Cleaned_Data/prepared_all.csv")
    skim_without_charts(prepared_all)

<table>
<caption>Data summary</caption>
<tbody>
<tr class="odd">
<td style="text-align: left;">Name</td>
<td style="text-align: left;">prepared_all</td>
</tr>
<tr class="even">
<td style="text-align: left;">Number of rows</td>
<td style="text-align: left;">4334101</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Number of columns</td>
<td style="text-align: left;">17</td>
</tr>
<tr class="even">
<td style="text-align: left;">_______________________</td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;">Column type frequency:</td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;">character</td>
<td style="text-align: left;">11</td>
</tr>
<tr class="odd">
<td style="text-align: left;">numeric</td>
<td style="text-align: left;">6</td>
</tr>
<tr class="even">
<td style="text-align: left;">________________________</td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;">Group variables</td>
<td style="text-align: left;">None</td>
</tr>
</tbody>
</table>

Data summary

**Variable type: character**

<table style="width:100%;">
<colgroup>
<col style="width: 24%" />
<col style="width: 12%" />
<col style="width: 18%" />
<col style="width: 5%" />
<col style="width: 5%" />
<col style="width: 7%" />
<col style="width: 11%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">skim_variable</th>
<th style="text-align: right;">n_missing</th>
<th style="text-align: right;">complete_rate</th>
<th style="text-align: right;">min</th>
<th style="text-align: right;">max</th>
<th style="text-align: right;">empty</th>
<th style="text-align: right;">n_unique</th>
<th style="text-align: right;">whitespace</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">ride_id</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">16</td>
<td style="text-align: right;">16</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">4334101</td>
<td style="text-align: right;">0</td>
</tr>
<tr class="even">
<td style="text-align: left;">rideable_type</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">11</td>
<td style="text-align: right;">13</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">3</td>
<td style="text-align: right;">0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">started_at</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">19</td>
<td style="text-align: right;">19</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">3761873</td>
<td style="text-align: right;">0</td>
</tr>
<tr class="even">
<td style="text-align: left;">ended_at</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">19</td>
<td style="text-align: right;">19</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">3774490</td>
<td style="text-align: right;">0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">start_station_name</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">7</td>
<td style="text-align: right;">64</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1529</td>
<td style="text-align: right;">0</td>
</tr>
<tr class="even">
<td style="text-align: left;">start_station_id</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">3</td>
<td style="text-align: right;">44</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1259</td>
<td style="text-align: right;">0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">end_station_name</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">10</td>
<td style="text-align: right;">64</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1575</td>
<td style="text-align: right;">0</td>
</tr>
<tr class="even">
<td style="text-align: left;">end_station_id</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">3</td>
<td style="text-align: right;">44</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1273</td>
<td style="text-align: right;">0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">member_casual</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">6</td>
<td style="text-align: right;">6</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">2</td>
<td style="text-align: right;">0</td>
</tr>
<tr class="even">
<td style="text-align: left;">day_of_week</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">6</td>
<td style="text-align: right;">9</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">7</td>
<td style="text-align: right;">0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">season</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">6</td>
<td style="text-align: right;">6</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">4</td>
<td style="text-align: right;">0</td>
</tr>
</tbody>
</table>

**Variable type: numeric**

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 10%" />
<col style="width: 14%" />
<col style="width: 8%" />
<col style="width: 9%" />
<col style="width: 7%" />
<col style="width: 7%" />
<col style="width: 8%" />
<col style="width: 8%" />
<col style="width: 11%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">skim_variable</th>
<th style="text-align: right;">n_missing</th>
<th style="text-align: right;">complete_rate</th>
<th style="text-align: right;">mean</th>
<th style="text-align: right;">sd</th>
<th style="text-align: right;">p0</th>
<th style="text-align: right;">p25</th>
<th style="text-align: right;">p50</th>
<th style="text-align: right;">p75</th>
<th style="text-align: right;">p100</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">start_lat</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">41.90</td>
<td style="text-align: right;">0.04</td>
<td style="text-align: right;">41.65</td>
<td style="text-align: right;">41.88</td>
<td style="text-align: right;">41.90</td>
<td style="text-align: right;">41.93</td>
<td style="text-align: right;">45.64</td>
</tr>
<tr class="even">
<td style="text-align: left;">start_lng</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">-87.64</td>
<td style="text-align: right;">0.03</td>
<td style="text-align: right;">-87.83</td>
<td style="text-align: right;">-87.66</td>
<td style="text-align: right;">-87.64</td>
<td style="text-align: right;">-87.63</td>
<td style="text-align: right;">-73.80</td>
</tr>
<tr class="odd">
<td style="text-align: left;">end_lat</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">41.90</td>
<td style="text-align: right;">0.07</td>
<td style="text-align: right;">0.00</td>
<td style="text-align: right;">41.88</td>
<td style="text-align: right;">41.90</td>
<td style="text-align: right;">41.93</td>
<td style="text-align: right;">42.06</td>
</tr>
<tr class="even">
<td style="text-align: left;">end_lng</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">-87.64</td>
<td style="text-align: right;">0.11</td>
<td style="text-align: right;">-87.83</td>
<td style="text-align: right;">-87.66</td>
<td style="text-align: right;">-87.64</td>
<td style="text-align: right;">-87.63</td>
<td style="text-align: right;">0.00</td>
</tr>
<tr class="odd">
<td style="text-align: left;">ride_length</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">1047.23</td>
<td style="text-align: right;">3270.56</td>
<td style="text-align: right;">60.00</td>
<td style="text-align: right;">376.00</td>
<td style="text-align: right;">649.00</td>
<td style="text-align: right;">1157.00</td>
<td style="text-align: right;">2061244.00</td>
</tr>
<tr class="even">
<td style="text-align: left;">distance</td>
<td style="text-align: right;">0</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">2144.30</td>
<td style="text-align: right;">12633.13</td>
<td style="text-align: right;">0.00</td>
<td style="text-align: right;">914.03</td>
<td style="text-align: right;">1595.60</td>
<td style="text-align: right;">2773.13</td>
<td style="text-align: right;">9825063.44</td>
</tr>
</tbody>
</table>

#### We gonna analyze the following aspects to illustrate the differences between Casual and Member users.

-   All year round data analysis:

    -   Frequency of rides grouped by user type: casual or member

<!-- -->

    prepared_all %>% ggplot(aes(x = member_casual, group = rideable_type, fill = rideable_type)) +
      geom_bar()+
      labs(x = "User Type",
           y = "Frequency with aggregated ride type")

![](/assets/img/data%20analyzing%20-%20count%20of%20rides%20grouped%20by%20user%20type:%20casual%20or%20member-1.png)

-   Average riding time(s) per ride grouped by user type: casual or
    member

<!-- -->

    prepared_all %>%
      group_by(member_casual) %>%
      summarize(mlen = mean(ride_length)) %>%
      ggplot(aes(x = member_casual, y = mlen, fill = member_casual)) +
      geom_bar(stat = 'identity') +
        labs(x = "User Type",
           y = "Average riding time(s)")

![](/assets/img/data%20analyzing%20-%20average%20ride_length%20grouped%20by%20user%20type:%20casual%20or%20member-1.png)

-   Average riding distance(m) per ride grouped by user type: casual or
    member

<!-- -->

    prepared_all %>%
      group_by(member_casual) %>%
      summarize(mlen = mean(distance)) %>%
      ggplot(aes(x = member_casual, y = mlen, fill = member_casual)) +
      geom_bar(stat = 'identity')  +
        labs(x = "User Type",
           y = "Average riding distance(m)")

![](/assets/img/data%20analyzing%20-%20average%20distance%20grouped%20by%20user%20type:%20casual%20or%20member-1.png)

> Finding 1: The annual data shows that the frequency of members using
> shared bicycles is one-third higher than that of casual users.

> Finding 2: However, the average riding time(s) per ride of casual
> users is twice that of annual members, while the average riding
> distance(m) of two groups are almost same.

-   Involving day of week dimension to differentiate user behaviors:

    -   Frequency of rides per day of the week grouped by user type:
        casual or member

<!-- -->

    options(dplyr.summarise.inform = FALSE)
    # set up factor and level to plot bar from Monday to Sunday accordingly.
    prepared_all$day_of_week <- factor(prepared_all$day_of_week, levels = c("Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"))
    prepared_all %>% ggplot(aes(x = day_of_week, group = rideable_type, fill = rideable_type)) +
      geom_bar()+
      theme(axis.text.x = element_text(angle=45, vjust=.5, hjust=1))+
      facet_wrap(~member_casual)+
        labs(x = "Day of Week",
           y = "Frequency with aggregated ride type")

![](/assets/img/data%20analyzing%20-%20count%20of%20rides%20per%20day%20of%20the%20week%20grouped%20by%20user%20type:%20casual%20or%20member-1.png)

-   Average riding time(s) per day of the week grouped by user type:
    casual or member

<!-- -->

    temp <- prepared_all %>%
      group_by(day_of_week, member_casual) %>%
      summarize(mlen = mean(ride_length))
    temp$day_of_week <- factor(temp$day_of_week, levels = c("Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"))
    temp %>% ggplot(aes(x = day_of_week, y = mlen, fill = member_casual)) +
      geom_bar(stat = 'identity')+
      theme(axis.text.x = element_text(angle=45, vjust=.5, hjust=1))+
      facet_wrap(~member_casual)+
        labs(x = "Day of Week",
           y = "Average riding time(s)")

![](/assets/img/average%20ride_length%20per%20day%20of%20the%20week%20grouped%20by%20user%20type:%20casual%20or%20member-1.png)

    rm(temp)

-   Average riding distance(s) per day of the week grouped by user type:
    casual or member

<!-- -->

    temp <- prepared_all %>%
      group_by(day_of_week, member_casual) %>%
      summarize(mlen = mean(distance))
    temp$day_of_week <- factor(temp$day_of_week, levels = c("Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"))
    temp %>% ggplot(aes(x = day_of_week, y = mlen, fill = member_casual)) +
      geom_bar(stat = 'identity')+
      theme(axis.text.x = element_text(angle=45, vjust=.5, hjust=1))+
      facet_wrap(~member_casual)+
        labs(x = "Day of Week",
           y = "Average riding distance(m)")

![](/assets/img/average%20distance%20per%20day%20of%20the%20week%20grouped%20by%20user%20type:%20casual%20or%20member-1.png)

    rm(temp)

> Finding 3: The frequency patterns of annual members and casual members
> per day of week through out the whole year are different. Casual
> members tend to use shared bicycles more frequently on weekends, while
> annual members use shared bicycles more frequently on weekdays.

> Finding 4: If we spread the average riding time per ride into the day
> of weeks, we can clearly find out casual members have a longer riding
> time per ride on weekends than they do on weekdays, while this
> difference is almost non-existent among annual members

> Finding 5: If we spread the average riding distance into the day of
> weeks, both casual users and annual members cycled slightly higher
> distances on Wednesdays and weekends than at other times

-   Involving rideable type dimension to differentiate user behaviors: :

    -   Frequency of rides per rideable type grouped by user type:
        casual or member

<!-- -->

    options(dplyr.summarise.inform = FALSE)
    prepared_all %>% ggplot(aes(x = rideable_type, group = rideable_type, fill = rideable_type)) +
      geom_bar()+
      theme(axis.text.x = element_text(angle=45, vjust=.5, hjust=1))+
      facet_wrap(~member_casual)+
        labs(x = "Ride type",
           y = "Frequency")

![](/assets/img/data%20analyzing%20-%20count%20of%20rides%20per%20rideable_type%20grouped%20by%20user%20type:%20casual%20or%20member-1.png)

-   Average riding time(s) per rideable\_type grouped by user type:
    casual or member

<!-- -->

    prepared_all %>%
      group_by(rideable_type, member_casual) %>%
      summarize(mlen = mean(ride_length)) %>%
      ggplot(aes(x = rideable_type, y = mlen, fill = member_casual)) +
      geom_bar(stat = 'identity')+
      theme(axis.text.x = element_text(angle=45, vjust=.5, hjust=1))+
      facet_wrap(~member_casual)+
        labs(x = "Ride type",
           y = "Average riding time(s)")

![](/assets/img/average%20ride_length%20per%20rideable_type%20grouped%20by%20user%20type:%20casual%20or%20member-1.png)

-   Average riding distance per rideable type grouped by user type:
    casual or member

<!-- -->

    prepared_all %>%
      group_by(rideable_type, member_casual) %>%
      summarize(mlen = mean(distance)) %>%
      ggplot(aes(x = rideable_type, y = mlen, fill = member_casual)) +
      geom_bar(stat = 'identity')+
      theme(axis.text.x = element_text(angle=45, vjust=.5, hjust=1))+
      facet_wrap(~member_casual)+
        labs(x = "Ride type",
           y = "Average riding distance(m)")

![](/assets/img/average%20distance%20per%20rideable_type%20grouped%20by%20user%20type:%20casual%20or%20member-1.png)

> Finding 6: All users (annual members more significant) are more
> inclined to use classic bikes, then electric bikes. Docked bikes are
> minimally used among casual users and never used among annual members.

> Finding 7: Surprisingly, the average riding time on an docked bike
> turns out to be the longest even though few casual users use it.

> Finding 8: The average riding distance of electric bikes is the
> highest one, but not noticeable among different bike types.

-   Involving season dimension to differentiate user behaviors:

    -   Frequency of rides per season grouped by user type: casual or
        member

<!-- -->

    # set up factor and level to plot bar from spring to winter accordingly.
    prepared_all$season <- factor(prepared_all$season, levels = c("spring", "summer", "autumm", "winter"))
    prepared_all %>% ggplot(aes(x = season, group = rideable_type, fill = rideable_type)) +
      geom_bar()+
      theme(axis.text.x = element_text(angle=45, vjust=.5, hjust=1))+
      facet_wrap(~member_casual)+
        labs(x = "Day of Week",
           y = "Frequency with aggregated ride type")

![](/assets/img/Frequency%20of%20rides%20per%20season%20grouped%20by%20user%20type:%20casual%20or%20member-1.png)

-   Average riding time(s) per season grouped by user type: casual or
    member

<!-- -->

    options(dplyr.summarise.inform = FALSE)
    temp <- prepared_all %>%
      group_by(season, member_casual) %>%
      summarize(mlen = mean(ride_length))
    temp$season <- factor(temp$season, levels = c("spring", "summer", "autumm", "winter"))
    temp %>% ggplot(aes(x = season, y = mlen, fill = member_casual)) +
      geom_bar(stat = 'identity')+
      theme(axis.text.x = element_text(angle=45, vjust=.5, hjust=1))+
      facet_wrap(~member_casual)+
        labs(x = "Season",
           y = "Average riding time(s)")

![](/assets/img/average%20ride_length%20per%20season%20grouped%20by%20user%20type:%20casual%20or%20member-1.png)

    rm(temp)

-   Average riding distance per season grouped by user type: casual or
    member

<!-- -->

    options(dplyr.summarise.inform = FALSE)
    temp <- prepared_all %>%
      group_by(season, member_casual) %>%
      summarize(mlen = mean(distance))
    temp$season <- factor(temp$season, levels = c("spring", "summer", "autumm", "winter"))
    temp %>% ggplot(aes(x = season, y = mlen, fill = member_casual)) +
      geom_bar(stat = 'identity')+
      theme(axis.text.x = element_text(angle=45, vjust=.5, hjust=1))+
      facet_wrap(~member_casual)+
        labs(x = "Season",
           y = "Average riding distance(m)")

![](/assets/img/average%20distance%20per%20season%20grouped%20by%20user%20type:%20casual%20or%20member-1.png)

    rm(temp)

> Finding 9: For all users, the seasons in which shared bikes are mainly
> used are summer and autumn

> Finding 10: Surprisingly, for casual users, although the frequency of
> using shared bikes is relatively high in summer and autumn, the
> average riding time(s) per use is shorter than in spring and winter.
> This pattern was not found in annual members

> Finding 11: In warm seasons, the average riding distance of shared
> bikes is generally higher than in cold seasons among all users

-   Involving Hour dimension to differentiate user behaviors:

    -   Frequency of rides per hour grouped by user type: casual or
        member

<!-- -->

    temp <- prepared_all %>% mutate(hour = as.character(hour(started_at)))
    options(dplyr.summarise.inform = FALSE)
    # set up factor and level to plot bar from 0 to 23.
    temp$hour <- factor(temp$hour, levels = c("0","1","2","3","4","5","6","7","8","9","10","11","12","13","14","15","16","17","18","19","20","21","22","23"))
    temp %>% ggplot(aes(x = hour, group = rideable_type, fill = rideable_type)) +
      geom_bar()+
      theme(axis.text.x = element_text(angle=45, vjust=.5, hjust=1))+
      facet_wrap(~member_casual)+
      labs(x = "hour",
           y = "Frequency with aggregated ride type")

![](/assets/img/data%20analyzing%20-%20count%20of%20rides%20per%20hour%20grouped%20by%20user%20type:%20casual%20or%20member-1.png)

    rm(temp)

-   Average riding time(s) per hour grouped by user type: casual or
    member

<!-- -->

    temp <- prepared_all %>% mutate(hour = as.character(hour(started_at)))
    temp1 <- temp %>%
      group_by(hour, member_casual) %>%
      summarize(mlen = mean(ride_length))
    temp1$hour <- factor(temp1$hour, levels = c("0","1","2","3","4","5","6","7","8","9","10","11","12","13","14","15","16","17","18","19","20","21","22","23"))
    temp1 %>% ggplot(aes(x = hour, y = mlen, fill = member_casual)) +
      geom_bar(stat = 'identity')+
      theme(axis.text.x = element_text(angle=45, vjust=.5, hjust=1))+
      facet_wrap(~member_casual)+
      labs(x = "Hour",
           y = "Average riding time(s)")

![](/assets/img/data%20analyzing%20-%20average%20ride_length%20per%20hour%20grouped%20by%20user%20type:%20casual%20or%20member-1.png)

    rm(temp)
    rm(temp1)

-   Average riding distance per hour grouped by user type: casual or
    member

<!-- -->

    temp <- prepared_all %>% mutate(hour = as.character(hour(started_at)))
    temp1 <- temp %>%
      group_by(hour, member_casual) %>%
      summarize(mlen = mean(distance))
    temp1$hour <- factor(temp1$hour, levels = c("0","1","2","3","4","5","6","7","8","9","10","11","12","13","14","15","16","17","18","19","20","21","22","23"))
    temp1 %>% ggplot(aes(x = hour, y = mlen, fill = member_casual)) +
      geom_bar(stat = 'identity')+
      theme(axis.text.x = element_text(angle=45, vjust=.5, hjust=1))+
      facet_wrap(~member_casual)+
      labs(x = "hour",
           y = "Average riding distance(m)")

![](/assets/img/data%20analyzing%20-%20average%20distance%20per%20hour%20grouped%20by%20user%20type:%20casual%20or%20member-1.png)

    rm(temp)
    rm(temp1)

> Finding 12: For the two groups of users, from 6:00 in the morning, the
> frequency of using shared bicycles gradually increases until it
> reaches the peak at 17:00 in the afternoon.

> Finding 13: Between 7 am and 9 am, for annual members, the usage of
> shared bicycles reaches a small peak as well. This pattern is not
> found among casual users.

> Finding 14: For casual users, the frequency of usage is basically
> positively correlated with the average riding time. However, for
> annual members, the average riding time remains relatively stable, and
> does not change over time with changes in frequency of rides.

> Finding 15: For the average riding distance, there is no significant
> pattern among different time slots for each group.

### Share and Act: A clear statement of the business task + recommendations based on your analysis

#### Reviewing business task/gut feelings and summerize our findings against analytic results

Before we offer any recommendation, let’s review the business tasks, our
ideas/gut feelings at the very beginning and the findings after data
analysis.

-   We are given a scenario that a new marketing strategy will be rolled
    out for better fit the company’s future development - converting
    existing casual users to annual members effectively. We are assigned
    a task to analyze the differences between casual users and annual
    members.

-   We came up with seleral ideas/gut feelings before data tell us the
    ‘truth’. In the end, it was found that some of them were not
    significant, and some were even contrary to our cognition.

-   We got, in total, 15 findings after analysis based on metrics like
    frequency of rides, average riding time, average riding distance and
    dimensions like rideable type, day of the week, season and hour
    separation. And we can tell the following differences between casual
    users and annual members:

> casual users：The frequency of using shared bicycles is low, and the
> speed of cycling is faster in spring and summer. The main purpose of
> using shared bicycles is for weekend amusement. The movement distance
> per unit of time(speed) is relatively slow, more like wandering on the
> road. It is also used for short-distance activities(shopping/dinner,
> etc.) after getting off work. When there is no dockless bicycle
> nearby, docked one will also be selected, however, since there are
> relatively few docks, the user experience is not good enough (the
> average riding time of using docked bicycles is longer)

> annual members: The frequency of using shared bicycles is high, and
> the speed of cycling is stable. The main purpose of using shared
> bicycles is for commute purposes. The movement distance per unit of
> time(speed) more stable during weekdays, indicating they ride bikes on
> a fix distance(home to office, vise versa) with fix speed(stable road
> conditions during work days). it is also used for pleasure on weekends
> with relatively low frequency, riding time and distance. When there is
> no dockless bicycle nearby, they will never choose the docked ones
> (mainly because parking is inconvenient and they should go to work on
> time)

> There is another finding we don’t know the reason: The average
> distance traveled on Wednesday is slightly higher than on other
> weekdays for all riders. That might be caused by some special events
> in Chicago.

#### Recommendations based on your analysis

-   For existing casual users, it is very worth to encourag them to use
    shared bikes to go to and get off the work. Meanwhile, providing
    membership experience for them who use shared bicycles for going to
    or getting off work on consecutive working days is a very good way
    for promotion and conversion.

-   Put more dockless bikes to the market so that casual users can
    reduce the frequency of using docked bicycles; at the same time,
    reducing the average cost of using docked bicycles to offset the
    additional costs of casual users is another good approach for
    promotion and conversion.

-   Increasing the intensity of placing advertisements in restaurants
    and entertainment venues near the workplaces to expose more brand
    and utilities of shared bikes is also a good way to for promotion
    and conversion to casual users.
