# kickstarter-analysis
Performing analysis on Kickstarter data to uncover trends.
## Overview of Project
Louise, a playwright started a crowdfunding campaign and noticed that she came close to her fundraising goal in a short amount of time. Now, she would like to learn how different campaigns fared in relation to their launch dates and their funding goals.
### Purpose
The purpose of the project is to determine if launch dates and funding goals affect the outcome of a fundraising campaign.
## Analysis and Challenges
The analysis of the data involves examining: 
- Outomes Based on Launch Date
- Outcomes Based on Goals

The challenges involved with the data set involve:
- Data scrubbing
- Accounting for outliers

### Analysis of Outcomes Based on Launch Date
![image_name](https://github.com/Mugunthan24/kickstarter-analysis/blob/main/resources/Outcomes%20Based%20on%20Launch%20Date.png)
![image_name](https://github.com/Mugunthan24/kickstarter-analysis/blob/main/resources/Theater_Outcomes_vs_Launch.png)

The first graph shows the outcome based on launch date for each month for all campaigns while the second shows the same information but specific to Theater. Both graphs have a similiar pattern where: 
- the highest number of successful campaigns are in May and June
- the lowest number of successul campaigns began in December

In the graph showing overall results January, June, July, and October appear to have the highest number of failed campaigns.
In the graph specific to theater May, June, July, August, and October appear to have the highest number of failed campaigns.
### Analysis of Outcomes Based on Goals
![image_name](https://github.com/Mugunthan24/kickstarter-analysis/blob/main/resources/Outcomes_vs_Goals.png)
The graph above shows the percentage of successful, failed, and cancelled campaigns for plays based on the goal amounnt. For plays, there are no cancelled campaigns creating an inverse relationship between the percentage of successful and failed campaigns. Based on the graphs, campaigns for plays that are:
- under $5,000 have a 73% or slighly above of succeeding
- have a fund raising goal between $35,000 and $44,999 have a 67% of succeeding
- with a goal between $45,000-$49,000 have a 100% chance of failing
- greater than $50,000 have a 88% of failing
### Challenges
To begin the analysis, the data was first assessed to gain familiarity with the information in the dataset, while determining if the data needed to be modified or scrubbed. As a result, it was noted that the fields “deadline” and “launched_at” had issues since they contain Unix timestamps, which measure time as the number of seconds since midnight of January 1, 1970. This presented a challenge because in order to assess trends across time the data needed to be in a date format that accounted for day, month, and year. To resolve the problem, the unix seconds was converted to days by dividing the seconds by 60 to get minutes, then dividing the minutes by 60 to get hours, and finally dividing the number of hours by 24 to get days. Next, this number of days was added to the date Jan 1, 1970 to get the actual launch and deadline dates. Additionally, the data presently has goal amounts that are outliers, and these amounts could have been entered incorrectly. If these amounts are entered incorrectly then we should try our best to learn the actual values, and if we cannot then we can remove the outliers. However, if the outlier values are correct, then we should keep the data because it will give us a more accurate story. Other potential issues would be numeric values appearing as text in the spreadsheet. The data type would have to be changed to numeric or a data type showing monetary value (currency, accounting) using the data type dropdown menu in the Home ribbon.
## Results
The results will go over conclusions for Theater Outcomes by Launch Date, Outcomes Based on Goals, limitations of this dataset, and potential tables and graphs that can be give us a better idea of the story hidden within the data.
### Theater Outcomes by Launch Date
Conclusions that can be gathered for Theater Outcomes by Launch Date are that:
- launching campaigns in May or June are more likely to be successful
- launching campaigns in December should be avoided
There may be a seasonal connection where campaigns are more likely to succeed during warmer months and less likely to succeed during colder months. 
### Outcomes Based on Goals
Conclusions that can be gathered from Outcomes Based on Goals is that the lower the fundraising goal, the more likely the campaign is to succeed. 
### Limitations of Dataset
Some limitations of the dataset are:
- There are outliers that we cannot say for certain were entered incorrectly so it may not be a good idea to remove them
- the data is representative of a sample and not a population. The sample may not be representative
- the original data set needed scrubbed (Unix Time Stamps converted to dates)
- New columns needed to be created using existing data (Years, Parent Category, Subcategory, etc.)
### Potential Tables and Graphs
Some potential tables and graphs that could have been used are:
- showing the relationship between number of backers and campaign outcomes
- showing the relationship between the year the campaign was launched and campaign outcome
- showing the relationship between the month the campaign was launched at the outcome specifically for plays
