# Sales-Analysis-dashboard
Sales Analysis Dashboard
Dashboard link: https://app.powerbi.com/links/4YAP8JhU68?ctid=7e2137dd-6ef9-46eb-974e-5086fd7cdd20&pbi_source=linkShare
Project Objective
The objective of this project is to design and develop a comprehensive sales analysis dashboard that enables sales managers, executives, and decision-makers to effectively monitor, analyze, and manage sales performance and trends. This dashboard aims to enhance sales strategies, improve decision-making, and drive revenue growth through the following specific goals
Import data to Power BI
1. Prepare csv file
2. Import CSV file to Power BI
3. Data cleaning
4. Data Modeling to manage relationship among various tables.

DAX Queries
Total Sales Amount
Sales_AMt = sum(FactInternetSales[SalesAmount])

Month 
shortmonth = switch(DimDate[MonthNumberOfYear],
1, "Jan",
2, "Feb",
3, "Mar",
4, "Apr",
5, "May",
6, "Jun",
7, "Jul",
8, "Aug",
9, "Sep",
10, "Oct",
11, "Nov",
12, "Dec")

Customer Age Group
Customer_Age_Group = 
  var _age= DATEDIFF(DimCustomer[BirthDate],today(),year)
  Return
  switch( true(),
  _age < 30,"20-30",
   _age >=30 && _age <40, "30-40",
   _age>=40 && _age <50,"40-50",
    _age >=50 && _age<60,"50-60",
   _age>=60,"60+","unknown")


Project Insight
Overview
•	Total Sales Amount of 29.27 million and sales order of 26.67 thousand.
•	The territory North America has the highest sales revenue among the three territory region
•	The product category bikes was the highest selling product category in three region followed by accessories and clothing.
•	Customers having the lesser commute distance contributed the highest in sales revenue ie. 11million
•	Married customers contribute to the higher revenue of the company.

Sales Analysis Dashboard Using Power BI
1.	Use of Drill Down tools to further navigate the sales performance with the details of the product analyzed through sales territory, age group, marital status and product category.
2.	Use of tool tips to analyze whether number of children of customer also contribute to the sales revenue








