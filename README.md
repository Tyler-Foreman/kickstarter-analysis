# Overview of Project
This intent of this project is to perform an analysis on historical Kickstarter data to uncover trends for an upcoming theater project campaign that Louise is working on. We are looking to gather insights for Louise on specific factors that make a project campaign successful, so that Louise can mirror her campaign to other successful campaigns on Kickstarter.

# Kickstarter Analysis

To perform our analysis for Louise's kickstarter campaign I created many different worksheets to best understand all of the data to be able to make a firm recommendation for Louise. The raw data provided was substantial, however there was more data needed to perform a proper analysis. Since Louise is looking to create a campaign for her upcoming theater play, Fever, I needed to break out the category and subcategory fields to be able to parse out the musical and spaces subcategories that fell under the theater category. I also needed to convert the unix timestamp data to properly understand when each campaign was created and ended - to be able to understand how long each campaign was. I also created a year column from the campaign creation date to be used for additional filtering.

Now with all the data fields that I would need to perform my analysis, I began creating several pivot tables and charts to put together my recommendation for Louise.

## US Theater - Category Analysis 

I first created a new worksheet to hold a pivot table and chart, to filter by all parent categories. I was looking to see how all the parent category campaigns compared against one another in a quick view to see the count of successful, failed, live, and cancelled campaigns.

We can see that theater is the most common Kickstarter campaign category by several hundred campaigns . By reviewing the chart below, you will see that there are over 900 theater campaigns that have been started on Kickstarter in the US, with over half of them being successful. The next closest parent category campaign starterd in the US on Kickstarter was the music category with just over 600 campaigns.

![Parent Category Outcomes](/Parent%20Category%20Outcomes%20-%20Stacked%20Column%20Chart.png "Kickstarter Parent Category Outcomes")

## US Theater/Play - Subcategory Analysis

While it is important to know how many theater campaigns have been started in the US on Kickstarter, Kickstarter does classify 3 subcategories under the parent category for theater. Since Louise is looking to create a Kickstarter campaign for her upcoming theater play - I looked to narrow this data even further. I created a new worksheet for a new pivot table and chart that housed subcategory statistics to be able to narrow my search for theater/play campaigns in the US. I was able to find out that most of the campaigns in the US for the parent category theater, are in fact campaigns for plays. Based on the chart below, you will see that 

![Theater Play Campaigns in the US](/Theater_Play_Campaigns_US.png "Theater/Play Campaigns in the US")

## US Theater/Play - Campaign Based on Launch Date Analysis

The next step in my analysis was to best understand when these theater/play campaigns were created. Since I had convereted the Unix timestamp to the creation date of each campaign, I created a new pivot table and chart in which I was able to filter down to this category and subcategory by year. The following line graph below represents the theater/play outcomes based on launch date for each month (over all years).

![Theater/Play Campaigns Based on Launch Date](/Theater_Plays_Subcategory_Outcomes_US.png "Theater/Play Campaigns Based on Launch Date")

As we take a look further into the theater/play Kickstarter campaign outcomes based on launch date, we can see from the graph above that theater campaigns are extremely successful in the month of May through July. The remaining months do have successful campaigns as well, but there is clear evidence that these months underperform the late spring and early summer months.

## US Theater/Play - Goal Analysis

Now that I had a recommendation for Louise on when she should kick off her theater/play campaign for Fever, I needed to perform an analysis to provide her a recommendation on how much money her campaign goal should be to be a successful campaign. I filtered the data set down to just US and created a box and whisker plot using the goal and pledged columns in the data set, as seen below.

![US Plays Box Plot](/US%20-%20Plays%20Box%20Plot.png "US Plays Box Plot")

### US Theater/Play - Successful Goal Median

I then took the above data and narrowed it further to filter the raw data set by only successful theater/play campaigns. I saw the amount pledged for successful theater/play campaigns received $5,000 or less for 75% of the successful campaigns - as seen in the successful US plays graph below. We can also see the median goal for a Kickstarter campaign is $3,000.  

