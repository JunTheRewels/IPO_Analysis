# IPOs_Worth_the_Hype?

For project 1, our group chose to do an analysis of IPOs over the last decade. Our goal was to find, process, and assess data on these events and the subsequent performance of the securities. There are hundreds or even thousands of IPOs each year, and some of them garner massive amounts of public attention. We wanted to determine whether IPOs are worth the hype they receive, or if retail investors would do better to simply invest in an index, like the S&P 500.

We began with a csv file containing IPO data from 1996 to 2018. We decided to just focus on the last 10 years (since 2011), and since we were determining whether IPOs are generally worth the hype, we chose initial trading volume as a determiner for our sample set. We used pandas to read the csv and pare it down from thousands of columns to fewer than 10, and then filtered the content to produce a dataframe that displayed only the top 10 IPOs by initial trading volume (w/in the first month) per year.To get the data for 2019-2021, we located a website that contained all of the IPOs from that time period, copied the data into a csv file and similarly pared it down to provide us with our needed samples. We were planning to use API calls to gather performance data on our sample set, but the returned data was incomplete and we thus had to pull the data on each security one-by-one from Yahoo Finance in csv format and create the aggregated files in excel.

Having gathered our data and condensed it into the required format, we ran a number of analyses on it. In the file 'api_calls.ipynb', we made Alpaca API calls for ticker 'SPY' to represent the S&P 500, but encountered the same data gaps even for this ticker so used Yahoo Finance csv's again for all years prior to 2018 (where the data was incomplete). We created files and made the api calls starting at the beginning of each year, with every end date as 7/19/2021. We ran these for each year to provide comparable cumulative return data for the samples that went public that year, which we showed with line plots, and compared standard deviation with box plots to compare volatility.
