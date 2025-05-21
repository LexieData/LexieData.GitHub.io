<img src="images/The World Bank Project.png?raw=true"/>

# A Rich Topic You Can Truly Bank On

## Introduction
This is my first project using SQL or Structered Query Language. I used SQL to analyze data from the IDA or International Development Association. IDA is a part of the World Bank Group that provides concessional financing, grants, and policy advice to the poorest countries in the world. 

There were **4** queries I answered:
  1. Show all transactions from Nicaragua.
  2. How many total transactions?
  3. How many total transactions per country?
  4. What is the max owed to the IDA?

---
## The Data

The data comes from the World Bank Group website and they update their data quarterly. For this project I was assigned a snippet of this data to query from the year 2022. The live data can be found on this <a href="https://financesone.worldbank.org/ida-statement-of-credits-grants-and-guarantees-historical-data/DS00976">website</a>

In Excel I cleaned the data for any duplicates and then I used <a href="CSVFiddle.io">CSVFiddle.io</a> to practice these SQL queries. 

---
## Analysis: The Vault
My first query was to find all transactions from  **Nicaragua**. I did this by entering the following:
<img src="images/SQL Nicaragua.png?raw=true"/> <br>
From the first few rows that were returned you can also see the status of their credit in the righthand column below:
<img src="images/SQL_Credit.png?raw=true"/>

Next I found out how many total transactions their were by entering this query:
<img src="images/SQL All.png?raw=true"/> <br>
There were a total of **1,048,575** transactions.

Then I found how many transactions each country had by this query:
<img src="images/SQL Country.png?raw=true"/> <br>
Which yeilded **136** countries with their transaction numbers listed. <br>
By using the **GROUP BY** and **ORDER BY** function, you can see the countries that populated in alphabetical order:
<img src="images/SQL Country Breakdown.png?raw=true"/> <br>

The max owed to the IDA was found using this simple query:
<img src="images/SQL MAX.png?raw=true"/> <br> 
**$793,256,127.60** was owed to the IDA at this time. 
To find out which country owed this much to IDA, I did this query:
<img src="images/SQL Due to IDA.png?raw=true"/> <br> 
 I had to **LIMIT** to 12 since the data set is too large for CSVFiddle.
This loan is for the SSA III project or the **"Third Elementary Education Project."** The aim of this project is to improve the quality of education for elementary students in India.

## Final Statement
By using SQL for this snapshot of IDA data, I learned:
  1. How to use SQL functions i.e. **SELECT**ing all transactions for Nicaragua.
  2. There were a total of **1,048,575** transactions.
  3. By using **GROUP BY** and **ORDER BY** I could see the **136** countries and their transactions.
  4. **India** had the largest loan owed to IDA and the loan was for the Third Elementary Education Project.

This project was a beginner exercise to practice SQL queries. With this data I was also taught aggregations such as MAX, MIN, SUM, AVG, and COUNT. I learned the WHERE BY clause and its AND, OR, NOT operators. I am excited to continue learning SQL with other projects! Please reach out via <a href="www.linkedin.com/in/lexie-langella">LinkedIn</a> if you have any questions or want to connect.


