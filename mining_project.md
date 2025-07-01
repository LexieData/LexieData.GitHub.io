<img src="images/Metals_R_Us_Title.png?raw=true"/>

# Metals 'R' Us: A Mining Analysis Using Python

## Introduction
Metals 'R' Us (not a metal toy store as the name might suggest) is a Canadian flotation plant that extracts impurities (e.g. silica) from iron ore concentrate. The goal is to yeild clean iron that they can sell. This is part of the mining process for manufacturing plants. In order to practice engineering data analysis, I was assigned to analyze this mining data for Avery Smith's Data Analytics Accelerator course.

What I learned from this project was:
  1. You can see summary statistics in Python by coding **df.describe()**
  2. How to create a **boolean mask** and filter data
  3. The **pairplot** accessed through Seaborn showed no correlation between variables
  4. A **line graph** showed "% Iron Concentrate" dropped the same time "% Silica Concentrate" spiked on the same day


## The Data
The data set for this project comes from <a href="https://www.kaggle.com/datasets/edumagalhaes/quality-prediction-in-a-mining-process">Kaggle</a>. 
I used Python code in a program called DeepNote to analyze the data. I had to install Pandas in order to manipulate the data and install Seaborn and Matplotlib in order to visualize the data.
When downloading the mining data for this project, there were commas where decimals should be so I used this code to fix that: <br>
```python
df = pd.read_csv('MiningProcess_Flotation_Plant_Database.csv',decimal=",")
```
Also part of the data cleaning process involved ensuring all the variables were correct. The date column was defined as a string column so I changed it to a date/time column by using this code using Pandas: 
```python
df['date'] = pd.to_datetime(df['date'])
```

I determined there were 737,453 rows and 24 columns by using this code:
```python
df.shape
```
Also, the date range was between March 2017 and September 2017 and samples were taken every 20 seconds or every hour (depending on the column). The "% Iron Concentrate" column is important for showing how pure the iron is.

## Analysis

I answered **4** prompts related to professional basketball:
  1. Show the summary statistics for each column.
  2. Show data for only June 1, 2017.
  3. Visualize how all variables relate to one another.

### 1st Prompt 
The boss wants the summary statistics for each column including the mean, median, min, and max. It was quite a simple code to answer this prompt. 
<img src="images/Python Summary.png?raw=true"/>
Each row represents a different statistic. Median is represented by the 50th percentile aka "50%". 

### 2nd Prompt
The boss says something weird happened on June 1, 2017 and wants me to investigate. So I used a boolean mask and filtered the data to show only rows and columns for June 1, 2017. 
<img src="images/Python Date Range.png?raw=true"/>
Since there are 432 pages of this data, it is hard to see any salient numbers. Creating a visualization would help to see any trends present, which leads into prompt 3. 

### 3rd Prompt
The boss then requests a visualization that relates all variables, for June 1, 2017. I did this using the Seaborn library and creating a pairplot using this code:
```python
sns.pairplot(df_june_important)
```
A pairplot shows correlations between variables, in this case if there are any relationships between 4 columns: "% Iron Concentrate," "% Silica Concentrate," "Ore Pulp pH," and "Flotation Column 5 Level."
<img src="images/Python Seaborn1.png?raw=true"/>
<img src="images/Python Seaborn2.png?raw=true"/>
As you can see, there is no discernable linear trend or patterns. I confirmed this by using a correlation matrix:
<img src="images/Python Correlation.png?raw=true"/>
All the numbers are not close to 1 (except where the same variables intersect) or -1 so these numbers also do not show a relationship to each other.

### 4th Prompt
The boss wants to see how the % Iron Concentrate and the other variables change throughout June 1st, 2017. I created a line graph in Seaborn to show the relationship of every pointfor "% Iron Concentrate" throughout the day when samples were taken:
```python
sns.lineplot(x='date', y='% Iron Concentrate', data=df_june)
```
Then I created line graphs for the rest of the variables using a "for loop" in Matplotlib so I could write one loop that creates multiple graphs:
```python
for i in important_cols:
    sns.lineplot(x='date', y=i, data=df_june)
    import matplotlib.pyplot as plt
    plt.show()
```
<img src="images/Python Line Graph1.png?raw=true"/>
<img src="images/Python Line Graph2.png?raw=true"/>
<img src="images/Python Line Graph3.png?raw=true"/>
<img src="images/Python Line Graph4.png?raw=true"/>
From these graphs, you can see important spikes in the data i.e. around the 9:00 sample, there was a low percentage of iron concentrate and a high percentage of silica concentrate. Also, at 15:00 the "Flotation Column 5 Level" suddenly drops from a steady 500 to almost nothing; in this case this means the lower the level, the higher the grade of concentration. 

## Conclusion 
In this guided engineering project for the Data Analytics Accelerator, I learned how to code in Python, how to use/download libraries in Python such as Pandas, Seaborn, and Matplotlib, and how to analyze mining data. Please reach out if you would like to connect on <a href="https://www.linkedin.com/in/lexie-langella/">LinkedIn</a>! 