![Successful_US_Plays_Based_On_Goals](/Successful_US_Plays_Based_On_Goals.png "Successful US Plays Based On Goals")

### US Theater/Play - Failed Goal Median

After obtaining an understanding of successful theater/play campaign goals, I went back to the raw data set to adjust this to view failed theater campaigns. I felt this information would be helpful to obtain an understanding of what goals these failed campaigns were aiming for, so that we could properly advise Louise on a proper goal range that will provide her with the best success. As seen in the failed US plays graph below, we see that the median goal is $5,000 and that 75% of the failed plays had a goal of $10,000 or less.

![Failed_US_Plays_Based_On_Goals](/Failed_US_Plays_Based_On_Goals.png "Failed US Plays Based On Goals")

### US Theater/Play - Overall Outcomes Based on Goals

This information was helpful to gather, however it would also be best to understand how successful all of these campaigns were based on their goal. I created a new worksheet in which I built out a table that defines a series of goal ranges, calculating the number of successful/failed/cancelled theater/play campaigns. With this data properly calculated in my new worksheet, I performed a statistical analysis of the percentage of success/failed/cancelled within each goal range. From there I then illustrated this using a line chart, with the x-axis showing the specific goal ranges and the y-axis showing the percentage metrics as seen below.

![Theater/Play Outcomes Based on Goals](/Resources/Outcomes_vs_Goals.png "Theater/Play Outcomes Based on Goals")

# Final Recommendation

Based on my review and analysis of the kickstarter data provided, Louise should start her theater/play kickstarter campaign in the US in the month of May. May has been the most successful month for these campaigns historically per our review of the campaign based on launch date analysis.

Since Louise's upcoming project is to for a play in the US, it is my recommendation to aim for a goal of $3,000 - $4,000 for the campaign. The data does show there are campaigns with goals higher than this that have been successful, however these are outliers in the overall data set and the median goal of a successful campaign is $3,000 as where the median of failed campaigns is $5,000. As we see in the 'Outcomes Based on Goal' graphic above the success of a campaign goal between $1,000 - $4,999 is near 80% and precipitously drops below 60% when the campaign goal is $5,000 - $9,999.

## Challenges

I did not have any challenges in putting together my analysis for the kickstarter campaign. One of the main challenges I would see users encountering with this raw data set is in properly converting the launched_at and converted columns, to be able to produce a proper mm/dd/yyyy format. I would anticipate users complete the mathematical conversion fine, however that then left a numerical number. If a user did not properly update the format of this column to 'short date' the data would be relatively useless for them in their analysis.

# Results

Below are the final results question answers.

## Two conclusions made about the Theater Outcomes by Launch Date

- In review of the 'Theater Outcomes by Launch Date' pivot chart, it is clear that the best month to create for theater Kickstarter campaigns are during the months of May - July.
- The second conclusion that is made from this pivot chart is that the winter months are not a great time to start a theater campaign on Kickstarter. In the month of December, there was effectively a one-to-one relationship of successful and failed theater campaigns.

## Conclusion about Outcomes based on Goals
- In review of the data created by goal range that shows the success/failure of play campaigns based on their goal, it is clear that the most successful campaigns are those with goals under $5,000. There is a negative correlation between the success of a campaign and the target goal of that campaign that is shown in the chart. There is also some misleading information seen in this data for campaigns ranging from $35,000 - $45,000. It appears these campaigns are more successful, however there is not enough of a substantial data set to properly determine this as a valid trend.

## Limitations of the data set
- Since we are defining goals in the raw data set across different world currencies (ie: USD/GBP/EURO) there is no current conversion of this currency that would allow us to properly calculate the outcomes based on goal. Currently we are taking data for plays based on goal value, however $3,000 GBP is approximately $4,000 USD - so this does not leave us with a proper data set to perform these calculations.

## Other tables and graphs
- To properly come up with a recommendation for Louise for her US play, we should come up with a table that properly converts all goal and pledge amounts based on their currency and perform a calculation to USD. This would then provide us with consistent goal/pledged monetary values to perform a better analysis on successful campagains based on their goal.

