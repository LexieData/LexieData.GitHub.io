<img src="images/Metals_R_Us_Title.png?raw=true"/>

# Metals 'R' Us

## Introduction
Metals 'R' Us (not a metal toy store as the name might suggest) is a Canadian flotation plant that extracts impurities (silica) from iron ore concentrate. The goal is to yeild clean iron that they can sell. This is part of the mining process for manufacturing plants. 


What I learned from this project was:
  1. You can see summary statistics in Python by coding **df.describe()**
  2. 


## The Data
The data set for this project comes from <a href="https://www.kaggle.com/datasets/edumagalhaes/quality-prediction-in-a-mining-process">Kaggle</a>. 
I used Python code in a program called DeepNote to analyze the data. I had to install Pandas in order to manipulate the data and install Seaborn and Matplotlib in order to visualize the data.
When downloading the mining data for this project, there were commas where decimals should be so I used this code to fix that: <br>
```python
df = pd.read_csv('MiningProcess_Flotation_Plant_Database.csv',decimal=",")
```

Also part of the data cleaning process involved making sure all the variables were correct. The date column was defined as a string column so I changed it to a date/time column by using this code: 
```python
df['date'] = pd.to_datetime(df['date'])
```
Important facts about the data structure include:
  a. how many rows and columns are in this data set
```python
df.shape
```
The output showed 737453 rows and 24 columns.
  b. date range
Between March 2017 and September 2017, samples were taken every 20 seconds or every hour. The "% Iron Concentrate" column is important for showing how pure the iron is.

## Analysis

I answered **4** prompts related to professional basketball:
  1. Show the summary statistics for each column.
  2. Show data for only June 1, 2017.
  3. Visualize how all variables relate to one another.

### 1st Prompt 
My prompt was "The boss wants the summary statistics for each column including the mean, median, min, and max." It was quite a simple code to answer this prompt. 
<img src="images/Python Summary.png?raw=true"/>
Each row represents a different statistic. Median is represented by the 50th percentile aka "50%". 

### 2md Prompt
Our boss says something weird happened on June 1, 2017 & wants us to investigate. So I used a boolean mask and filtered the data to show only rows and columns for June 1, 2017. 
<img src="images/Python Date Range.png?raw=true"/>

### 3rd Prompt
The boss wants requests a visualization that relates all variables. I did this using the Seaborn library and creating a pairplot. A pairplot shows correlations between variables, in this case if there are any relationship between 4 columns: "% Iron Concentrate," "% Silica Concentrate," "Ore Pulp pH," and "Flotation Column 5 Level."
<img src="images/Python Seaborn1.png?raw=true"/>
<img src="images/Python Seaborn2.png?raw=true"/>
