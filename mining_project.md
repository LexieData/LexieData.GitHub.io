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
By using the code below, I could see how many rows and columns are in this data set:
```python
df.shape
```
The output showed 737453 rows and 24 columns.

Also part of the data cleaning process involved making sure all the variables were correct. The date column was defined as a string column so I changed it to a date/time column by using this code: 
```python
df['date'] = pd.to_datetime(df['date'])
```

Between March 2017 and September 2017, samples were taken every 20 seconds or every hour. The "% Iron Concentrate" column is important for showing how pure the iron is.

## Analysis

I answered **4** prompts related to professional basketball:
  1. Show the summary statistics for each column
  2. 

### 1. 
My prompt was "The boss wants the summary statistics for each column including the mean, median, min, and max." It was quite a simple code to answer this prompt. 
<img src="images/Metals_R_Us_Title.png?raw=true"/>
### 2. 
Our boss says something weird happened on June 1, 2017 & wants us to investigate. So I filtered the data to show only rows and columns between the dates May 31, 2017 and June 1, 2017. 

```python
print('this is the python code I used to solve this problem')
```

