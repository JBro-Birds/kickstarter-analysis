# Kickstarting with Excel

## Overview of Project
This project is a second analysis request from Louise after her play "Fever" came close to its fundraising goal in a short amount of time.  She now wants to know how different campaigns fared in relation to their launch dates and their funding goals.

### Purpose
The purpose is to determine how different theater campaigns fared in relation to their launch dates and how different play campaigns fared in relation to their funding goals.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
I created a line chart to show "theater" outcomes based on launch date.  The kickstarter campaign dataset includes the parent category "theater", outcome categories of "successful", "failed" and "canceled", and corresponding campaign launch dates.  With the launch date of each campaign event being defined by a time stamp in the original dataset I had to convert the time stamp values into a date format "mm/dd/yyyy" by use of a formula and then apply the "YEAR" function to convert the launch date to the year in which the date incurred in.  After doing so I first created a pivot table filtered on the "theater" category and on "all" years from the dataset.  The pivot table shows by calendar month the number of "successful", "failed" and "canceled" campaigns.  I created a line chart that plots the data from the pivot table.  

<img width="384" alt="Theater_Outcomes_vs_Launch" src="https://user-images.githubusercontent.com/110485380/190402816-4ab250a2-7148-44cd-8b6b-7836da08c2d0.png">

![Theater Outcomes vs Launch_Date](https://github.com/JBro-Birds/kickstarter-analysis/resouces/"Theater_Outcomes_vs_Launch.png")

### Analysis of Outcomes Based on Goals
I created a line chart for "play" outcomes based on goals by showing outcome percentage by goal range $values.  The kickstarter dataset includes the subcategory "plays", outcome categories of "successful", "failed" and "canceled", and corresponding campaign "goal" $value.  Due to the vast number of unique goal $values across all the "play" campaigns a defined $range was created to categorize each campaign into a range $value category.  The "COUNTIFS" forumla was used to determine the number of campaigns by goal range $value and by outcome category.  The percentage for each outcome by range $value is formulated by the number of each specific outcome divided by the total number of outcomes by range $value. I created a line chart that plots the data from the pivot table. 

<img width="338" alt="Outcomes_vs_Goals" src="https://user-images.githubusercontent.com/110485380/190402732-2ed5c645-6b06-4fe4-859f-304016c2f458.png">

### Challenges and Difficulties Encountered
Challenges and difficulties encountered centered around certain data attributes that needed to be convereted into different formats and creating ranges $values to categorize goal $values in to.  Both of these challenges needed to be addressed in order to create effective pivot tables and corresponding line charts.  For the outcomes based on launch date analysis the time stamp format for the launch date would not be an effective format to show in the chart because it would be next to impossible to visualize and understand what the chart is showing.  Changing the format by use of formulas and creating the "YEAR" attribute simplified the launch date for the analysis and chart.  Likewise for the outcomes based on goals analysis if the large volume of unique goal $values were not mapped into range categories by the "COUNTIFS" formula the pivot table would be cumbersome to create and the chart would be next to impossible to understand. By using Excel formulas these challenges were resolved and effective line charts were produced in order to provide the necessary analysis for Louise's request.

## Results

### Two conclusions drawn about the outcomes based on launch date
The months of May, June and July are the optimal months to launch crowdfunding campaigns for "theater" projects when compared to other months of the year due to the higher rate of successful campaigns vs. failed compaigns.  The least optimal month to launch a campaign is the month of December in which it is nearly a 50/50 chance of a successful vs. failed campaign.

### Conclusion about the outcomes based on goals
The better chance for a succesful crowdfunding campaign for "play" projects is to set the goal $value to less than $5,000.  When goal $values are set greater than $5,000 the failure rate is typically higher than the success rate; there are a couple of higher range $value categories in which the success rate is higher than the failure rate but due to the low number of campaigns in the categories it is most likely driven by outliers.

### Some limitations of this dataset
There are a few limitations of this dataset.  There could be more data attributes provided that would better help determine potential campaign outcome status.  Examples would be main communication method used to contact targeted pledgers, if there was a follow-up method used to reach out to unresponsive  targeted pledgers along with the timing of the followup, and demograpics of the targeted pledgers.  In addition, providing one or more of these attributes mentioned could better explain any outliers.

### Other possible tables and/or graphs that could be created
There are a few other possible tables and/or graphs that could be created to show visuals of the results.  A box and whisker chart comparing distribution of campaign goals vs. distribution of total amount pledged by time period (by year or by month).  A bar graph comparing campaign goals vs. pledged by outcome by period (by year or by month).  A table showing descriptive statistics of successful and failed compaigns.
