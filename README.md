# kickstarter-analysis

**Overview of the Project**

The purpose of the analysis is to help Louise understand how different crowdfunding campaigns have fared in relationship to their launch dates and their funding goals, to help compare to what her progress is in funding her play *Fever*. In order to achieve this will conduct technical analysis on a datase we have from Kickstarter.

**Analysis and Challenges**

*Analysis #1*

First we looked at crowdfunding results based on launch date. We bucketed the data by month based on launch dates, to then create a summary of how many projects have been succesful , failed and canceled by month. In order to make the analysis more relevant to Louise we then focused mainly on Theater projects by filtering this summary by that Parent Category. For this summary we mainly used a pivot table. Finally we created a line graph to visualize the analysis and draw conclusions. 

![First Graph](https://github.com/lladosvi/kickstarter-analysis/blob/main/Theater_Outcomes_vs_Launch.png)

*Analysis #2*

Secondly we looked at the the crowdfunding results based on the size of the goal. We bucketed the projects by goal dollar amount creating ranges every $5,000, to then create a summary of how many projects have been succesful , failed and canceled by each bucket. In order to make the analysis more relevant to Louise we focused mainly on the plays project subcategory. For this summary the main function we used was countif (example:=COUNTIFS(Data!$D:$D,"<1000",Data!$F:$F,"successful",Data!$R:$R,"plays")). Finally we created a line graph to visualize the analysis and draw conclusions. 

![Second Graph](https://github.com/lladosvi/kickstarter-analysis/blob/main/Outcomes_vs_Goals.png)

*Challenges*

One of the main difficulties we found in this analysis was with the use of COUNTIFS and testing for errors. When we started the 3rd column with the results for canceled projects, we got 0 for the first bucket and then 0 for any other bucket. It seemed strange, we were not sure if that was the and error in the formula or what was not working. So to validate if all these 0s were valid or something was wrong we went back to data and filtered by plays and then by canceled to find out there were no datapoints or intersections to be found under this criteria. Sp this way we validated the formulas were working properly and 0s were the real outcome. Otherwise the process to get to both graphs was very straightforward.

**Results**

*Analysis #1 - Conclusion #1*

When looking at the graph is easy to identify the peak in the year for succesful projects for the theater category with May being the largest count and June being the second largest. But when looking in more detail those months also seem to be peaks for the failed counts and thus the total number of projects. So before jumping into quick conclusions we realized is worth digging deeper and adding a % of succesfull projects to the summary table (see updated table below). When doing this we now can conclude that may and june are not only the 2 best months based on count of succesful projects but also based on percent of succesfull projetcs. May is the higherst at 67% and June follows at 65% with the average of the year being at 61%. So this is good information for Louis to know if at this point she can manage the launch date, those months are the best two based on the analysis we have done with success ratios starting to decline earlier or later in the year.

![image](https://user-images.githubusercontent.com/96096924/146431954-3a4e8ae5-cf34-4509-bcd1-f9b0452d2d64.png)

*Analysis #1 - Conclusion #2*

The next thing we want to look at to help Louis is the opposite of the above is what monhts she should be trying to avoid even if she cannot launch in may and june. To draw this conclusion we are going to look again to the graph and the summary table above. For this we can approach it from 2 diffrent angles, first and the more simplistic is to look at the chart and based on absolute succesful counts and on a high level looking at peaks and valleys in the graph you want generally avoid before april and after august, so in other words heading into and in the summer is probably the best shot. To draw more precise conclusions we want to look at the summary table and look at what months are below average for % of succesful projects. In doind that I would say avoid January, August, October and December. 

*Analysis #2 - Conclusion #1*

Now we are look at drawing conclusions on success factor associated with the size of the goal. I think we can do this looking both at the 2nd graph and the table used to create this graph, and to keep it simple will look at success % as looking at failures is exactly the inverse. Again will look at peak and valleys and I would say there are 2 clearly marked peaks. First anything under $5,000 seem to have the highest succes rates between 73 and 76%, so in other words the smaller the projects the easier to reach funding goals. Second peak and a bit lower is between $35,000 and $45,000 at 67% but the number of data points in this range is only 9 out of a sample fo more than 1,000. So bottom line my advice and conclusion for Louis would be that the smaller the goal the higher the chances of succeding. 

*Summary of Limitations*



*Further Analysis Recommendations*
