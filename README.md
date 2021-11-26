# IPOs_Worth_the_Hype?

For project 1, our group chose to do an analysis of IPOs over the last decade. Our goal was to find, process, and assess data on these events and the subsequent performance of the securities. There are hundreds or even thousands of IPOs each year, and some of them garner massive amounts of public attention. We wanted to determine whether IPOs are worth the hype they receive, or if retail investors would do better to simply invest in an index, like the S&P 500.

We began with a csv file containing IPO data from 1996 to 2018. We decided to just focus on the last 10 years (since 2011), and since we were determining whether IPOs are generally worth the hype, we chose initial trading volume as a determiner for our sample set. In the file ***csv_reader.ipynb***, we pared it down from thousands of columns to fewer than 10, and then filtered the content to produce a dataframe that displayed only the top 10 IPOs by initial trading volume (w/in the first month) per year.

![1](/images/01.png)

![2](/images/02.png)

![3](/images/03.png)

![4](/images/04.png)

![5](/images/05.png)

![6](/images/06.png)

![7](/images/07.png)

![8](/images/08.png)

![9](/images/09.png)

To get the data for 2019-2021, we located a website that contained all of the IPOs from that time period, used file ***ipo's_2019-2021.ipynb*** to copy the data into a csv file and similarly pared it down to provide us with our needed samples. We were planning to use API calls to gather performance data on our sample set, but the returned data was incomplete and we thus had to pull the data on each security one-by-one from Yahoo Finance in csv format and create the aggregated files in excel.

![15](/images/15.png)
![16](/images/16.png)
![17](/images/17.png)
![18](/images/18.png)

Having gathered our data and condensed it into the required format, we ran a number of analyses on it. In the file ***api_calls.ipynb***, we made Alpaca API calls for ticker 'SPY' to represent the S&P 500, but encountered the same data gaps even for this ticker so used Yahoo Finance csv's again for all years prior to 2018 (where the data was incomplete). We created files and made the api calls starting at the beginning of each year, with every end date as 7/19/2021. We ran these for each year to provide comparable cumulative return data for the samples that went public that year, which we showed with line plots, and compared standard deviation with box plots to compare volatility.

We also ran some additional code to find out top IPO volume by year and performance by sector in ***final_csv_filter*** and ***top_ipo_by_sector***, respectively. All of our analysis led us to the conclusion that although a few of the top IPOs outperformed the S&P 500, most did approximately the same or worse, and with much higher levels of risk. And because this analysis was only run on the sample set of top IPOs by initial trading volume each year (for which we could obtain data), there are thousands more in the full population to consider. Assuming the sample set generally reflects the population, the odds of choosing a correct IPO or building a portfolio of them that outperforms the S&P 500 is highly unlikely, and the amount of risk you would be taking on to do so is vastly greater than simply emulating the market. From our project, it is our recommendation that retail investors ought to primarily invest in stable market-tracking securities and only commit a small portion of it to these IPOs.
