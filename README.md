# Kickstarting with Excel: Kickstarter Campaign Analysis

## Overview of Project
I analyzed this dataset to uncover trends related to the Kickstarter campaign start date for Theater Categories and the respective goals for Campaigns in the Plays" Subcategory. The data set included campaigns from 2007 to 2017 and included Categories, Subcategories, Dates Launched, Pledged Amounts, Goals, and Outcomes. I organized these points throughout the analysis to determine if there were significant patterns or learnings within the historical information. 

### Purpose
The purpose of this analysis was to give Louise data-backed information about how other campaigns on the Kickstarter platform fared, specifically in the Parent and Subcategories she was interested in, so that she could potentially use to inform future campaigns. 

## Analysis and Challenges

### Summary of method
I performed the analysis by focusing on the "Theater" Parent Category. I organized data points by Outcome (successful, failed, canceled) in relation to Campaign Dates Launched via a Pivot table. I also derived total Successful, Failed, and Canceled outcomes in relation to Goal using twelve different ranges from less 1000 to greater than 50000. 

### Analysis of Outcomes Based on Launch Date

1. Theater campaigns launched in June were more successful than other months of the year despite there being more campaigns launched in June than any other month but May. 
2. Theater campaigns that launched in December were more equal in their success or failure. For all Parent Categories, campaigns were more likely Failed in December.
3. In all months, there are less failed campaigns than successful campaigns. 
4. Kickstarter campaigns launched in January were more likely than other months to be cancelled.

### Visual analysis of Outcomes Based on Launch Date

![Theater_Outcomes_vs_Launch](kickstarter-analysis/Resources/Theater_Outcomes_vs_Launch.png)


### Analysis of Outcomes Based on Goals
1. There is not much difference in success or failure between Campaigns that set goals between 5,000 to 24,999. In particular, campaigns 15000 to 19999 had an equal number of campaigns success as fail. 
2. There is a 40% greater success percentage if a campaign set a goal between 35000 to 39999 than one that in the next lower range 30000 to 34999.
3. Campaigns that asked for less than 1000 had a higher percentage of Successful Outcomes than those with higher goals. 
4. Campaigns with goals between 25000 to 29999 were much more likely to have Failed Outcome (80%)

Example of Countifs formula used to derive totals based on "Play" subcategory, Success Outcome, and Goal Range: =COUNTIFS(Kickstarter_Data!$D:$D,"<1000",Kickstarter_Data!$F:$F,"successful",Kickstarter_Data!$R:$R,"plays")

### Visual analysis of Outcomes Based on Goals

![Outcomes_vs_Goals](kickstarter-analysis/Resources/Outcomes_vs_Goals.png)


### Challenges and Difficulties Encountered

There were no major blocking challenges related to this data set. 

Minor challenges include:
- The Kickstarter tab of All Up data was filtered at the beginning of my analysis so that the Year() formula was only applied to the visual cells. To overcome this challenge I double checked that filters were off when repeating the formula. There should be no lasting effect on the result.
- There was no data for Canceled Outcomes for the Subcategory "Plays" so there are no references in comparison to Failed or Successful. This could not be overcome without changes to the dataset.
- There are conficting references to "Launch Date" when it is renamed "Date Created" after the date conversion. I believe that Column S in the Kickstarter Tab should be named "Launch Date Conversion". This is because someone may "Create" the kick-starter and not actually "Launch" it for a period of time. Otherwise, "Launch" should be defined as either configured in the Kickstarter platform OR set public. 

## Results

### Conclusions on Outcomes based on Launch Date
1. It is best to start a Kickstarter campaign for a Theater Campaign or any campaignin May or June.
2. It is likely worst to start a Kickstarter campaign in December.

### Conclusions on Outcomes based on Goals
1. Kickstarter campaigns for plays were more likely to be Successfully funded if the goal was less than 1000 or between 35000 to 44999. 
2. Kickstarter campaigns for plays that asked for more than 50000 were not likely to be fully funded. 

### Dataset limitations
1. This data set ends in 2017 and may be outdated
2. This data set is missing important points related to how the Campaign was shared and how many times the campaign page was viewed (number of times, on what platforms) to build deeper recommendations about how Louise should plan for the future. 
3. This data set had major outliers with one Campaign 22603% Funded as an example.

### Other tables or graphs to consider
1. Theater Outcomes based on Backers Count filtered by Goal amount would give insights into how many backers Louise should shoot for based on the amount asked for in the future. 
2. Theater Outcomes based on how long the campaign will run before the deadline would give Louise an idea of how long to set the Kickstarter timing.
3. Play or Theater Outcomes related to if the campaign was a Staff Pick or a Spotlight. To find out how important it is to seek these categories. 
4. The Theater Outcomes by Launch Date should also be visually broken down by year to determine if these trends have been building or declining throughout the ten year date range.
