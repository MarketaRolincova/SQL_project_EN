# SQL project – Data about wages and food prices in the Czechia and their processing using SQL

# Project assignment
In your analytical department of an independent company that deals with the standard of living of citizens, you have agreed to try to answer a few defined research questions that address the availability of staple foods to the general public. Colleagues have already defined the basic questions that they will try to answer and provide this information to the press department. This department will present the results at the next conference focused on this area.

To do this, they need you to prepare robust data bases in which it will be possible to see a comparison of the availability of food based on average incomes over a certain period of time.

As additional material, prepare a table with GDP, GINI coefficient, and population of other European countries in the same period, as a primary overview for the Czech Republic.

# Research questions
1.	Are wages rising in all industries over the years, or falling in some?
2.	How many liters of milk and kilograms of bread can be bought in the first and last comparable periods in the available price and wage data?
3.	Which food category is increasing in price the slowest (has the lowest percentage year-on-year increase)?
4.	Has there been a year in which the year-on-year increase in food prices was significantly higher than wage growth (greater than 10 %)?
5.	Does the level of GDP affect changes in wages and food prices? Or, if the GDP increases more significantly in one year, will this be reflected in food prices or wages in the same or the following year by a more significant increase?

# Method
In the project, I use data on wages in various sectors and on the prices of selected foods over a period of several years. The data set comes from the Czech Republic's Open Data Portal.

First, I created a joined table from 5 tables with primary data (2x fact table, 3x codebook), I selected the ones I needed to answer the questions. My goal was to create a single table with aggregated data over a period of time. I first aggregated the data according to the specified categories - 1) industrial branches in the case of wages (19 branches) and 2) food category in the case of food prices (27 categories) and then according to the common time period - years 2006-2018. The resulting table contains the average price/wage for each category and year.

Furthermore, I created an accompanying table with data about European countries from two primary tables that contain information about the countries of the world and their economies.

I then created SQL queries over the tables to answer the research questions. The SQL files are named "research question" followed by the number of the question I am answering.

# Answers to research questions

# 1.	Are wages rising in all industries over the years, or falling in some?
Only 4 sectors out of a total of 19 are recording sustained wage growth. The sectors with continuous growth are:
- Agriculture, forestry, fishing
- Manufacturing industry
- Health and social care
- Another activities

Two periods in particular are significant in the data, namely the years 2009/2010 and 2012.

In 2009/2010 there was a year-on-year decrease in some sectors, namely the following sectors:
- Mining and quarrying
- Production and distribution of electricity, gas, heat and air conditioning
- Accommodation, catering and hospitality
- Professional, scientific, and technical activity
- Education
- Cultural, entertainment, and recreational activities

It is interesting that only one sector (Public Administration and Defence; Mandatory Social Security) recorded a significant increase in 2009, after which the wage decreased and the increase above the level of 2009 occurred again only in 2014.

The year 2012 was significant in terms of wage growth. Since this year, most sectors have seen a decline, which reversed in 2014, 2015, and sometimes even 2017 in some cases.

# 2.	How many liters of milk and kilograms of bread can be bought in the first and last comparable periods in the available price and wage data?
In 2006, it was possible to purchase from an average salary of CZK 20,754:
- 1,437 liters of milk
- 1,287 kilograms of bread

In 2018, it was possible to purchase from an average salary of CZK 32,536:
- 1,642 liters of milk
- 1,342 kilograms of bread

Based on these numbers, the data suggests that average wages are rising at a faster rate than food prices, and society is getting richer.

# 3.	Which food category is increasing in price the slowest (has the lowest percentage year-on-year increase)?
The category that increases in price the slowest is Quality white wine. Followed by Draft beer, light beer, bottled beer, and Natural mineral sparkling water. However, all of these are technically drinks. Therefore, the first real food that increases in price the slowest is Ham salami, followed by Boneless beef.

It should be noted that there are 24 categories of food (out of a total of 27 categories) that are even cheaper, not more expensive.

# 4.	Has there been a year in which the year-on-year increase in food prices was significantly higher than wage growth (greater than 10 %)?
There is none, the highest difference in the year-on-year increase in food prices compared to wage growth is 6.79% between 2012 and 2013.

# 5.	Does the level of GDP affect changes in wages and food prices? Or, if the GDP increases more significantly in one year, will this be reflected in food prices or wages in the same or the following year by a more significant increase?
The level of GDP has no significant effect on food prices or the level of wages in a given year or the following year, i.e. if GDP increases significantly in one year, it will not affect food prices or wages in the same direction.

As an example, I will give the years 2011-2013, we have already marked this period in research question 1 as one of the economic peaks for many branches of industry, and research question 4 in turn indicates that it was the highest increase in prices compared to wages for the monitored period (6.79%). However, GDP at that time did not grow significantly, on the contrary, it even fell in some years.

- annual GDP growth 2010/2011: 1.79%
- year-on-year decrease in GDP 2011/2012: -0.79%
- year-on-year decrease in GDP 2012/2013: -0.05%

