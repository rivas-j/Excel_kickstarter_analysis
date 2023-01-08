# Kickstarter Theater Campaign Analysis with Excel

![Theater Outcomes vs Funding Goals](images/Theater_Outcomes_vs_Launch.png)

## <div align="center">Analyze Kickstarter data to help decide the next successful theater campaign</div>

<p align="center">
<a href="#goal">Goals</a> &nbsp;&bull;&nbsp;
<a href="#dataset">Dataset</a> &nbsp;&bull;&nbsp;
<a href="#tools-used">Tools Used</a> &nbsp;&bull;&nbsp;
<a href="#analysis-and-challenges">Analysis and Challenges</a> &nbsp;&bull;&nbsp;
<a href="#results">Results</a> &nbsp;&bull;&nbsp;
<a href="#summary">Summary</a>
</p>



# <div align="center">Goal</div>

The client ran a Kickstarter campaign for a play called "Fever" that almost reached its goal in a short amount of time. The aim is to look at data from all other Kickstarter Theater campaigns, then perform an analysis to identify trends amongst other Successful fundraisers. The findings will help narrow down parameters for the client's following fundraiser.


# <div align="center">Dataset</div>
Kickstarter campaign data was compiled from the years 2009-2017 in an Excel spreadsheet, then analyzed trends based on Launch Date and Funding Goals and their effect on campaign success.


- [Kickstarter Data](data/kickstarter_data.xlsx): Spreadsheet containing data for 4,114 Kickstarter campaigns, downloaded from Amazon S3 host

# <div align="center">Tools Used</div>
- **Microsoft Excel:** Spreadsheet used to analyze dataset and produce visualizations


# <div align="center">Analysis and Challenges</div>

## Analysis of Outcomes Based on Launch Date

First a pivot table was generated from the original data set using the **Outcomes** in the column portion, **Date Created** in the row portion, with the **Parent Category** and **Years** as filters, as seen in the screenshot below:

![Pivot Table - Theater Outcomes Based on Launch Date](images/Pivot_Table_Theater_Outcomes_vs_Launch.png)

The filter feature was used to focus solely on the "Theater" category, then filter the Outcomes to highlight the Successful, Failed and Canceled campaigns.

Using that filtered pivot table, a line chart was generated to visualize the relationship between launch dates and the count of Successful, Failed and Canceled Theater Kickstarter campaigns:

![Chart - Theater Outcomes Based on Launch Date](images/Theater_Outcomes_vs_Launch.png)

## Analysis of Outcomes Based on Goals

A simple table was created to analyze the campaign funding goals. Funding tiers were determined to summarize the count of Successful, Failed and Canceled Play campaigns. Please see the completed table in the table below:

![Table - Play Outcomes vs Goals](images/Table_Outcomes_vs_Goals.png)

COUNTIFS formulas were used, such as the quoted one below, to calculate the count of Successful plays within each goal tier outlined in the table.

> =COUNTIFS(Kickstarter!$F:$F,"successful",Kickstarter!$D:$D,"<1000",Kickstarter!$R:$R,"plays")

A percentage of each outcome was calculated in order to generate the line chart below:

![Chart - Play Outcomes vs Goals](images/Outcomes_vs_Goals.png)

This line chart used the Goal column along the X-Axis, and Percentage of Outcomes along the Y-Axis. A legend was included that depicted colored lines that corresponded to the Percentage of Successful, Failed and Canceled plays based on the Goal amount.

## Challenges and Difficulties Encountered
- The dates in the initial data set were in UNIX format, which is very difficult for customers and analysts to read. It also made it harder to organize pivot tables and charts. Excel formulas were used to convert the UNIX dates to a more readable Day/Month/Year format.
- Originally, the **Parent Category** and **Subcategory** data of each Kickstarter campaign were in the same column. Excel's text to columns feature was used to split this data into two separate columns respectively titled "Parent Category" and "Subcategory". This allowed separate analyses to be performed for the **Theater** category and the **Plays** subcategory.
- Upon generating the line chart for the Play Outcomes vs Goals table, there was a lot of noise. Since the entire table was highlighted to generate the chart, the formatting of the chart was adjusted using filter feature. Columns from the original table that were meant to be excluded were deselected. Here is a screenshot of how this was accomplished:

![Formatting Chart - Play Outcomes vs Goals](images/Formatting-Outcomes_Based_on_Goals.png)

# <div align="center">Results</div>

## Theater Outcomes Based on Launch Date
- Based on the above chart titled **Theater Outcomes by Launch Date**, the month of May yielded the most Successful Theater campaigns. The months of May through August, and October also yielded the highest number of failed Theater campaigns. Our conclusion is that May seems to be the best month for launching a successful theater Kickstarter campaign.
- We would advise not starting a Theater campaign in December, where the rate of Successful and Failed campaigns are equal.

## Play Outcomes Based on Campaign Goals
- According to the above line chart titled **Outcomes Based on Goals**, we suggest aiming for two campaign goal ranges: $1,000 to $4,999 if you have a tight budget, $35,000 to $44,999 if you foresee needing a higher budget. These two goal ranges showed the highest percentage of Successful Play campaigns, and the lowest percentage of Failed Play campaigns.

## Possible Dataset Limitations
- These charts do not account for geographic region. Right now we have results from many different countries in the same analysis.  We suggest narrowing down the scope of this analysis to a specific country where you plan on running your campaign for more accurate results.

## Suggestions for Additional Analysis
- Because our client's previous Kickstarter Campaign almost reached it's funding goal in a short period of time, we would like to explore the length of each campaign and try to determine any trends that might affect campaign duration.
- We would like to use stacked column charts to visualize the data differently, which may be easier to read than a line chart in our opinion.

[Back to top](#kickstarter-theater-campaign-analysis-with-excel)








