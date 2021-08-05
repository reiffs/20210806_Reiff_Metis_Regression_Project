# 20210806_Reiff_Metis_Regression_Project
_This repo contains project scoping, MVP concepts, and accompanying analytical documentation/findings for the Metis Linear Regression Module commenced Jul 2021_

---
### **Project scope**
* **Background:** Traditional academic finance supposes that markets are at least [weak-form efficient](https://www.investopedia.com/terms/e/efficientmarkethypothesis.asp) (stock prices reflect historical pricing data, but do not always fully reflect public/non-public information relevant to valuation), and many finance/banking professions are predicated on capturing inefficient security pricings, e.g. buying 'undervalued' stocks. Sell-side research analysts at Wall Street firms issue investment research on thousands of publicly traded stocks, publicly communicating their opinions on the investment prospects for individual stocks and sectors, usually including their estimates for financial metrics such as revenue and earnings. My hypothesis is that stocks lacking adequate Wall Street research coverage may have more investing opportunities due to reduced information dissemination. This project serves as a starting point for identifying undercovered stocks for further investing due diligence, with the assumption that an investor with time and skill can make informed investing decisions to generate investing [alpha](https://www.investopedia.com/terms/a/alpha.asp). 
* **Data & implementation:** This analysis will employ a regression model to determine a stock's ideal 'coverage' (number of active publishing sell-side analysts) relative to fundamental size/profitability metrics that are known to drive intrinsic value and investor interest (e.g., revenues, assets, profitability). This regression will serve as a prescriptive analysis of coverage for stocks comprising the [Russell 1000](https://en.wikipedia.org/wiki/Russell_1000_Index) stock index, and will entail the following features:
    * Enterprise Value. Market valuation of the company's total assets. 
    * Market Capitalization. Market valuation of the company's traded equity. 
    * Average Trading Volume. Average number of shares traded daily for the latest 3 months. 
    * Float. Percent of shares actively traded compared to total shares outstanding. 
    * ROA. Return on the company's assets. 
    * ROE. Retrun on the company's equity. 
    * LTM Revenues. Latest twelve months of revenue. 
    * LTM Gross Profit Margin. Gross profit margin, based on LTM P&L. 
    * LTM Operating Profit Margin. Operating profit margin, based on LTM P&L. 
    * LTM EBITDA. Latest twelve months of Earnings Before Interest, Taxes, Depreciation, and Amortization. 
    * LQ Assets. Latest quarter assets. 
* **Tool/technology requirements:** I will scrape company fundamentals and sell-side research coverage metrics from [Yahoo Finance](https://finance.yahoo.com/) using BeautifulSoup, supplement the scraped data with 3 features from the YF API, clean the resulting combined dataframe utilizing Pandas/Numpy, and will conduct the regression analysis with Python's SKlearn. Matplotlib and Seaborn will be used for data visualizations.     
* **Objective(s):** The goal of this analysis is to find a meaningful relationship between desirable fundamental qualities of stocks and their respective coverage (number of publishing analysts). If there is a meaningful relationship, stocks with desirable investment fundamentals but low analyst coverage could be identified as 'underfollowed', and may be identified as candidates for further investing due diligence.      

---
### **Findings/conclusions**
A Ridge regression model outperformed standard linear regression and LASSO regression in cross-validation trials, and performed moderately well on the holdout set with an R^2 value of 0.4598 (MAE of 4.1630). Model performance suggests that there may be limited utility in using it to gauge a company's coverage for pre-due diligence screening. 
