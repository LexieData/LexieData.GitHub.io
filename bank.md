<img src="images/The Finance Project.png?raw=true"/>

# A Rich Topic You Can Truly Bank On

## Introduction
This is my first project using SQL or Structered Query Language. I used SQL to analyze data from the IDA or International Development Association. IDA is a part of the World Bank Group that provides concessional financing, grants, and policy advice to the poorest countries in the world. 

There were **6** queries I answered:
  1. Show all transactions from Nicaragua.
  2. How many total transactions?
  3. How many total transactions per country?
  4. What is the max owed to the IDA?
  5. Which was the most recent pay?
  6. Who has the most loans?

---
## The Data
I used <a href="CSVFiddle.io">CSVFiddle.io</a> which is a website used to practice SQL queries. 
The data comes from the World Bank Group website and updates their data quarterly. For this project I was assigned a snippet of this data to query from the year 2022. The live data can be found on this <a href="https://financesone.worldbank.org/ida-statement-of-credits-grants-and-guarantees-historical-data/DS00976">website</a>

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
By using the **GROUP BY** and **ORDER BY** function, you can see the first **12** countries that populated in alphabetical order:
<img src="images/SQL Country Breakdown.png?raw=true"/>

The max owed to the IDA was found using this simple query:
<img src="images/SQL MAX.png?raw=true"/> <br> 
**$793,256,127.60** was owed to the IDA at this time. Wow!


By using this query below I found that India has the most loans, oweing 793256127.6 to IDA. I had to LIMIT to 12 since the data set is too large for CSVFiddle.
<img src="images/SQL MAX.png?raw=true"/> <br> 
This loan is for the SSA III project or the "Third Elementary Education Project." The aim of this project is to improve the quality of education for elementary students in India.


