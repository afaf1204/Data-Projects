# Finance Data Project

## Get the Data
In this section, I plan to use pandas to directly read data from Google finance using pandas!
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
For further visualization, we try to visualize some financial analysis.
First, we try to visualize close price for each bank for the entire index of time (2008-2016).
Using for loop to create simple line plot:

![All Banks Close Price Lineplot](https://github.com/afaf1204/Data-Projects/blob/main/Finance%20Project/images/11.%20All%20Banks%20Close%20Price%20Lineplot.PNG)

Using .xs to get cross section of the data:

![All Banks Close Price Lineplot using .xs](https://github.com/afaf1204/Data-Projects/blob/main/Finance%20Project/images/12.%20All%20Banks%20Close%20Price%20Lineplot%20using%20.xs.PNG)

We can see, using for loop and using .xs resulting the same plot, the difference is we can use shorter code while using .xs than using for loop.

After that, we create line plot using iplot, the difference is we can create an interactive graph while using iplot, where we can get the data directly when we move our cursor to certain line.

![All Banks Close Price Lineplot using iplot](https://github.com/afaf1204/Data-Projects/blob/main/Finance%20Project/images/13.%20All%20Banks%20Close%20Price%20Lineplot%20using%20iplot.PNG)

Then, we try to create a moving averages plot using rolling with window = 30.

![Bank of America 2008 moving averages](https://github.com/afaf1204/Data-Projects/blob/main/Finance%20Project/images/14.%20Bank%20of%20America%202008%20moving%20averages.PNG)

After that, we try to create correlation data frame using Close price as key value.

![All Banks Close Price Correlation Head](https://github.com/afaf1204/Data-Projects/blob/main/Finance%20Project/images/17.%20All%20Banks%20Close%20Price%20Correlation%20Head.PNG)

Then we try to create HeatMap and ClusterMap using simple plot.

Correlation HeatMap:

![Heatmap All Banks Close Price Correlation](https://github.com/afaf1204/Data-Projects/blob/main/Finance%20Project/images/15.%20Heatmap%20All%20Banks%20Close%20Price%20Correlation.PNG)

Correlation ClusterMap:

![Clustermap All Banks Close Price Correlation](https://github.com/afaf1204/Data-Projects/blob/main/Finance%20Project/images/16.%20Clustermap%20All%20Banks%20Close%20Price%20Correlation.PNG)

After that, we try to create HeatMap using iplot.

Correlation HeatMap using iplot:

![Heatmap All Banks Close Price Correlation using iplot](https://github.com/afaf1204/Data-Projects/blob/main/Finance%20Project/images/18.%20Heatmap%20All%20Banks%20Close%20Price%20Correlation%20using%20iplot.PNG)

The difference between simple plot and iplot is when using iplot, we can **create an interactive plot** where we can see the value for certain position using our pointer, and simple plot just showing the plot and **does not create** an interactive plot.

Furthermore, we try to create some advance financial analysis technic. We try to plot using iplot to get an interactive plot. 

First, we create Bank of America candlestick for the year 2015. Using iplot and kind as 'candle', we get candlestick plot:

![Bank of America 2015 candlestick](https://github.com/afaf1204/Data-Projects/blob/main/Finance%20Project/images/19.%20Bank%20of%20America%202015%20candlestick.PNG)

Second, we create Morgan Stanley simple moving averages for the year 2015. We use .ta_plot(study='sma') and periods [13, 21, 55]:

![Morgan Stanley 2015 simple moving average](https://github.com/afaf1204/Data-Projects/blob/main/Finance%20Project/images/20.%20Morgan%20Stanley%202015%20simple%20moving%20average.PNG)

Third, we create Bank of America Bollinger Band Plot for the year 2015. We use .ta_plot(study='boll'):

![Bank of America Bollinger Band Plot](https://github.com/afaf1204/Data-Projects/blob/main/Finance%20Project/images/21.%20Bank%20of%20America%20Bollinger%20Band%20Plot.PNG)

## Conclusion

## Further Information
For further information regarding the code that I use in this project, kindly check this [link](https://github.com/afaf1204/Data-Projects/blob/main/Finance%20Project/Finance%20Project.ipynb)
