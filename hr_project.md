<img src="images/The HR Project.png"/>

# Driven to Attrition: Insights for HR

There are many reasons why employees leave a company. Finding out why employees leave can help a company reduce the cost of training new employees, increase employee satisfaction/retention rate, and improve efficiency and productivty by having a stable workforce.

For this guided project, I analyzed fictional people data from IBM by pretending to be an intern for IBM's Human Resources department. The boss wants to know why people are leaving the company aka the company's attrition. 

Four takeways from this project are: <br>
  1. The strongest positive correlation was between **monthly income** and **total working years** <br>
  2. How to create a **pairplot** in R to show correlations between company demographics. <br>
  3. A **box and whisker plot** showed the average age an employee left the company was **33** years old. <br>
  4. By creating a **multiple linear regression model**, a person’s age and total years worked at this company explains around **60%** of the variance in people’s monthly income.

## The Data
This data set comes from Kaggle and can be found <a href="https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset">here</a>. 
There are 1,470 rows of data; each representing an employee and 35 columns that describe each employee, including the most important column for the project: "Attrition".  
I uploaded the data set into RStudio and used the programming language "R" to glean insights and visualize the data.

The boss had four tasks/questions:
  1. How do the most important demographics correlate?
  2. Create a pairplot to show this correlation.
  3. Use data to dispute a claim that the older employees were let go at a higher rate than the younger folks.
  4. Create a multiple linear regression model that predicts the monthly income based upon age and total working years.

## Analysis
### Task 1
The company wants to get an overview of how some of the most important demographics correlate. I did this by creating a correlation matrix.

<img src="images/R Correlation1.png?raw=true"/>
<img src="images/R Correlation2.png?raw=true"/>
<img src="images/R Correlation3.png?raw=true"/>
The four highest correlations are: a fairly strong positive correlation (.77) between monthly income and total working years, a fairly strong positive correlation (.68) between age and total working years, a moderately positive correlation (.49) between monthly income and age, and a low correlation (.30) between number of companies worked and age. <br>

### Task 2
The boss wants to see a visual of the top four correlations. I did this by creating a pairplot using the "pairs" function in R:

<img src="images/R Pairplot.png?raw=true"/>

This pairplot is represented as scatter plots that compare two variables at a time. From this pairplot, I see that the older you get, the more time you spend working and the more monthly income you make. This insight supports the correlation matrix made previously.

### Task 3
A disgruntled employee is suing the company because they think layoffs were heavily influenced by ageism. They're claiming the older employees were let go at a higher rate than the younger folks. The boss wants me to shut this down with the power of statistics. I used a box and whisker plot to show the average age of employees who were fired/left the company.

<img src="images/R Box and Whisker Plot.png?raw=true"/>

This plot shows the average age of the person who was fired/left was slightly lower than those who stayed and was between age 30 and 40. But to be sure, I used hypothesis testing. The hypothesis test used is the Welch Two Sample t-test since I am comparing two samples. 

<img src="images/R Hypothesis Test.png?raw=true"/>

The p-value is 1.38e-08 and since it’s a really small number, there is a statistically significant difference between the older and younger employees. These results support the box and whisker plot by showing more young employees left the company than older employees. The average age of those who left the company was 33 years old.

### Task 4
The boss first wants to see a linear regression model that predicts monthly income based on age. I did this by using the lm or linear model function in R then adding "summary" to the function to see the results:

<img src="images/R Linear Model1.png?raw=true"/>

Since the p-value is less than .05 and by looking at the R squared value, we can say that a person’s age at this company explains 25% of the variance in people’s monthly income. <br>

Now the boss wants to see a multiple linear regression model that predicts monthly income based on age AND total working years. I added the "TotalWorkingYears" variable by using the + sign in the orginal linear model function:

<img src="images/R Linear Model2.png?raw=true"/>

By adding total working years, the r squared value went up so we can say that a person’s age and total working years at this company explains around 60% of the variance in people’s monthly income. So factoring in both age and total working years has a higher predictability on effecting monthly income. 

## Conclusion

I am happy to have learned and practiced some R skills.



From this data, I answered three questions: which schools are struggling the most, how does class size effect college admission, and what are the top math schools in the state. My Tableau dashboard showed the names of the 10 schools that received a 100% graduation rate and those that had the lowest graduation rate, the higher the class size the more likely a student is to graduate, and a list of the 4 elementary schools that met the passing threshold for 4th grade math. 

This project was my first to use data in Tableau and create a dashboard. If you would like to hear me summarize this project, you can find my Loom video  <a href="https://www.loom.com/share/6573c3b7baf64ee2a45619b407ed0c16?sid=f42bb273-2565-4327-b59a-63999b5964fc">here</a>.
If you have any questions or would like to connect, please reach out to me on <a href="https://www.linkedin.com/in/lexie-langella/">LinkedIn</a>.
