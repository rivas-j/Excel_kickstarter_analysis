# Kickstarting with Excel

## Overview of Project

### Our client ran a Kickstarter campaign for a play called "Fever" that almost reached its goal in a short amount of time. The overall aim of this analysis is to determine how other Theater campaigns during that time fared by looking at launch dates and funding goals.

### We compiled data from Kickstarter Campaigns from the years 2009-2017 in an Excel spreadsheet, then analyzed trends to help our client decide details for an upcoming fundraiser. First we formatted the Excel data in order to facilitate our analysis. Here are some methods we utilized: 

- Added colors via conditional formatting to make the spreadsheet more visually striking

- Converted date formats from UNIX to Months/Years to help pivot table analysis

- Separated Kickstarter Campaign categories and subcategories into their own columns

### After improving the data set with formatting, we utilized pivot tables, COUNTIFS formulas, and Line Charts to determine trends surrounding launch dates and how campaign outcomes related the the initial goal amount. Below we will dive into the details around our analysis, and will share our suggestions based on our findings.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

First we generated a pivot table from the original data set using the **Outcomes** in the column portion, **Date Created** in the row portion, with the **Parent Category** and **Years** as filters, as seen in the screenshot below:

![Pivot Table - Theater Outcomes Based on Launch Date](https://github.com/rivas-j/kickstarter-analysis/blob/8768d94373275b37a591f8606f02490f6646e1a3/Resources/Pivot_Table_Theater_Outcomes_vs_Launch.png)

We used the filter feature to focus solely on the "Theater" category, and filtered the Outcomes to highlight just the Failed, Successful and Canceled campaigns.

Using that filtered pivot table, we generated this line chart to visualize the relationship between launch dates and the success rate of theater Kickstarter campaigns:

![Chart - Theater Outcomes Based on Launch Date](https://github.com/rivas-j/kickstarter-analysis/blob/5a990a44e53bcde5722ba97e0bd8fb429a922622/Resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals

For this portion of the analysis we created a simple table meant to analyze the campaign funding goals in different spending tiers, then summarizing the rates of Successful, Failed and Canceled. Please see the completed table in the screenshot below:

![Table - Play Outcomes vs Goals](https://github.com/rivas-j/kickstarter-analysis/blob/763dc868a1c70b7a35fb8e169b8e17f5dfaa4438/Resources/Table_Outcomes_vs_Goals.png)

We used COUNTIFS formulas, such as the quoted one below, to calculate the count of Successful plays within each goal tier outlined in the table.

> =COUNTIFS(Kickstarter!$F:$F,"successful",Kickstarter!$D:$D,"<1000",Kickstarter!$R:$R,"plays")

We then calculated the percentage of each outcome in order to generate the line chart below:

![Chart - Play Outcomes vs Goals](https://github.com/rivas-j/kickstarter-analysis/blob/5a990a44e53bcde5722ba97e0bd8fb429a922622/Resources/Outcomes_vs_Goals.png)

This line chart uses the Goal column along the X-Axis, and Percentage of Outcomes along the Y-Axis. We included a legend below depicting each colored line corresponding to Percentage Successful, and Failed plays based on the Goal amount.

### Challenges and Difficulties Encountered
- The dates in the initial data set were in UNIX format, which is very difficult for customers and analysts to read. It also makes it harder to organize our pivot tables and charts. We addressed this by using Excel formulas to convert the UNIX dates to Day/Month/Year format.
- Originally, the **Parent Category** and **Subcategory** of each Kickstarter campaign were in the same column. We used Excel's text to columns feature to split this data into two separate columns respectively titled "Parent Category" and "Subcategory". Doing this allowed us to perform separate analyses for the **Theater** category and the **Plays** subcategory.
- When we first generated the line chart for the Play Outcomes vs Goals chart, there was a lot of noise. Since we initially highlighted the entire table to generate the chart, we had to adjust the formatting by using the filter feature, removing the columns from the original table we wanted to exclude. Here is a screenshot of how we accomplished it:

![Formatting Chart - Play Outcomes vs Goals](https://github.com/rivas-j/kickstarter-analysis/blob/be58b9012a4df8d6539c990a99a9090419ca4001/Resources/Formatting%20-%20Outcomes%20Based%20on%20Goals.png)

## Results

### Theater Outcomes Based on Launch Date
- Based on the above chart titled **Theater Outcomes by Launch Date**, the month of May yielded the most Successful Theater campaigns. The months of May through August, and October also yielded the highest number of failed Theater campaigns. Our conclusion is that May will be the best month for launching a Successful new Theater campaign.
- We would advise not starting a Theater campaign in December, where the rate of Successful and Failed are equal.

### Play Outcomes Based on Campaign Goals
- According to the above line chart titled **Outcomes Based on Goals**, we suggest aiming for two campaign goal ranges: $1,000 to $4,999 if you have a tight budget, $35,000 to $44,999 if you foresee needing a higher budget. These two goal ranges showed the highest Successful percentage of Play campaigns, and the lowest failed percentage of Play campaigns.

### Possible Limitation in our Data Set
- One possible limitation of these charts is not accounting for geographic region. Right now we have results from many different countries in the same analysis.  We suggest narrowing down the scope of this analysis to a specific country where you plan on running your campaign for more accurate results.

### Suggestions for Additional Scope of Analysis
- Because our client's previous Kickstarter Campaign almost reached it's funding goal in a short period of time, we would like to explore the length of each campaign and try to determine any trends that might affect campaign duration.
- We would like to explore using stacked column charts to visualize the data differently, which may be easier to read than a line chart in our opinion.
