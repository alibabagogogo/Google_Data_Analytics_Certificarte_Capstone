# Google_Data_Analytics_Certificarte_Capstone
Case Study: How Does a Bike-Share Navigate Speedy Success?

## Scenario

You are a junior data analyst working in the marketing analyst team at Cyclistic, a bike-share company in Chicago. The director of marketing believes the company's future success depends on maximizing the number of annual memberships. Therefore, your team wants to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, your team will design a new marketing strategy to convert casual riders into annual members. But first, Cyclistic executives must approve your recommendations, so they must be backed up with compelling data insights and professional data visualizations.

## Characters and teams

* Cyclistic: A bike-share program that features more than 5,800 bicycles and 600 docking stations. Cyclistic sets itself apart by also offering reclining bikes, hand tricycles, and cargo bikes, making bike-share more inclusive to people with disabilities and riders who can't use a standard two-wheeled bike. The majority of riders opt for traditional bikes; about 8% of riders use the assistive options. Cyclistic users are more likely to ride for leisure, but about 30% use them to commute to work each day.
* Lily Moreno: The director of marketing and your manager. Moreno is responsible for the development of campaigns and initiatives to promote the bike-share program. These may include email, social media, and other channels.
* Cyclistic marketing analytics team: A team of data analysts who are responsible for collecting, analyzing, and reporting data that helps guide Cyclistic marketing strategy. You joined this team six months ago and have been busy learning about Cyclistic's mission and business goals --- as well as how you, as a junior data analyst, can help Cyclistic achieve them.
* Cyclistic executive team: The notoriously detail-oriented executive team will decide whether to approve the recommended marketing program.

## About the Company

In 2016, Cyclistic launched a successful bike-share offering. Since then, the program has grown to a fleet of 5,824 bicycles that are geotracked and locked into a network of 692 stations across Chicago. The bikes can be unlocked from one station and returned to any other station in the system anytime.

Until now, Cyclistic's marketing strategy relied on building general awareness and appealing to broad consumer segments. One approach that helped make these things possible was the flexibility of its pricing plans: single-ride passes, full-day passes, and annual memberships. Customers who purchase single-ride or full-day passes are referred to as casual riders. Customers who purchase annual memberships are Cyclistic members.

Cyclistic's finance analysts have concluded that annual members are much more profitable than casual riders. Although the pricing flexibility helps Cyclistic attract more customers, Moreno believes that maximizing the number of annual members will be key to future growth. Rather than creating a marketing campaign that targets all-new customers, Moreno believes there is a very good chance to convert casual riders into members. She notes that casual riders are already aware of the Cyclistic program and have chosen Cyclistic for their mobility needs.

Moreno has set a clear goal: Design marketing strategies aimed at converting casual riders into annual members. In order to do that, however, ***the marketing analyst team needs to better understand how annual members and casual riders differ***, why casual riders would buy a membership, and how digital media could affect their marketing tactics. Moreno and her team are interested in analyzing the Cyclistic historical bike trip data to identify trends.

## Roadmap for successful data analysis deliveries:

| Roadmap |                      Deliverable                       |
|:-------:|:------------------------------------------------------:|
|   Ask   |         A clear statement of the business task         |
| Prepare |         A description of all data sources used         |
| Process | Documentations of any cleaning or manipulation of data |
|  Share  |       Supporting visualizations and key findings       |
|   Ask   |         A clear statement of the business task         |
|   Act   | Your top three recommendations based on your analysis  |

### Ask: A clear statement of the business task

Based on the given context about this data-driven decision making project, we have to carefully think about business task before we proceed to any further steps. There is a hypothesis raised by the director of marketing, who believes "the company's future success depends on maximizing the number of annual memberships". Meanwhile, "the finance analysts have concluded that annual members are much more profitable than casual riders".

Accordingluy, there are mainly two ways to expand the number of annual memberships, one is launching marketing campaigns that targets all-new customers, the other one is converting existing casual riders into annual members. After leveraging the pros and cons, costs and expectations, etc., the later one 'should' have a higher conversion rate with lower cost, as casual riders are already aware of the the program and have chosen it for their mobility needs.

Thus, in order to effectively convert the existing casual riders to annual members, it can be broken down into three main aspects:

1.  Finding out differences: How do annual members and casual riders use Cyclistic bikes differently?
2.  Knowing the reasoning for being an annual member: Why would casual riders buy Cyclistic annual memberships?
3.  Setting up effective marketing approaches: How can Cyclistic use digital media to influence casual riders to become members?

We will see that this project is related to the `Question 1` due to dataset limitation mentioned in following "Prepare" step.

Before we go deeper on the dataset itself, general speaking, we should firstly think about in what ways we can differentiate between the two groups of users in the context of participating bike share programs. Here are some rough ideas/gut feelings:

1.  Do casual riders use bicycles for a shorter period of time than the annual members on average?
2.  Do casual riders use bicycles less frequently than annual members within a period of time on average?
3.  Do casual riders use bicycles for a shorter distance than annual members on average?
4.  Do annual members usually use bicycles for commuting(Peaking period from 7:00-9:00 A.M. and 17-19 P.M. per day)? More in summer than winter? 
5.  ... ...

> Ok, you might come up with more ideas. let's leave them here and move on to the remaining phases to explore what we can do with the given dataset (Please keep in mind, in reality, theoretically we could do infinite analysis if we have 'sufficient' dataset. Even if we do not have 'enough' data metrics and dimensions till now, we can somehow try to collect them in the near future to continusly consolidate, update or even completely overturn the analytic results. All in all, data analysis is a process that requires long-term continuous revision)
