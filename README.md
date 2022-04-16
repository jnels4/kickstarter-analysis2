# kickstarter-analysis2
Analysis of kickstarter data centering on theater -> plays 
# Kickstarting with Excel

## Overview of Project
This project went through multiple phases of analysis on kickstarter data from the year 2009 through 2017.  Our client was interested in creating a kickstarter campaign focused on theater and in particular plays.  Initially, we focused our analysis on the Great Britian theater/play kickstart scene, from the initial overview of the data we provided our client with our assessment.  After reviewing our initial analysis, our client wanted us to focus on a few specific metrics: Success/Fail/Canceled theater campaigns by year, and the percentage of campaigns that were successful/failed or canceled based on the amount of money requested in their goal.  For this analysis we looked at ALL kickstarter plays created from 2009 through 2017 to reach a more robust conclusion. 

### Purpose

The purpose of this analysis was to determine which month our client would have success and where they should place their initial kickstarter goal to achieve the best chance of success.

## Analysis and Challenges

This analyis went through two main phases. Firstly the analysis of outcomes (success/fail/cancled) based on their lauch date and the overall success of a campaign based on their stated monetary goals.

### Analysis of Outcomes Based on Launch Date

The first phase of analysis was to look at how successful (or not) a campaign was based on it's launch date.  We created a view of our kickstarter data that focused on the parent category - theater - and the years of data we had (2009 - 2017), based on this view, and the associated chart (see below), it seems as if historically the most successful month to launch a campaign is May, followed by June and July.  Historically, May saw 111 successful campaigns, 52 failed campaigns and 3 cancled campaigns.  May shows a 67% success over the years 2009 through 2017, and proves to be the month with the highest percentage of successful campaigns. June (65%) and July (63%), are close runners-up for successful kickstarter theater campaigns.

![TheaterOutcomesVsLaunch](https://user-images.githubusercontent.com/6634774/163687631-1e7a05dc-426d-4e0b-a494-2c7fb4155ef6.png)


### Analysis of Outcomes Based on Goals

The next phase of analysis focused on the requested goal and it's associated rate of success (see chart below).  For this phase, we looked specifically at kickstarters for plays, as our client is interested in producing a play.  We created "goal bands", to group the goals within a range of requested funding.  From this view, we concluded that a campaign created with a goal of less than $5000, would potentially see the greatest success.  The band for campaign created below 1000 saw a 76% success rate, and campaigns created with a requested goal of 1000 to 4999 saw a 73% success rate.  It would be reasonable to suggest that our client create a campaign that can be funded for less than $5000. 


![OutcomesVsGoals](https://user-images.githubusercontent.com/6634774/163687644-d263e90f-b4ae-46f8-9eb7-e6cfbf4fb324.png)


### Challenges and Difficulties Encountered

Challenge 1: Creating goal bands and making sure that the correct totals added up.  To address this challenge, I first created my formulas for each of the 12 groups, ensuring there were no syntactical errors.  I then created a formula to sum up my count.  Next, I created a COUNTIF() that would total all of the kickstarter play campaigns with a goal greater than 0.  If the sum of my current data AND the COUNTIF() matched, I knew I had the correct number of campaigns.  I did this for Success/Failed/Cancled projects to ensure my count was correct.

Challenge 2: Tedious modification.  Creating 12 disctinct formulae was both tedious, time consuming and prone to error.  To work more efficiently, I horizontally copied my formula into the 2 adjacent cells (Success -> failed & cancled), I then highlighted the "failed" row, and used find&replace to change success to fail.  I did this for the cancled column as well.  To ensure my counts were still correct, I used the same method from challenge 1 to double check my work.

Challenge 3: Effciency is king.  I used the new Outcomes table to create a pivot chart to produce the line graph needed for analysis.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
    1. Campaigns created in May have the greatest chance of success. (67%)
    2. June and July could be suitable replacements if necesary (65%/63% respectively).
- What can you conclude about the Outcomes based on Goals?
    1. Campaigns created below $5000 will have the greatest chance of success. Less than 1000 has a 76% chance, and 1000 - 5000 is 72%, combined the chance of success for a campaign below $5000 is 73%.
- What are some limitations of this dataset?
    1. This data only look at 2009 - 2017, which  may be outdated for a campaign starting in 2022.
    2. This data only shows how successful the kickstarter was, not the actual project itself.
    3. The data shows no metrics for if successful campaigns went on to be officially launched for consumption.
    4. There is no information on kickstarter success vs actual revenue for a project.
- What are some other possible tables and/or graphs that we could create?
    1. We can look specifically at Launch date + Goal.  We can use this new table to determine how successful a campaign is by its launch date and requested goal.
    2. We can analysis of the entire theater subcategory, not just plays.  This would give a better idea of how the entire category is distributed success/fail wise.
    3. We can also look at kickstarters for theater space and see if it makes sense to also suggest a concurrent campaign to purchase/renovate a theater space.
