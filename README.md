# Kickstarting Analysis

## Compare Kickstarting Campaigns Based on Launch Dates & Funding Goals

The purpose of this analysis is to determine if kickstarting campaign outcomes could be predicted based on their launch dates and / or fundraising goals.

## Analysis and Challenges: 

### Analysis of Outcomes Based on Launch Date: 

I completed the analysis by looking at the outcomes of campaigns based on launch dates, specifically which month the campaign was started in. I looked at only kickstarters with the Parent Category of "theater". To do this I created a new column called “Years” and used the formula =Year(startdate). Then I created a pivot table with Parent Category and Years as the filters, StartDate as the rows and Outcomes as the columns. I filtered out the “Live” outcomes and removed “Quarters” from the StartDate rows so that just months were listed. I then created a line chart based on this pivot table.

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/95837693/147700375-65a1d73d-0ee7-4305-8c50-7d9c62c540b3.png)

By looking at the chart "Theater Outcomes Based on Launch Date" we can see that May has the most successful kickstarter campaigns, but May also has the most total campaigns. I then looked at the percentage of successful campaigns for each month to see that 67% of May's campaigns were successful. Overall, 61% of theater campaigns were successful, so May campaigns had a 6-point advantage over the total average. From the data I can see that the least successful kickoff months were December (49%), October (57%), and January (58%).   

### Analysis of Outcomes Based on Goals: 

I looked at outcomes based on Funding Goal ranges for the subcategory “plays”. To do this I created a table with the specified funding goal ranges as rows labels and the column headings of “Successful”, “Failed”, and “Canceled”. I used Countifs formulas to count the campaigns that fit the row and column specifications and were of the subcategory “plays”. For example, = COUNTIFS(Kickstarter!$F:$F, "successful",  Kickstarter!$D:$D, "<1000", Kickstarter!$R:$R, "plays") counted all the campaigns that were “successful”, had a fundraising goal of less than $1,000, and had the subcategory of “plays”.

To calculate the percentage columns, I first totaled the “successful”, “failed”, and “canceled” columns into a “Total Projects” column. Then I created a formula with “successful” over “Total Projects” for the “Percentage Successful” and the same for “failed” and “canceled”. I created a line chart based on the percentage columns.

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/95837693/147700404-33b199cb-05f6-4e52-afa3-f331ccc54cc4.png)

Comparing the percentage successful for the different goal ranges, I can see those campaigns with goals less than $5,000 and those with goals ranging from $35,000 up to $45,000 were the most successful. Plays with goals greater than $45,000 were the least likely to be successful.

### Challenges and Difficulties Encountered: 

Creating the Outcomes Based on Launch Date pivot table was interesting to see how Excel automatically handles the dates and creates quarters. Deleting out the Quarters brought up the list of Months, but I didn't understand why we needed the "Years" column until I tried to create the pivot table without that column and realized then that I couldn't get to months without the "Years" column. 

I encountered challenges with the Countifs for the Funding Goals analysis as I hadn’t used that formula before and the format of the formula wasn't like something I'd seen before. The "Help" in Excel actually helped me understand the sintax of that formula. Once I understood the formula layout, I was able to get the counts. Another challenge in the Outcomes based on Goals table was that some of the ranges had small numbers for their total projects and I don’t think those results are reliable.

## Results

Based on launch date, if I were recommending a month to launch a kickstarter it would be May. I would also recommend avoiding December as a launch month, as those campaigns were least successful.

Based on goals, the campaigns of less than $5,000 had the highest success rates. I would not recommend campaigns of more than $45,000 as they had very low success rates. 

Limitations in the dataset are that when looking at plays, most campaigns had goals of less than $10,000, so looking at campaigns with goals of more than that might not give us reliable results. 

We could also look at the data in terms of outcomes in relation to how long the campaigns lasted, how many contributors took part in the campaigns, and look at the data based on the country the campaigns took place in. 
