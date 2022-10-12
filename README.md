# Project-1- Canadian Bank Stocks 
## Scope and Purpose of Project
For the purpose of this project, our group wanted to investigate and determine a predictive model for the long term behaviour of relatively stable ETFs. 

The team wanted to understand how this model would react and change due to the unforseen impacts the COVID-19 pandemic had on the Canadian Banks. For this purpose, the timeframe of the model data that the team will be analyzing covers 4 years: August 2016 through July 2020. While the validation data will cover: August 2019 through July 2020 - 6 months before and after the February 2020 COVID-19 crash. Due to this being unforseen and very out of the ordinary, the team will be ignoring the data up until Feb 2020 then picking our analysis back up 6 months post crash. 

Once the group determine the project scope and timeframe of which the data would be derived from, the team then went to work into fidning, cleaning and summarizing the data to then be analyzed to answer our hypothsised questions. 

For the purpose of simplicity during the data analysis, the team created acronyms for each of the areas of which data was pulled from. 

| Data Provider  | Acronym |
| ------------- | ------------- |
| Bank of Montreal  | BMO  |
|  Canadian Imperial Bank of Commerce | CM  |
|  Scotiabank | BNS  |
|  National Bank  | NA  |
|  Royal Bank of Canada | RY  |
|  TD | TD Bank  |
|  BMO Canadian Banks Equal Weight  | [ZEB](https://www.bmogam.com/ca-en/advisors/zeb-bmo-equal-weight-banks-index-etf/)  |
|  BMO Canadian Banks Covered Call |  [ZWB](https://www.bmo.com/gam/ca/advisor/products/etfsfundUrl=/fundProfile/ZWB!hash!holdings#fundUrl=%2FfundProfile%2FZWB%23holdings)  |
|  iShares Government Bonds | IGB  |
|  CAD futures vs USD | CD  |
|  US Dollar Index  | DX  |
|  Crude Oil Futures | CL  |

 The Canadian Bank Stocks consisted of: 
1. Bank of Montreal
2. Scotiabank 
3. Canadian Imperial Bank of Commerce
4. National Bank 
5. Royal Bank of Canada
6. TD Bank

The Canadian Banks ETFs consisted of: 
 1. BMO Canadian Banks Equal Weight: this is an EFT that contains 6 Canadian bank stocks weighted equally based on value. Meaning that an individual could buy $1000 of each of the 6 stocks or $6000 of ZEB and the performance should be about the same.
 3. BMO Canadian Banks Covered Call

The Commodities (Future contracts) consisted of: 
1. iShares Government Bonds
2. CAD futures vs USD
3. US Dollar Index  
4. Crude Oil Futures

From the collection of data, the group then cleaned, formatted the data, using Panadas, to ensure all values utilized in future analyzation was consistent across the board. Nulls, incomplete values, unknown charecters ect were removed from the data sets and all entries were formatted identically to ensure future visulizations would produce a picture that was accurate to the data pulled. The data sets were summarized and generic data statistics were determined. 

Figure 1:
<img width="500" alt="Screen Shot 2022-10-05 at 6 53 21 PM" src="https://user-images.githubusercontent.com/110856988/195225240-d341b401-165c-4aab-8011-d910c46d75f9.png">

Figure 2:
<img width="500" alt="Screen Shot 2022-10-11 at 9 01 34 PM" src="https://user-images.githubusercontent.com/110856988/195225249-6f76e77a-5245-40ed-86de-6d0c59155ad3.png">

From here, the team set off to analyzing the data using the data visualization methods taught in class to answer the groups set of main questions. 

## Questions Findings, Analysis, Conclusions and Implications

*Question 1: What can insights from the first 3 years tell us about the next 3 years?*

From Figure 3, a steady averaged incline in the daily adjusted close on a year over year basis can be found. The BMO Equal Weight Banks Index ETF has been designed to replicate, to the extent possible, the performance of the Solactive Equal Weight Canada Banks Index , net of expenses. The Fund invests in and holds the Constituent Securities of the Index in the same proportion as they are reflected in the Index.
Figure 3: 
<img width="500" alt="Screen Shot 2022-10-11 at 9 00 09 PM" src="https://user-images.githubusercontent.com/110856988/195225305-07d14d4a-9081-46e0-a61c-38fd44ed34ae.png">


*Question 2: Which securities should be bought?*

To determine the answer to this question, the team had to conduct an Monte Carlo simulations produce daily simulated returns for August 2016 - August 2019 as the purchase relies on risk and expected return. The rational into why a Monte Carlo simulation was performed is that determining the statistical properties of these simulation would help to inform which stocks are the best purchases. However, the raw Monte Carlo simulations, as seen below, are messy and the data is somewhat hard to visualize. 

Figure 4: 
<img width="500" alt="Screen Shot 2022-10-11 at 9 03 08 PM" src="https://user-images.githubusercontent.com/110856988/195225395-002bf794-f8e8-4f03-bf4b-7a0b78ea1e6b.png">

Figure 5:
<img width="500" alt="Screen Shot 2022-10-11 at 9 03 22 PM" src="https://user-images.githubusercontent.com/110856988/195225403-72bfec10-4bdb-4bd4-adbd-3a73251e50c5.png">

It was clear that cleaning the data from the simulation would help to get a better understanding of the nature of the Monte Carlo. The following two graphs, line and histogram charts, were  created:

Figure 6:
<img width="500" alt="Screen Shot 2022-10-11 at 9 07 31 PM" src="https://user-images.githubusercontent.com/110856988/195226720-8f85fa3d-5254-449f-9519-054dc8c334dd.png">

Figure 7: 
<img width="500" alt="Screen Shot 2022-10-11 at 9 10 17 PM" src="https://user-images.githubusercontent.com/110856988/195226721-ba0304e7-6c64-43c1-85c7-4b5682e9f086.png">

To provide some context to the charts:

Figure 6, Line plot, represent the mean, two standard deviations and the 95% confidence interval as a function of the trading day. The legend of said plot is as follows: green is the mean, yellow is 1 standard deviation, orange is 2 standard deviations and red is the 95% confidence interval. As such, 95% of all simulation ended between the red lines

Figure 7, the Histogram, shows the distributions of the data after three years.

By comparing these charts, a clearer understanding of the future returns of a given stock or EFT can be summarized to follow the same or similar pattern as exhibited in Figure 5 and 6.  

Clearly, additional data exploration and analyzation had to be conducted to product a suitable answer to this question as risk of each option must be taken into consideration. Aside from standard deviation, summarized in Figure 5, sharpe ratios and Beta calculations are useful tools to determining risk as beta calculated as the movement relative to a stable index, in this case government bonds while sharpe ratios can tell us if a portfolio or stock is acceptable to hold. 

Figure 8: 
<img width="500" alt="Screen Shot 2022-10-11 at 9 10 17 PM" src="https://user-images.githubusercontent.com/110856988/195226113-fcb39d7b-2c3f-4eb6-9971-02a913252e1b.png">

Figure 9:
<img width="500" alt="Screen Shot 2022-10-11 at 9 10 24 PM" src="https://user-images.githubusercontent.com/110856988/195226116-00fb5fa2-7ef4-4fe4-acb6-ddf187bf2a27.png">

Figure 10:
<img width="500" alt="Screen Shot 2022-10-11 at 9 10 31 PM" src="https://user-images.githubusercontent.com/110856988/195226137-6fa70879-4c49-45b6-b500-3826407033c6.png">

From Figure 8 to 10 the team can conclude that:  
- Betas are highly correlated, not particularly useful for distinguishing stocks
- Sharpe ratios favour BNS, ZWB and CM
- NA, TD and RY have highest returns both in historical data and Monte Carlo simulations, but lowest Sharpe due to high volatility
- Monte Carlo predict smallest standard deviation for ZEB and ZWB with average predicted returns making them good choices
- BNS and CM show comparatively poor returns and are more risky than the ETFs, unlikely to be good picks

*Question 3: What is the leading indicator through the use of offsetting?*

Leading Indicators:
Leader is the security that predicts
Target is the security being predicted
p is the number days the Leader precedes the Target

Process:
Calculate the trailing 5 day average return of the Leader
Cycle backwards in time weekly for 6 weeks (30 Days)
Look for correlation to the Target’s 5 day average return 
             
Figure 11:
<img width="500" alt="Screen Shot 2022-10-11 at 9 35 18 PM" src="https://user-images.githubusercontent.com/110856988/195228726-c7a48619-b603-40ad-880d-1b4d4fdd2df2.png">

Figure 12:
<img width="500" alt="Screen Shot 2022-10-11 at 9 35 24 PM" src="https://user-images.githubusercontent.com/110856988/195228731-e513953e-56ac-492d-9e25-f48feb54e0ab.png">

Figure 13:
<img width="500" alt="Screen Shot 2022-10-11 at 9 36 13 PM" src="https://user-images.githubusercontent.com/110856988/195228822-d2af0229-c9f3-49db-9c5b-2eab4e945507.png">

Figure 14:
<img width="500" alt="Screen Shot 2022-10-11 at 9 36 21 PM" src="https://user-images.githubusercontent.com/110856988/195228825-93cf7950-27ca-4b2d-a5f1-ce6ab98fee04.png">

*Question 4: What is the correlation between the data?*

To ensure the team covered the scope of the project at hand, the team had to determine the correlation between the data scrubbed as understanding the correlation between the data would give us a better understanding of the rate at which what data sets change at the same rate (positively or negatively), meaning that they are linerally related. Understanding this will help us to better understand the long term behaviour and thus which securities should be bought. 

To do this however the team utilized a heat mat, presented below both visually and within a table format in Figure 15 and 16. 

Figure 15:
<img width="500" alt="Screen Shot 2022-10-11 at 9 41 51 PM" src="https://user-images.githubusercontent.com/110856988/195229398-30d89a71-5dbe-471c-9412-f99665b537b8.png">

Figure 16:
<img width="500" alt="Screen Shot 2022-10-11 at 9 42 00 PM" src="https://user-images.githubusercontent.com/110856988/195229401-ade41a88-cd2f-4cd1-b8ef-fc85233d8170.png">

*Question 5: Would or does COVID impact your decision?*

!! require visualizations!!

What can additionally be commented on is the psychological nature of a market crash which was caused by the COVID-19 pandemic. The crash was unforseen by many therefor the prepardness of those individuals was not to par to ensure a positive outcome if a crash, as this one occured, did infact occur. Therefor it is clear the pandemic has left many shell shocked into the purchase of stocks, Canadian or not, as many are unsure if or when another crash similar could happen in the future. 

## Connection to Course Content

The connection to the course content is found throughout this project. From participating in class and the activities, the team was able to use our collective knowledge to determine which visualizations would best answers the questions the team hypothesized at the start of this project. To ensure that the team outputted these visualizations the understanding and utilization, taugh through this course, was key through the useage of Pandas. 

## Areas of challenge

Overall there were three main areas of challenge:
1. Ensuring the data required to fufill the scope of the project was avalible for useage. We were warned prior to starting this project that ensuring that we had all data required to fulfill our hypothesis was key to be successful in this project and that this must be done early in the project. So as a team we brainstormed on what data we required and reached out for assistance in obtaning data that we did not have access to. 
2. Our team decided Monte Carlo?
3. Determining which visulizations best answered the questions that we proposed. During the last two months in class we have been introduced to many concepts and ways to present data in a way that can be easily read by anyone. To this then, our team had to review the methods that we were taught with some trial and error to determine which of what we learned best presented the data we collected and cleaned. 

## Usage and Installation instructions

To view this project, follow the main branch found in this Github repo to the final code that encompasses all of the contributions made by the team members. 

The code which is submitted is commented with concise, relevant notes that other developers can understand so future extensions on the work submitted can be explored if needed. 



