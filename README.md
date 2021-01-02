# kickstarter-analysis

# Analysis Report on Kickstarter Campaign 

## Overview and Purpose of Project:

	Projecting the success rate of Louise`s play Fever in Crowdfunding campaign based on launch dates and funding goals with the help of Kickstarter data. 


## Analysis and Challenges:

### Analysis of Outcomes Based on Launch Date:
	1. I have created pivot table by selecting the Kickstarter data and insert tab.

	2. In the Pivot table Fields column and rows are filled with outcomes and Launched dates as the analysis is based on them. The values are filled based on  count of outcomes in order  to see the success count. Theater can be seen after Parent category is placed in filters and also Years to know is also placed in filters to understand which years success rate is high.

	3. In order to get better understanding of the filtered data, Chart was created by selecting pivot table, then Analysis tab is used followed by Line and Mark chart.


### Challenges for Outcomes by Launch Date Analysis:

	1. Sorting columns labels column wise for successful, failed and canceled columns
	2. Confused between years column and the automatically created years column when Date Created Conversion column was placed in Row field of pivot table field.

### Analysis of Outcomes Based on Goals:
	1. Columns are filled using countifs(), sum() and round functions

	Codes :
	
	Number Successful:
	=COUNTIFS(Kickstarter!$D:$D,"<1000",Kickstarter!$F:$F, "successful",Kickstarter!$R:$R,"plays")
	Number failed:
	=COUNTIFS(Kickstarter!$D:$D,">=20000",Kickstarter!$D:$D,"<25000",Kickstarter!$F:$F, "failed",Kickstarter!$R:$R,"plays")
	Number cancelled:
	=COUNTIFS(Kickstarter!$D:$D,">=50000",Kickstarter!$F:$F, "canceled",Kickstarter!$R:$R,"plays")
	
	Total Projects:
	=SUM(B3:D3)
	
	Percentage successful:
	=ROUND((B7/E7),2)

	2. Percentage format id changed by number option of Home tab

	3. In order to get better understanding of the calculated data. Chart was created by selecting required data, then insert tab and Line chart.
	
### Challenges for Outcomes Based on Goals Analysis :
	1. Confused while calculating different ranges in Countifs() functions 
	2. Learnt how to apply same formula to different cells
	
## Results:
### Conclusions based on Launch Date:
	1. Outlier is in February.
	2. Success rate is mostly seen in the months of May and June. In the recent years from 2014 -2016 these months are highly successful. 
	3. Thus, for Louise to reach her target she should invest in May or June 

### Conclusions based on Goals:
	1. Outliers are from 35,000 to 44,999$
	2. If the budget of the play is less i.e. lower than 15,000 to 19,999$ then the success percentage is equal to or more than half. 
	3. Therefore, Louise might succeed as her budget is 12,000$

### Limitation of Kickstarter data set:
	1. Details of genres of plays like comedy, tragedy, Horror etc.,
	2. Details of age of people who gave the donations so as to find which age group liked which kind of play.
	3. Regions where the fund raising campaign are held in a given country
	
### Other possible tables and/or graphs that we could create:
	1. Tables and Graphs are possible based on backers count and percentage funded
