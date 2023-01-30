# Application of DAX (Data Analysis Expression)

# Introduction
On several occasions, we’ve been able to build a Power BI Report by dragging and dropping the various fields involved from connected tables. This is not always sufficient for all business questions, in many sceenarios, you will need to apply DAX to create new measures and columns that will help you provide the right answers to the business question. Simply put it this way, DAX makes it possible to extend the functions to Microsoft Power BI.

# Objective 
Learning throught #30daysOfLearning on:
Application of DAX concepts on a Dashboard Project
DAX (Data analysis Expression)
Measure
Calculated Column
Context
Time Intelligence
DAX is developed by Microsoft
A library of Functions and Operators
Build Formulas and Expression 
Create Calculated tables, Columns and Measures

* Measure are summarization of data
A way of defining aggregate calculation of data
It is often called Calculated Measure
* Column Vs Measure
Calculated column creates a value for each row in table
Measures are calculated on demand 
Measure are calculated based on filters

- For DAX to be easy to use 
1 Function ( There are mor than 250 function)
2 Evalution context

- What to know about function
1 Synatax (input)
2 Type
Multiple (Sum)
Single (Filter)

- Aims of Analysis Data is to summarize the data.
Single point- give data like, sum, average, percentage.
Tablefunction- summarizing the portion of the table
- Calculated Function
- Calculated Table
- Calculated Column

# Exploration
To know the different function in DAX
-	Calculated Column 
* Calculated Value without a function
E.g Create new column (Discount amount)
Discount Amount = Sales[Sales]*Sales[Discount]
* Calculated Value out a function in DAX
Related
E.g Region =Related(Location[Region]
-	Calculated Table
E.g New Table 
Calendar = calendarauto[]
E.g Office suppliers Products = Filters(Products, products[category]= “Office Suppliers”

Measure: allow us to exted our analysis further more.
•	Create a new measure
E.g Revenue = Sum(Sales[Sale])
Note: Measure are the formular use in the Viz, don’t add to data
* Objective: to display the team by sale by particular month
 Input slicer – Order of date(Year, Month)
 Bar chart of sales by sales Team
 Right on sales to create a new measure
- To understand measure you must knw – Evaluation context (Row and Filter)
- Measure work based on filter context
E.g Revenue without Organic = Sumx(Sales[Sales])
=Sumx(
  …………Filter(sales, Related(salesReps
   [sales team])<>”organic”)
   ………...Sales[Sales])
- To compare or filter the year and  month 
E.g Previous month Revenue = Calculated([Revenue(WO Organic)],Previous month (sales[order date] . [date])
 
# Data sourcing
#30DaysOfLearning
Data Provided to implement what was taught in the session 
Data link https://aka.ms/30DLDATGitHubRepo 
The folder name is “DAX Dataset”

Then, we create a report for the Dataset 

![DAX APP](https://user-images.githubusercontent.com/107544339/215388418-ec490b20-6e8b-412f-b2bb-f5bbd432a95b.png)

![This image] https://github.com/OluwaseunPhronesis/DAX-Data-Analysis-Xpression-/blob/main/DAX%20APP.png

