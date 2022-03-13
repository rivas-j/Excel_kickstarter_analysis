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
Using a filtered pivot table, we generated this line chart to visualize the relationship between launch dates and the success rate of theater Kickstarter campaigns:

![Theater Outcomes Based on Launch Date](https://github.com/rivas-j/kickstarter-analysis/blob/5a990a44e53bcde5722ba97e0bd8fb429a922622/Resources/Theater_Outcomes_vs_Launch.png)



### Analysis of Outcomes Based on Goals
![Play Outcomes vs Goals](https://github.com/rivas-j/kickstarter-analysis/blob/5a990a44e53bcde5722ba97e0bd8fb429a922622/Resources/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered
- The dates in the initial data set were in UNIX format, which is very difficult for customers and analysts to read. It also makes it harder to organize our pivot tables and charts. We addressed this by using Excel formulas to convert the UNIX dates to Day/Month/Year format.
- Originally, the Parent Category and Subcategory of each Kickstarter campaign were in the same column. We used Excel's text to columns feature to split this data into two separate columns respectively titled "Parent Category" and "Subcategory". Doing this allowed us to perform separate analyses for the "Theater" category and the "Plays" subcategory.

## Results

### Theater Outcomes Based on Launch Date
- Based on the above chart, the month of May yielded the most successful Theater campaigns. The months of May through August, and October also yielded the highest number of failed Theater campaigns. Our conclusion is that May will be the best month for launching a successful new Theater campaign.
- We would advise not starting a Theater campaign in December, where the rate of Successful and Failed are equal.

### Play Outcomes Based on Campaign Goals
- What can you conclude about the Outcomes based on Goals?

### Possible Limitation in our Data Set
- One possible limitation of these charts is not accounting for geographic region. Right now we have results from many different countries in the same analysis.  We suggest narrowing down the scope of this analysis to a specific country where you plan on running your campaign for more accurate results.

### Suggestions for Additional Scope of Analysis
- Because our client's previous Kickstarter Campaign almost reached it's funding goal in a short period of time, we would like to explore the length of each campaign and try to determine any trends that might affect campaign duration.
- We would like to explore using Stacked Column charts to visualize the data differently, which may be easier to read than a line chart in our opinion.
