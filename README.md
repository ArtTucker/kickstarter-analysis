# A Focused Analysis of Theater-based Kickstarter Campaigns

## Overview and Purpose of Project

This project focused on performing analysis on Kickstarter data to uncover trends in theater-based crowdfunding campaigns. The requester was "Louise," someone who was considering starting her own crowdfunding campaign to support a play they were producing. The primary tool used was Microsoft Excel. The source data was a table of 4114 campaigns from 2010 through 2017, sourced with a bias towards theater campaigns, but sampling from a range of other categories as well. The methods used included pivot tables, break-out tables of subsets of data, charts of various criteria, and various statistical formulas.

## Analysis and Challenges

The majority of the analysis conducted in this exercise was performed through pivot tables and graphs based on those tables. 

![Parent Category Stats Pivot Table](resources/cat_stats_pivot01.png)

Pivot tables, while being a wonderfully powerful tool, can be a bit of a challenge to get used to. In setting up the criteria, it can be confusing to know which value you want to set as columns, rows, filters, and values. Sometimes it is necessary to stumble through settings until the table shows you the information you're looking for in a way that makes logical sense.

![Outcomes Based on Goals table](resources/outcomes_goals01.png)

Our table for 'Outcomes Based on Goals' was built from formula -- mostly `COUNTIFS()` plus some simple arithmetic. The great hazard here is formatting and paying attention to detail. When you've got cell after cell that reads:
`=COUNTIFS(Kickstarter!D:D,">=1000",Kickstarter!D:D,"<5000",Kickstarter!F:F,"Successful",Kickstarter!R:R,"plays")`
... then the next cell reads:
`=COUNTIFS(Kickstarter!D:D,">=5000",Kickstarter!D:D,"<10000",Kickstarter!F:F,"Successful",Kickstarter!R:R,"plays")`
... you have to make sure you change the right variable, and only the right variable. Sometimes clicking and dragging works to help you fill out more cells more efficiently. And sometimes you have to make judicious and careful use of the Find-and-Replace tool.

## Know your chances (Parent Category and Subcategory Stats)

![Category Outcomes](images/cat_outcomes.png)
In the first tab of the workbook, after the raw/starting data tab, we begin to make some observations. We begin by looking at success and failure rates of the crowdfunding data we were presented with. We can see from the chart, that out of over 900 US-based theater-related Kickstarter campaigns, over half were successfully funded, with just over one-third failures (did not meet fundraising goals).

![Theater Subcategory Outcomes](images/theater_subcat_outcomes.png)
In the next worksheet tab we narrow down our analysis to more specifically what "Louise" is interested in. We can see that out of the 671 campaigns for plays, over 60% were successful, also with roughly one-third failures.

What this shows is that overall odds are good for the success of theater-related Kickstarter projects, though they are not guaranteed. There is still a non-negligible risk of failure. That said, let's look at another factor that could contribute to the success of a crowdfunding campaign.

## The Right Timing (Analysis of Outcomes Based on Launch Date)

![Theater Campaigns Outcomes Based On Launch-date](images/launchdate_theater_outcomes.png)
The above chart shows the number of theater-related Kickstarter campaigns, differentiated by outcome, charted by the month in which they were launched. It is fairly apparent from a quick glance, that most successful campaigns are launched in May or June. It is also apparent that the highest likelihood of failure occurs with campaigns launched in December or January. The safe assumption is that a large number of Kickstarter's customer-base/audience are probably focused at that time of year on saving their money for holiday shopping or end-of-the-year expenses.

## Realistic Goals and Expectations (Analysis of Outcomes Based on Goals)

![Outcomes Based on Goals](resources/Outcomes_vs_Goals.png)
One of the last keys to success we can observe through our data is how setting the right goal for our campaign is important to the success of the campaign. The chart above shows that campaigns with lower-range goals (under $20,000) had a higher chance of succeeding than of failing. At goals of $20,000 and above campaigns were more likely to fail. There is a small island of success between play campaign goals of $35,000 and $45,000, but keep in mind that the chart only shows percentages, and the actual sample size at that range is just 9 campaigns.

## Results

After all this work, what have we learned about setting a Kickstarter campaign on the right track for success?
* The odds are historically in your favor. Using the starting data presented, more campaigns are successful than fail.
* Campaigns launched in May or June tend to be the most successful, while campaigns launched in December have almost as much of a chance at failing than succeeding.
* Campaigns for plays launched with moderate goals - under $20,000 - have the most chance for success.

So, do we now have all the tools necessary to create our own phenomenal, blockbuster theater-related Kickstarter campaign? Not really. There are a variety of limitations inherent in this analysis. First and foremost, the dataset we started with was exceptionally limited and dated. It was a sampling of only just over 4000 campaigns, dating from 2009 to 2017. Secondly, since the sample was incomplete and seemed heavily biased towards theater-based projects, we also can't be sure that it wasn't also heavily biased towards ***successes***, ***successful campaigns that launched in the middle of the year***, or ***Successful campaigns with goals under $20,000***. Additionally, this form of analysis tells us nothing of the effect of marketing or additional milestone goals on the success of a campaign. Lastly, while Excel is a great tool, it would be easily overwhelmed by datasets of 


- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?


