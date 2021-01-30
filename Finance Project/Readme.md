# Finance Data Project



## Get the Data

In this section we will learn how to use pandas to directly read data from Google finance using pandas!
But I got problems when reading the data through Google finance, the reason is Google has discontinued the API, so I use the [all_banks file](https://github.com/afaf1204/Data-Projects/blob/main/Finance%20Project/all_banks) instead.

## Project Intro/Objective
In this data project we will focus on exploratory data analysis of stock prices. Keep in mind, this project is just meant to practice your visualization and pandas skills, it is not meant to be a robust financial analysis or be taken as financial advice.

## Project Library
- Numpy
- Pandas
- Matplotlib
- Seaborn
- datetime
- matplotlib.pyplot
- Plotly
- Cufflinks

## Data and Setup
In this section, I want to show some of the data information, it includes Data Frame Info and Data Frame Head. We use stock information from the following bank:
- Bank of America (BAC)
- CitiGroup (C)
- Goldman Sachs (GS)
- JPMorgan Chase (JPM)
- Morgan Stanley (MS)
- Wells Fargo (WF)

Data Frame Head:

![Data Frame Head](https://github.com/afaf1204/Data-Projects/blob/main/Finance%20Project/images/1.%20Data%20Frame%20Head.PNG)

Bank of America Head:

![BAC Data Frame Head](https://github.com/afaf1204/Data-Projects/blob/main/Finance%20Project/images/2.%20BAC%20Data%20Frame%20Head.PNG)

## Exploratory Data Analysis
From all banks data, we can calculate the returns for each bank to find how each bank performance during 2008 financial crisis.

All banks returns data frame head:

![Bank Returns Data Frame Head](https://github.com/afaf1204/Data-Projects/blob/main/Finance%20Project/images/3.%20Bank%20Returns%20Data%20Frame%20Head.PNG)

For further study, we can use pairplot to see how each bank performance related to each other:

![Data Frame Pairplot](https://github.com/afaf1204/Data-Projects/blob/main/Finance%20Project/images/4.%20Data%20Frame%20Pairplot.PNG)

For better understanding, we look to all banks return data. We looking for minimum, maximum, and standard deviation from each bank.

Minimum returns:

![Returns min](https://github.com/afaf1204/Data-Projects/blob/main/Finance%20Project/images/5.%20Returns%20min.PNG)

Maximum returns:

![Returns max](https://github.com/afaf1204/Data-Projects/blob/main/Finance%20Project/images/6.%20Returns%20max.PNG)

Returns standard deviation:

![Returns std](https://github.com/afaf1204/Data-Projects/blob/main/Finance%20Project/images/7.%20Returns%20std.PNG)

Returns 2015 standard deviation:

![Returns 2015 std](https://github.com/afaf1204/Data-Projects/blob/main/Finance%20Project/images/8.%20Returns%202015%20std.PNG)

Morgan Stanley 2015 distribution plot:

![Morgan Stanley Returns 2015 Distplot std](https://github.com/afaf1204/Data-Projects/blob/main/Finance%20Project/images/10.%20MS%20Returns%202015%20Distplot%20std.PNG)

CitiGroup 2008 distribution plot:

![CitiGroup Returns 2015 Distplot std](https://github.com/afaf1204/Data-Projects/blob/main/Finance%20Project/images/9.%20CitiGroup%20Returns%202015%20Distplot%20std.PNG)

## Data Visualization
