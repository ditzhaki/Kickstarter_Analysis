# An Analysis of Kickstarter Campaigns

## Overview
Louise, an up-and-coming playright, started a crowdfunding campaign to help fund her play _Fever_. This being her first crowdfunding campaign, Louise felt hesitant and seeked assistance in order to gain a better understanding of campaigns from start to finish. Using Kickstarter data to analyze trends and patterns, we gave Louise helpful recommendations that allowed her play to come close to its fundraising goal in a short amount of time. Now, we will dive into how different campaigns fared in relation to their launch dates and their funding goals. 

## Analysis and Challenges

[Kickstarter_Challenge.xlsx](https://github.com/ditzhaki/Kickstarter_Analysis/files/8501914/Kickstarter_Challenge.xlsx)

### Theater Outcomes Based on Launch Date
The purpose of this analysis is to obtain an understanding of the relationship between the outcomes of theater campaigns and their launch date. To help us further analyze the outcomes of the different campaigns, we first needed to sort the data by separating the Parent Category from the Subcategory. Then, we needed to convert the dates of the campaign's creation and extract the year from those dates. Organizing this information into individual columns allowed us to create a pivot table that filtered the campaigns by the **Parent Category** and **Year**, contained rows with the **Date Created**, and contained columns listing the number of **Outcomes** (Successful, Failed, and Canceled). Once the Pivot Table was constructed, we were able to filter the **Parent Category** to hone in on our dataset and reflect only Theater campaigns. 

![Screen Shot 2022-04-17 at 1 32 14 PM](https://user-images.githubusercontent.com/101564349/163725852-467fb80e-651d-4fa2-bb13-94b175fad667.png)

In order to visualize campaign outcomes based on the launch date, a line chart was created using the data in our pivot table. This visual representation depicts the relationship between the outcomes of each theater campaign and the month it launched. 

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/101564349/163720874-6c323f9b-2a89-4e15-8fcf-a0269555b390.png)

### Outcomes Based on Goals
The purpose of the next analysis is to obtain an understanding of the outcomes of theater campaigns based on their funding Goal. To help us analyze this relationship, we needed to organize and extract specific data into a new table. The funding goals were divvied up into 12 categories ranging from $0 to over $50,000. The key factors for this analysis were the Number of Successful Campaigns, the Number of Failed Campaigns, and the Number of Canceled Campaigns for each respective range of funding goals. These values were extracted from the Kickstarter Dataset through the use of the COUNTIFS() function and placed into columns. Using these values, the Total Number of Projects was obtained through the use of the SUM() function. Lastly, the Percentage of Successful, Failed, and Canceled Campaigns was calculated. 

![Screen Shot 2022-04-17 at 1 41 03 PM](https://user-images.githubusercontent.com/101564349/163726087-381d383b-d5e4-47cc-b8c9-a60c0ba6ab9a.png)

In order to visualize campaign outcomes based on the set goal, a line chart was created using the data in our newly constructed table. This visual representation depicts the relationship between the outcomes of each theater campaign and its goal. 

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/101564349/163720929-183f8b99-5484-4c63-a21f-2ccd3c1f2813.png)

### Challenges and Difficulties Encountered
A challenge I encountered during this analysis was looking at the raw dataset and coming up with information that needed to be extracted/sorted in order to uncover the trends and patterns we wanted to see. I feel that it's easy to get overwhelmed by all of the information in a dataset, as it is rare for it to be presented in the exact way you need it. However, I found it to be helpful to take the time to map out what it was that I was looking for by stating the goal of my analysis and backtracking until I uncovered the data needed. I also feel that constructing a Pivot Table can be a bit of a similar difficulty. It can be challenging to organize the data into the proper fields to yield the results we need. 

## Results

### Conclusion - Outcomes Based on Launch Date
Based on the analysis above, it can be concluded that the number of succssful theater campaigns was the highest in May, facing a steady decline in the months following. The total number of successful campaigns in May was 111 with approximately half that amount in failed campaigns. Because of these results, it is recommended that the launch date for a new campaign aim to be around May or June.

The data also reflects that the number of successful theater campaigns was the lowest in December. Specifically, the ratio of successful to failed campaigns was almost 1:1, giving us the notion to conclude that it is the riskiest month to launch a campaign.

### Conclusion - Outcomes Based on Goals
Based on the analysis above, it can be concluded that the number of successful theater campaigns was the highest when a goal of less than $5000 was set. For both goal ranges, the percentage of successful campaigns was between 76% and 73%. However, as the goal ranges increased the percentage of successful campaigns steadily declined for the most part.

### Limitations of this Dataset
With this dataset comes limitations. Because this dataset only contains datapoints for 4,113 campaigns, we only really get to see a sample size. Specifically for theater, the dataset contains only 1,393 **theater** campaigns. It would be useful to have a larger dataset for higher accuracy. 

There are also limitations when it comes to the type of data recorded within this dataset. There are other key factors that we could analyze for each campaign such as the duration of the campaign and the genre (whether it be horror, drama, romance, etc.). This could reveal other relationships that impact the outcome of a theater campaign. 

### Other Possible Tables / Graphs
Other possible tables and/or graphs that could be useful for future analysis are:

* Amount Pledged vs. Amount of Goal for Successful Campaigns
* Amount Pledged vs. Amount of Goal for Unsuccessful Campaigns

This could tell us whether a relationship lies in campaigns being more successful if they met their funding goal.

* Outcomes based on Location

This could tell us whether Louise would be more successful launching her campaign in a different country.
