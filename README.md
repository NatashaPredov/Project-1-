# Project-1- Canadian Bank Stocks 
## Scope and Purpose of Project
For the purpose of this project, our group wanted to investigate and determine a predictive model for the long term behaviour of relatively stable ETFs. 

We wanted to understand how this model would react and change due to the unforseen impacts the COVID-19 pandemic had on the Canadian Banks. For this purpose, the timeframe of the model data that we will be analyzing covers 4 years: August 2016 through July 2020. While the validation data will cover: August 2019 through July 2020 - 6 months before and after the February 2020 COVID-19 crash. Due to this being unforseen and very out of the ordinary, we will be ignoring the data up until Feb 2020 then picking our analysis back up 6 months post crash. 

Once the group determine the project scope and timeframe of which the data would be derived from, we then went to work into fidning, cleaning and summarizing the data to then be analyzed to answer our hypothsised questions. 

For the purpose of simplicity during the data analysis, we created acronyms for each of the areas of which data was pulled from. 

| Data Provider  | Acronym |
| ------------- | ------------- |
| Bank of Montreal  | BMO  |
|  Canadian Imperial Bank of Commerce |   |
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
1.  Bank of Montreal
2. Scotiabank 
3. Canadian Imperial Bank of Commerce
4.  National Bank 
5. Royal Bank of Canada
6.  TD Bank

The Canadian Banks ETFs consisted of: 
 1. BMO Canadian Banks Equal Weight
 2. BMO Canadian Banks Covered Call

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

<img width="500" alt="Screen Shot 2022-10-11 at 9 00 09 PM" src="https://user-images.githubusercontent.com/110856988/195225305-07d14d4a-9081-46e0-a61c-38fd44ed34ae.png">

*Question 2: Which securities should be bought?*

To determine this question, the team had to conduct an Monte Carlo simulations produce daily simulated returns for August 2016 - August 2019 as the purchase relies on risk and expected return. The rational into why a Monte Carlo simulation was performed is that determining the statistical properties of these simulation help to inform which stocks are the best purchases. However, the raw Monte Carlo simulations, as seen below, are messy and the data is somewhat hard to visualize. 

Figure 3: 
<img width="500" alt="Screen Shot 2022-10-11 at 9 03 08 PM" src="https://user-images.githubusercontent.com/110856988/195225395-002bf794-f8e8-4f03-bf4b-7a0b78ea1e6b.png">

Figure 4:
<img width="500" alt="Screen Shot 2022-10-11 at 9 03 22 PM" src="https://user-images.githubusercontent.com/110856988/195225403-72bfec10-4bdb-4bd4-adbd-3a73251e50c5.png">

It was clear that cleaning the data from the simulation would help to get a better understanding of the nature of the Monte Carlo. The following two graphs, line and histogram charts, were  created:

Figure 5:
<img width="500" alt="Screen Shot 2022-10-11 at 9 07 31 PM" src="https://user-images.githubusercontent.com/110856988/195226720-8f85fa3d-5254-449f-9519-054dc8c334dd.png">

Figure 6: 
<img width="500" alt="Screen Shot 2022-10-11 at 9 10 17 PM" src="https://user-images.githubusercontent.com/110856988/195226721-ba0304e7-6c64-43c1-85c7-4b5682e9f086.png">

To provide some context to the charts:

Figure 5, Line plot, represent the mean, two standard deviations and the 95% confidence interval as a function of the trading day. The legend of said plot is as follows: green is the mean, yellow is 1 standard deviation, orange is 2 standard deviations and red is the 95% confidence interval. As such, 95% of all simulation ended between the red lines

Figure 6, the Histogram, shows the distributions of the data after three years.

By comparing these charts it is possible to get a better understanding of the future returns of a given stock or ETF. 

Clearly, additional data exploration and analyzation had to be conducted to product a suitable answer to this question as risk of each option must be taken into consideration. Aside from standard deviation, which was summarized above for the data sets, sharpe ratios and Beta calculations are useful tools to determining risk. 

Beta calculated as the movement relative to a stable index, in this case government bonds
Betas are highly correlated, not particularly useful for distinguishing stocks
Sharpe ratios favour BNS, ZWB and CM
NA, TD and RY have highest returns both in historical data and Monte Carlo simulations, but lowest Sharpe due to high volatility
Monte Carlo predict smallest standard deviation for ZEB and ZWB with average predicted returns making them good choices
BNS and CM show comparatively poor returns and are more risky than the ETFs, unlikely to be good picks

Figure 7: 
<img width="188" alt="Screen Shot 2022-10-11 at 9 10 17 PM" src="https://user-images.githubusercontent.com/110856988/195226113-fcb39d7b-2c3f-4eb6-9971-02a913252e1b.png">

Figure 8:
<img width="237" alt="Screen Shot 2022-10-11 at 9 10 24 PM" src="https://user-images.githubusercontent.com/110856988/195226116-00fb5fa2-7ef4-4fe4-acb6-ddf187bf2a27.png">

Figure 9:
<img width="239" alt="Screen Shot 2022-10-11 at 9 10 31 PM" src="https://user-images.githubusercontent.com/110856988/195226137-6fa70879-4c49-45b6-b500-3826407033c6.png">

Question 3: What is the leading indicator through the use of offsetting?

Question 4: What is the correlation between the data?

Question 5: Would or does COVID impact your decision?

## Connection to Course Content

## Areas of challenge

## Usage and installation instructions

## 

