+++
categories = ["Exploratory-Analysis"]
coders = []
date = 2020-07-10T23:00:00Z
description = "An Exploratory Analysis on Player Behaviour in Global MapleStory"
github = ["https://github.com/kaishuun/MapleRank-Analysis-of-Maplestory-Players"]
image = "https://res.cloudinary.com/kevinhe/image/upload/v1594505251/kisspng-logo-maplestory-brand-font-naver-blog-syncky-works-5ba3763eb3bda5.9287856415374392947362_rrvzyg.jpg"
title = "MapleRank"
type = "post"
[[tech]]
logo = "https://res.cloudinary.com/kevinhe/image/upload/v1594496492/724px-R_logo.svg_atz0ov.png"
name = "R"
url = "https://cran.r-project.org/"
[[tech]]
logo = "https://res.cloudinary.com/kevinhe/image/upload/v1594496511/1024px-Python-logo-notext.svg_tsqemn.png"
name = "Python"
url = "https://www.python.org/"

+++
The data was gathered on MapleStory Global's official ranking list by using BeautifulSoup4 as a web scrapper. Data aggregation and graphs were done using the Tidyverse set of packages in R.

This is just a snippit of the project, to check out the full documentation, check out my notebook [here](https://github.com/kaishuun/Maplestory-Rankings-Exploratory-Analysis/blob/master/Maplestory%20Analysis.ipynb).


## Introduction
Maplestory has been a popular MMORPG in the early-mid 2000's. Despite its dwindling popularity, it's one of the games I always return to every semester break. One of the big questions that a lot of people have and one that I ask quite frequently to my friends is "What job should I play?"; this question, combined with me recently learning web scraping has led me to find the data myself to look at player behaviour on choosing jobs and worlds. 

In this Exploratory Analysis we will answer the questions of:
- What jobs are popular?
- How do players differ in each worlds?
- What levels do most players end up?

In this Analysis we strictly look at players over level 205.

## Findings

### World Data

![](https://res.cloudinary.com/kevinhe/image/upload/v1594505679/World_Distribution_pg1bhz.png)

Here we see the distribution of players in each world. A common issue in MapleStory is players trying to find an empty map to either train or meso farm, for those who want more of a solo play styler a less populated world such as Elysium would be a perfect fit, while in Bera trying to find a guild or party quest would be much easier. This also shows the popularity and success of Reboot, being a special server where you can't trade with other players and where game enhancements are able to be purchased through mesos instead of money.

### Level Data
![](https://res.cloudinary.com/kevinhe/image/upload/v1594505666/Level_Distribution_per_world_mmz3b7.png)

Next, we take a look at what levels most players are. Player levels for each world are similarly distributed with a peak around level 210 followed by an exponential decrease. This shows that despite reboot being different from the normal worlds, players have a tendency to stop playing around level 210.

### Class Data
![](https://res.cloudinary.com/kevinhe/image/upload/v1594505654/popular_classes_for_each_world_y8cphe.png)

Finally, we take a closer look at what jobs players tend to play more. Kannas tend to be the most popular class in each of the worlds, primarily due to the popularity of meso farming and Kanna's Kishin skill, which boosts up spawn rate of monsters. Following along, explorers top other job types, which makes sense since each explorer category covers 2-3 different jobs (eg. Mages cover Ice/Lightning,Fire/Poison, and Bishop jobs). Looking at least played jobs, these jobs most often are in dire need of skill revamps due to their aging play style or their damage output.

![](https://res.cloudinary.com/kevinhe/image/upload/v1594505641/Max_Level_per_world_rrsxd1.png)

For hardcore players hoping to be the first to hit cap level in their world, many jobs still don't have a level 275 in their world! Reboot has most characters up to level cap, in the normal worlds, rankings are still up for grabs for multiple different jobs.
   
## In Depth Analysis
For a more indepth analysis of player data and more graphs showing the spread of jobs and worlds check out my notebook [here](https://github.com/kaishuun/Maplestory-Rankings-Exploratory-Analysis/blob/master/Maplestory%20Analysis.ipynb) . In there you'll find my code and more in depth commentary of my findings.

## Data Set
Feel free to use my collected data [here](https://github.com/kaishuun/Maplestory-Rankings-Exploratory-Analysis/blob/master/Maplestory%20Rank%20Data.csv) . I gathered the data using a web scraper that took down the rankings of players on the official MapleStory site. Characters data up to level 203 were collected, but only level 205 and above characters were present for this analysis. This data was last updated on June 14. For summary statistics of different Jobs in each world click [here](https://github.com/kaishuun/Maplestory-Rankings-Exploratory-Analysis/blob/master/Summary%20Statistics.csv).
