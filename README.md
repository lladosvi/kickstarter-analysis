# kickstarter-analysis

##Overview of the Project##

The purpose of the analysis is to help Louise understand how different crowdfunding campaigns have fared in relationship to their launch dates and their funding goals, to help compare to what her progress is in funding her play *Fever*. In order to achieve this will conduct technical analysis on a datase we have from Kickstarter.

**Analysis and Challenges**

First we looked at crowdfunding results based on launch date. We bucketed the data by month based on launch dates, to then create a summary of how many projects have been succesful , failed and canceled by month. In order to make the analysis more relevant to Louise we then focused mainly on Theater projects by filtering this summary by that Parent Category. For this summary we mainly used a pivot table. Finally we created a line graph to visualize the analysis and draw conclusions. 

![First Graph](https://github.com/lladosvi/kickstarter-analysis/blob/main/Theater_Outcomes_vs_Launch.png)

Secondly we looked at the the crowdfunding results based on the size of the goal. We bucketed the projects by goal dollar amount creating ranges every $5,000, to then create a summary of how many projects have been succesful , failed and canceled by each bucket. In order to make the analysis more relevant to Louise we focused mainly on the plays project subcategory. For this summary the main function we used was countif (example:=COUNTIFS(Data!$D:$D,"<1000",Data!$F:$F,"successful",Data!$R:$R,"plays")). Finally we created a line graph to visualize the analysis and draw conclusions. 

![Second Graph](https://github.com/lladosvi/kickstarter-analysis/blob/main/Outcomes_vs_Goals.png)

One of the main difficulties we found in this analysis was with the use of COUNTIFS and testing for errors. When we started the 3rd column with the results for canceled projects, we got 0 for the first bucket and then 0 for any other bucket. It seemed strange, we were not sure if that was the and error in the formula or what was not working. So to validate if all these 0s were valid or something was wrong we went back to data and filtered by plays and then by canceled to find out there were no datapoints or intersections to be found under this criteria. Sp this way we validated the formulas were working properly and 0s were the real outcome. Otherwise the process to get to both graphs was very straightforward.

**Results**


