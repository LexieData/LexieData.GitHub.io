<img src="images/Billboard Hits.png"/>

# Topping the Charts: A Billboard Artist Analysis

## All Aboard!
Music has been a big part of my life. I have two college degrees in music and my parents work for a music royalites company. Also, losing the heavy metal icon Ozzy Osbourne last week has inspired me to create a music capstone project for my data analytics studies. For this project, I am looking at the top songs on the Billboard Charts throughout the years and I'm hoping to see Ozzy or Black Sabbath in there somewhere! Let's dive deeper.

What I learned from this project was:
  1. The earliest year-end #1 Billboard hit was "The Gypsy" by **The Ink Spots** in 1946 and the latest being "Last Night" by **Morgan Wallen** in 2023.
  2. **The Beatles** were the only band to be on the rank 1, year-end Billboard charts more than once.
  3. **Pop** has become the most popular genre.
  4. **Ozzy Osbourne** showed up as a co-writer on one song but he himself nor **Black Sabbath** ever made the year-end Billboard charts.


## The Data
The data from this project comes from the Harvard Dataverse <a href="https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/KRQMKU">website</a>. This website shows the year-end Billboard annual charts for the United States from 1946-2023. This data includes the Billboard Hot 100 which launched in 1959 and the data prior to that has charts between 30 and 50 song ranking. Usually the Billboard Hot 100 shows the WEEKLY ranked songs but this data set shows the YEAR-END ranked songs which is measured by the combination of sales, streaming, and radio play throughout the year. <br>
This data set contains 7,004 rows and 12 columns, where each row represents a song and the columns contain information like rank, genre, artist, and year. I used **Power BI** to create visualizations using this data and **SQL** and **Excel** to analyze the data. 

## Analysis

I answered **4** questions about the year-end Billboard Charts:
  1. Who was ranked #1 in the charts by the end of each year?
  2. Which artists made the number one spot more than once?
  3. What genres represent the rank #1 songs and how do they change throughout the decades?
  4. Did Ozzy Osbourne and/or Black Sabbath make the Billboard Chart and if so, what was their ranking?


### Track 1
The first question asks: "Who ranked #1 in the charts by the end of each year?" I did this by using 2 SQL queries. <br>
This picture shows the earliest rank 1 songs.

<img src="images/SQL 1 Rank1.png"/> <br>

The Ink Spots had the earliest #1 hit with the song "The Gypsy".

And this picture shows the latest rank 1 songs on the billboard chart.
<img src="images/SQL 1 Rank2.png"/> <br>
Morgan Wallen had the latest #1 hit with the song "Last Night"


### Track 2
The second question is, "Which artists made the number one spot more than once?" I answered this by using the COUNTIF formula in Excel: <br>

<img src="images/Artist Occurances.png"/> <br>
 
I copied that formula for the rest of the artists and found that The Beatles were the only band to be on the rank 1, year-end 1946-2023 Billboard Charts. They were on there two times: in 1964 and 1968.

### Track 3
The third question asks, "What genres represent the rank #1 songs and how do they change throughout the decades?" I answered this by filtering the rank to "1" and comparing the genres in Excel. <br>

<img src="images/Genre Rank1.png"/>
<img src="images/Genre Rank2.png"/>
<img src="images/Genre Rank3.png"/>
<img src="images/Genre Rank4.png"/>

It is interesting to see how music tastes change throughout the years and the combination of genres one song can have like "Jazz/Swing, Indie, R&B" seen in the 1990's. <br>

I counted the genres using the COUNTIF function in Excel and ordered them by most popular at the top. Then I made a bar graph in PowerBI to visualize these results. <br>
<img src="images/PowerBI Genre.png"/> <br>

The most popular genre was Pop, followed by Rock. Pop was listed 41 times, whether it was by itself or with a group of other genres. The genres that ranked 1 the least amount of times were Disco and Funk. Jazz had one hit but was listed once by itself instead of grouped with Swing.

### Track 4
The last question is, "Did Ozzy Osbourne and/or Black Sabbath make the year-end Billboard Chart and if so, what was their ranking?"
I filtered the rows in SQL looking for either artist but sadly neither one was on the charts!

<img src="images/Ozzy Filter.png"/>
I found this hard to believe, so I looked into this further. 
Using Excel I searched for "Ozzy" anywhere in the table and I found this:

<img src="images/Excel Ozzy.png"/>

So Ozzy co-wrote on Lita Ford's song "Close My Eyes Forever". Even though he sang on the song, he wasn't listed as the main artist so he didn't show up on the original artist filter. There is no other mention of Ozzy or Black Sabbath in the year-end Billboard Chart rating. I know they have made the weekly Billboard Hot 100 charts but I learned from this data that they didn't rank high enough those years to land on the year-end chart. I wonder if future data will show Ozzy and Sabbath making it on the year-end Billboard Hot 100 chart for 2025 since it seems that fans have been playing his music more since his passing. 


## See You On the Other Side
I am glad I could use the skills I have learned in the Data Analytics Accelerator to complete this final capstone project for the bootcamp. It was fun to combine music and data analytics!

If you would like to connect, please reach out to me on <a href="https://www.linkedin.com/in/lexie-langella/">LinkedIn</a>! 
