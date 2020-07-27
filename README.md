# An Analysis of Kickstarter Campaigns
Performing analysis on Kickstarter data to uncover trends

# Kickstarting with Excel

## Overview of Project

Microsoft Excel was one of the first programs to integrate spreadsheets with charts and graphs. Excel is a great tool to visualize, manipulate, and evaluate data. With the analytical tools available in Excel, a user can analyze significant amounts of data to uncover trends and patterns that may impact a projects' decision making. In this project, we analyzed a data set consisting of over 4,000 crowdfunding projects to discover hidden trends.

### Purpose

In this project we will sharpen our Excel skills by applying several techniques that would allow us to organize and manipulate data incredibly fast. From using conditionals to help users better visualize relative data, to carrying out extremely complicated forms of statistical analysis, Excel can increase productivity in the workspace exponentially. It is one thing to store and manage large quantities of data, but it is another to discover relationships hidden among the lines.

## Analysis and Challenges

There were several notable pieces of analysis. Let us discuss two of our findings.

### Analysis of Outcomes Based on Launch Date
![Outcomes_Based_on_Launch_Date](https://user-images.githubusercontent.com/68082808/88490747-db8b2100-cf6b-11ea-8553-fa711a2aeddd.png)

My team and I considered creating a pivot table on Excel to be the most efficient way to reorganize our data, group them, and then count them. We found sing a pivot table to be exceptionally useful in finding a correlation between the success of theatrical productions, and what time of the year the Kickstarter launched. Excel’s pivot tables have the ability to take the data declared in the original spreadsheet, find the dates of all of the matching Kickstarters matching our filters, and give us an accurate count of the success (or failure/cancellation) of theatrical productions per month.


### Analysis of Outcomes Based on Goals
![Outcomes_Based_on_Goal](https://user-images.githubusercontent.com/68082808/88491444-cc5aa200-cf70-11ea-9444-4cfdcad493b9.png)

My team and I filtered through the many Kickstarter campaigns and chose to work with the most prevalent subcategory, plays! Our objective was to discover if there was a correlation between the target goal of the Kickstarter Campaigns (in U.S. Dollars), and their success, or lack thereof. We found Excels built in =COUNTIFS() function easily does the job of filtering the data, including only plays and distinguishing goal amount. By adding the criteria “=success”, “=failed”, or “=canceled”, and imposing the =COUNTIFS() function across a table, the user can easily see find the numerical count of outcomes based on goal. It is however kinder to the eye to visualize percentages because they are very useful in quantifying change. Therefore, the chart is based on the count between the categories “Success”, “Failure”, and “Canceled”, over the total number of plays within that goal group.

### Challenges and Difficulties Encountered

It is good to think of pivot tables and filters as a food processor that can slice and dice data. They help users answer questions, and hopefully uncover data, however its always possible to come up against a wall. I will go over two errors I came across when constructing the two tables above, and how I got around them.

Firstly, lets go over the =COUNTIFS() formula. I was wondering how to impose two numerical restrictions on the goal column making sure the inputted goals are greater than or equal to x, and greater than y. I first thought to make one =COUNTIF() statement following all the correct criteria, including goal values greater than or equal to x, and then subtracting another =COUNTIFS() statement including goal values that also satisfy the conditions greater than my upper limit y. This sadly returned an error. Its important to note that the =COUNTIFS() function can take several criteria, making sure that inputted goals are greater than or equal to x, and greater than y.

Not everything can be automated! Yes, Excel allows you to impose a function on several cells, but sometimes you must resort to copy and pasting functions and then manually inputting unique data. Be sure to check for typos, and remember, CTRL+F is your friend and can help you replace recurring data across several cells.


## Results

With regards to the table displaying outcomes based on goal, the chart is very easily misinterpreted. The chart itself does not express how many plays there are within each goal interval. For instance, there are 889 plays that set a goal between zero and 9,999 U.S. Dollars, whereas there were only 189 plays that set a goal greater than 10,000 U.S. Dollars. Therefore, this chart has a severe drawback. The following stacked bar graph visually represents the skew of the count of plays with respect to their outcome and set goal.

![Outcomes_Based_on_Goal (Stacked Bar)](https://user-images.githubusercontent.com/68082808/88496647-db9b1900-cf8b-11ea-81b3-c999ab15c6d9.png)

If there existed more plays that set a target goal over 10,000 U.S. Dollars, then the graph would more accurately represent the relationship between the set goal, and the outcome. Nonetheless, I believe the first three intervals, goals less than 1,000, goals between 1,000 and 4,999, and goals between 5,000 and 9,999, have a large enough sample size to draw a conclusion between the set goal and the success rate. This is only my subjective opinion, and it would be best to use proven statistical formulas to weigh in significant data. The chart tells us that the less a campaign ask for, the more likely the campaign is to succeed, and this generally makes sense. The less a campaign asks for, the easier it is to reach that target. This points to another drawback in the data set, it fails to indicate the methods of fundraising! To get a more accurate data set, it would be best to ask how the campaign advertised, and who they advertised to. I say this because perhaps the relevance of the play to whom the advertisements were tailored to play a role in success rate.

One can observe an obvious correlation between the date a theatrical Kickstarter campaign launches, and its outcome. There is a jump in success rate between the months of March and May, and then as the year goes on, the rate of success drops at a near consistent rate until December. The failure line stays rather steady throughout the year, especially when comparing it to the success line. One must take into consideration the limitations of the data set. Firstly, this is only a collection of theatrical campaigns initiated on Kickstarter, and do not account for the total pool of theatrical performances.

Our objective was to use Microsoft Excel to find relationships hidden beneath thousands of items, and perhaps identify the limitations of data sets. Before setting to work applying formulas and other advanced analytical techniques, an analyst must inquire whether their collection of data serves to answer their questions fairly. With the data collected in this project regarding Kickstarter campaigns, analysts from all fields may find some inquisitive relationships hidden within the lines. For instance, a business may be interested in finding the average percentage funded for a certain category across several nations, as that may indicate where the industry lies. Another business may take a similar approach to the data, inquiring about the average number of backers per country with respect to the average percentage funded, filtered the category of their industry.

