# kickstarter-analysis
Performing analysis on Kickstarter data to uncover trends.
## Overview of Project
Louise, a playwright started a crowdfunding campaign and noticed that she came close to her fundraising goal in a short amount of time. Now, she would like to learn how different campaigns fared in relation to their launch dates and their funding goals.
### Purpose
The purpose of the project is to determine if launch dates and funding goals affect the outcome of a fundraising campaign.
## Analysis and Challenges
To begin the analysis, the data was first assessed to gain familiarity with the information in the dataset, while determining if the data needed to be modified or scrubbed. As a result, it was noted that the fields “deadline” and “launched_at” had issues since they contain Unix timestamps, which measure time as the number of seconds since midnight of January 1, 1970. This presented a challenge because in order to assess trends across time the data needed to be in a date format that accounted for day, month, and year. To resolve the problem, the unix seconds was converted to days by dividing the seconds by 60 to get minutes, then dividing the minutes by 60 to get hours, and finally dividing the number of hours by 24 to get days. Next, this number of days was added to the date Jan 1, 1970 to get the actual launch and deadline dates. Other potential issues would be numeric values appearing as text in the spreadsheet. The data type would have to be changed to numeric or a data type showing monetary value (currency, accounting). Additionally, the data presently has goal amounts that are outliers, and these amounts could have been entered incorrectly.
### Analysis of Outcomes Based on Launch Date
![image_name](C:\Users\mugunthan.rengarajah\OneDrive - CLEAResult Consulting Inc\Desktop\Data Analytics Bootcamp\Analysis Projects\Crowdfunding Analysis\resources\Outcomes Based on Launch Date.png)
![image_name](C:\Users\mugunthan.rengarajah\OneDrive - CLEAResult Consulting Inc\Desktop\Data Analytics Bootcamp\Analysis Projects\Crowdfunding Analysis\resources\Theater_Outcomes_vs_Launch.png)
The first graph shows the outcome based on launch date for each month for all campaigns while the second shows the same information but specific to Theater. Both graphs have a similiar pattern where: 
- the highest number of successful campaigns are in May and June
- the highest number of failed campaigns are in October
- the lowest number of successul campaigns began in December overall for all campaigns, and for those specific to theater.
### Analysis of Outcomes Based on Goals
![image_name](C:\Users\mugunthan.rengarajah\OneDrive - CLEAResult Consulting Inc\Desktop\Data Analytics Bootcamp\Analysis Projects\Crowdfunding Analysis\resources\Outcomes_vs_Goals)
The graph above shows the percentage of successful, failed, and cancelled campaigns for plays based on the goal amounnt. For plays, there are no cancelled campaigns creating an inverse relationship between the percentage of successful and failed campaigns. Based on the graphs, campaigns for plays that are:
- under $5,000 have a 73% or slighly above of succeeding
- have a fund raising goal between $35,000 and $44,999 have a 67% of succeeding
- with a goal between $45,000-$49,000 have a 100% chance of failing
- greater than $50,000 have a 88% of failing
