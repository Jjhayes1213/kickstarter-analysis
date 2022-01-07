# Kickstarting with Excel

## Overview of Project
    This project was an exercise on how to help a client better understand their data by executing visual formatting and graphs.  By reformatting the data with colors, graphs and specific tables; categories can be quickly viewed and assessed.  Rather than a large datbase of information, the client can use this analysis and the data snapshots for personal use or share the collected data easily with others.
### Purpose
    The datset provided was large and it wasn't clear or easy to identify the success or failures of the compaigns.  The data included active, sucessful, failed and cancelled kickstarter projects. Adding tables and formatting the data so the successes and failures could be viewed and compared.  Adding the graphs in addition to the formatting really helps the client understand the data and allows for effective comparisons of the campaign results. 
## Analysis and Challenges
    The data at times was difficult to anlyze for best results due to having so many unnessessary columns.  Pulling out the key data to release the vital findings on this project was ideal.
### Analysis of Outcomes Based on Launch Date
    Starting off, data was pulled out to filter only the results of the "theater" campaigns.  Through a pivot table the date range was set by "months" and the row labels and the columns were filtered to show the results of the "Successful", "failed", and "canceled" campaigns. Overall only 37 theater campaigns were canceled.  The graph clearly identifies May and June as the highest success months for these campaigns.  
### Analysis of Outcomes Based on Goals
    This data was pulled to run a comparison of the "plays" campaigns.  The data was pulled to review the number of "successful", "failed", and "canceled" projects.  This chart was broken down to the count of the campaigns results based on the outcomes in goal ranges.  That is, the goal amount to be raised for each campaign and the success or failure if the campaign based on the goal amount sarting at less that $1000 and in category grouping of about $5000 all the way up to greater than $50000.  Incredibly we found that none of the play campaigns had been canceled.  However, success of the campaigns decreased dramatically for goals that were greater than $20000.  Overall failures also decreased greatly for campaigns over $20000.  Counts for campaigns over $20000 were low overall, however the graph clearly shows how the failures were much greater for the higher goals.  Additionally the Percentage totals for each campaign result was calculated, which ultimately was the data used in the graph for the comparrison of the Percentage: successful, failed and canceled outcomes.
### Challenges and Difficulties Encountered
    With the "Outcomes based on Launch Date" analysis, we had to convert the data in column "I" which was the "deadline", and column "J" which was titled "launched".  At first the series of numbers was not reconizable as a date range, so data was pulled from cell "I" and placed into the epoch & unix timestamp converter. This step was followed again with corresponding data in cell "J".  The converter proved this date to be a date range.
https://www.epochconverter.com/
    Next an equation was entered to convert the data for column's "I" and "J" and save this data into columns "S" and "T" respectively.
=(((J30/60)/60)/24)+DATE(1970,1,1)
    It is challenging when you recive data that you can not understand.  Folowing these steps, led to a better comparison of the data.
    With the "Outcomes based on Launch Date" analysis, the Countif formula had to be rewritten multiple times.  As I was doing my spot checks of the data, my counts were off.  However, the equation proved to be beneficial once it was re-written correctly.
=COUNTIFS(Kickstarter!$F:$F,"successful",Kickstarter!$D:$D,">=5000",Kickstarter!$D:$D,"<=9999",Kickstarter!$R:$R,"plays")
## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
    1) Overall the "theater" campaigns have been very successful.  However due to the high failure rate of campaigns in July through December, they may want to reduce the amount of campaigns in those months, and increase the campaigns in months of January through June.
    2)Though success rate high, having more than half as many failed "theater" campaigns is concerning.  In the months of May and June their success is about double the results of most months.  The team should review what is done in those months and replicate it for higher success rates in other months.
- What can you conclude about the Outcomes based on Goals?
    1)Overall the outcomes for the "plays" campaigns is much higher with the lower goals for funding.  The client should consider limiting or completely eliminating projects moving forward for plays with goals over $25000, and continue to increase and focus on getting funding on projects with less than $25000 goals.
- What are some limitations of this dataset?
    This dataset included fundraising campaigns that appeared to last only 1 or 2 months.  It would be beneficial to see if the success of the higher funding campaigns would increase, if they extended the timeframe between the launch date and deadline.
- What are some other possible tables and/or graphs that we could create?
    The client would benefit from a table that shows the success on campaigns for each country.  A bar graph would likely be prefered over a pie graph, to clearly compare which country's successes and failures are the highest. Ultimately graphs and formatting allows the client see where they should add more or decrease resources such as time, money and personnel.  So seeing the success and failures in each country should help with that decision making.