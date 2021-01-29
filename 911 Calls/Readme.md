# 911 Calls Capstone Project

For this capstone project we will be analyzing some 911 call data from [Kaggle](https://www.kaggle.com/mchirico/montcoalert). The data contains the following fields:

- lat : String variable, Latitude
- lng: String variable, Longitude
- desc: String variable, Description of the Emergency Call
- zip: String variable, Zipcode
- title: String variable, Title
- timeStamp: String variable, YYYY-MM-DD HH:MM:SS
- twp: String variable, Township
- addr: String variable, Address
- e: String variable, Dummy variable (always 1)

## Project Intro/Objective
The purpose of this project is show step-by-step how to analyze and visualize the dataset to better understand 911 calls and what originates them.

## Project Library
- Numpy
- Pandas
- Matplotlib
- Seaborn

## Data and Setup
In this section, I want to show some of the data information, it includes Data Frame Info and Data Frame Head.

### Data Frame Info
After imported all the libraries needed, I check the info() and head() of the data frame.

![Data Frame Info](https://github.com/afaf1204/Data-Projects/blob/main/911%20Calls/Images/1.%20DataFrame%20Info.PNG)

### Data Frame Head
![Data Frame Head](https://github.com/afaf1204/Data-Projects/blob/main/911%20Calls/Images/2.%20DataFrame%20Head.PNG)

## Data Visualization
In this section, I want to visualize the data needed using seaborn and look for something strange about the data.

### Reason Countplot
In this section, I will show you the countplot from the reason of all 911 calls. Before do this, I create a new feature from the title column where I split the reason and the department, where I got EMS, Traffic, and Fire departments.

![Reason Countplot](https://github.com/afaf1204/Data-Projects/blob/main/911%20Calls/Images/3.%20Reason%20Countplot.PNG)

### Day of Week Countplot
In this section, I create a coountplot of the Day of Week column with hue based off of the Reason Column.

![Day of Week Countplot](https://github.com/afaf1204/Data-Projects/blob/main/911%20Calls/Images/4.%20Day%20of%20Week%20Countplot.PNG)

### Month Countplot
In this section, I create a coountplot of the Month column with hue based off of the Reason Column.

![Month Countplot](https://github.com/afaf1204/Data-Projects/blob/main/911%20Calls/Images/5.%20Month%20Countplot.PNG)

## Exploratory Data Analysis
From month countplot, we can see that the our data has missing value, where there are some missing months. To see this missing data, we can use pandas and then visualize it using simple plot and lmplot (2D scatterplot with an optional overlaid regression line).

### Create groupBy Data Using Month Column
In this section, I create groupBy data using month column and then count all the data for aggregation, and then we can see the groupBy data frame using head() of the data frame.

![byMonth Head](https://github.com/afaf1204/Data-Projects/blob/main/911%20Calls/Images/16.%20byMonth%20Head.PNG)

### groupBy Data Visualization
Futhermore, we can visualize the data using simple plot and lmplot. 

![Count Calls per Month](https://github.com/afaf1204/Data-Projects/blob/main/911%20Calls/Images/6.%20Count%20Calls%20per%20Month.PNG)

![lmplot Count Calls per Month](https://github.com/afaf1204/Data-Projects/blob/main/911%20Calls/Images/7.%20lmplot%20Count%20Calls%20per%20Month.PNG)

With simple plot and lmplot, we can see the data from month 9 to 11.

### Visualize Available Data
For further understanding, we can visualize the available data. We can visualize the data by date and by departments.

Data by date:

![Groupby date call](https://github.com/afaf1204/Data-Projects/blob/main/911%20Calls/Images/8.%20Groupby%20date%20call.PNG)

Data by Traffic:

![Trafic Call Reason](https://github.com/afaf1204/Data-Projects/blob/main/911%20Calls/Images/9.%20Traffic%20Call%20Reason.PNG)

Data by Fire:

![Fire Call Reason](https://github.com/afaf1204/Data-Projects/blob/main/911%20Calls/Images/10.%20Fire%20Call%20Reason.PNG)

Data by EMS:

![EMS Call Reason](https://github.com/afaf1204/Data-Projects/blob/main/911%20Calls/Images/11.%20EMS%20Call%20Reason.PNG)

### HeatMap and ClusterMap Data
To help us read the data, we can use HeatMap and ClusterMap. HeatMap and ClusterMap makes it easy to read some related data where we collect the related data in certain places.

Using groupBy we create a new table using **day of week** and **date** column and then count all the data.
![dayHour Head](https://github.com/afaf1204/Data-Projects/blob/main/911%20Calls/Images/17.%20dayHour%20Head.PNG)

Then we create HeatMap and ClusterMap using dayHour data frame.
HeadMap of dayHour data frame.

![Hour-Day of Week Heatmap](https://github.com/afaf1204/Data-Projects/blob/main/911%20Calls/Images/12.%20Hour-Day%20of%20Week%20Heatmap.PNG)

ClusterMap of dayHour data frame.

![Hour-Day of Week Clustermap](https://github.com/afaf1204/Data-Projects/blob/main/911%20Calls/Images/13.%20Hour-Day%20of%20Week%20Clustermap.PNG)

Then using groupBy we create a new table using **day of week** and **month** column and then count all the data.
![dayMonth Head](https://github.com/afaf1204/Data-Projects/blob/main/911%20Calls/Images/18.%20dayMonth%20Head.PNG)

Then we create HeatMap and ClusterMap using dayHour data frame.
HeadMap of dayHour data frame.

![Month-Day of Week Heatmap](https://github.com/afaf1204/Data-Projects/blob/main/911%20Calls/Images/14.%20Month-Day%20of%20Week%20Heatmap.PNG)

ClusterMap of dayHour data frame.

![Month-Day of Week Clustermap](https://github.com/afaf1204/Data-Projects/blob/main/911%20Calls/Images/15.%20Month-Day%20of%20Week%20Clustermap.PNG)

From this HeatMap and ClusterMap, we can conclude that:
- There are **high** 911 call between hour **8-20**.
- There are **low** 911 call between hour **22-6**.
- Month **1, 4, and 7** has the **most** 911 call.
- Month **8 and 12** has **low** 911 call.
- On **saturday month 1**, there is **the highest** 911 call.


