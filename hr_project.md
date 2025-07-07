<img src="images/Massachusetts Education Overview.png"/>

# Driven to Attrition

There are many reasons why employees leave a company. Finding out why employees leave can help a company reduce the cost of training new employees, increase employee satisfaction/retention rate, and improve efficiency and productivty by having a stable workforce.

For this guided project, I analyzed fictional people data from IBM by pretending to be an intern for IBM's Human Resources department. The boss wants to know why people are leaving the company aka the company's attrition. 

I learned 4 things: <br>
  1. The strongest positive correlation was between **monthly income** and **total working years** <br>
  2. How to create a **pairplot** to show correlations between company demographics. <br>
  3. A **box and whisker plot** showed the average age an employee left the company was **33** years old. <br>
  4. By creating a **linear regression model**, a person’s age and total years worked at this company explains around **60%** of the variance in people’s monthly income.

## The Data
This data set comes from Kaggle and can be found<a href="https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset">here</a>. 
There are 1,470 rows of data and each row is an employee. There are 35 columns of data that describe each employee, including the most important column for the project: "Attrition".  
I uploaded the data set into RStudio and used R coding to glean insights and visualize the data.

The boss had four tasks/questions:
  1. How do the most important demographics correlate?
  2. Create a pairplot to show this correlation.
  3. Use data to dispute a claim that the older employees were let go at a higher rate than the younger folks.
  4. Create a linear regression model that predicts the monthly income based upon age and total working years.

## Analysis
### Task 1
The company wants to get an overview of how some of the most important demographics correlate. I did this by creating a correlation matrix.

<img src="images/R Correlation1.png?raw=true"/>
<img src="images/R Correlation2.png?raw=true"/>
<img src="images/R Correlation3.png?raw=true"/>
The four highest correlations found are: there is a fairly strong positive correlation (.77) between monthly income and total working years, a fairly strong positive correlation (.68) between age and total working years, a moderately positive correlation (.49) between monthly income and age, and a low correlation (.30) between number of companies worked and age Monthly Income – Total Working Year (.77) <br>

### Task 2
The boss wants to see a visual of the top four correlations. I did this by creating a pairplot:

<img src="images/R Pairplot.png?raw=true"/>

This pairplot is represented as scatter plots that compare two variables at a time. From this pairplot I see that the older you get, the more time you spend working.

### Task 3
The Secretary of Education believes math scores are an indication of a school's success rate. So by looking at math scores from the 4th grade, we can see which schools' teaching methods are successful and which need more work.

<img src="images/School 4th Grade.png?raw=true"/>

The passing threshold percentage of averaged math scores is 50% so as this line graph shows, there were only 4 schools that met the criteria. It would be interesting to see which of these 4 elementary schools feed into middle schools and eventually high schools. Do these elementary schools with the higher math scores have the same students who eventually attend the high schools that have the highest graduation percentage?

### Takeaways

From this data, I answered three questions: which schools are struggling the most, how does class size effect college admission, and what are the top math schools in the state. My Tableau dashboard showed the names of the 10 schools that received a 100% graduation rate and those that had the lowest graduation rate, the higher the class size the more likely a student is to graduate, and a list of the 4 elementary schools that met the passing threshold for 4th grade math. 

This project was my first to use data in Tableau and create a dashboard. If you would like to hear me summarize this project, you can find my Loom video  <a href="https://www.loom.com/share/6573c3b7baf64ee2a45619b407ed0c16?sid=f42bb273-2565-4327-b59a-63999b5964fc">here</a>.
If you have any questions or would like to connect, please reach out to me on <a href="https://www.linkedin.com/in/lexie-langella/">LinkedIn</a>.
