---
layout: post
title: "[Leveraged Finance] Defining Leveraged in Leveraged Finance"
---

{{ page.title }}
================

<p class="meta">July 2024 - Charlotte, NC</p>

A company is regarded as highly leveraged when it has a credit rating of speculative-grade assigned by Credit Rating Agencies. 
The ratings are often assigned using both quantitative measures and qualitative judgments. 

This post provides brief descriptions of two such rating methodologies.   

<br>

## Moody's Credit Ratings

Moody's Investor Service **ranks** the creditworthiness of borrowers using a standardized rating scale from Aaa (the highest quality) to C (the lowest quality). 

These ratings are calculated as a weighted average of factors considered in the Scorecard. Below is a scorecard for Integrated Oil and Gas companies [1].
- at the top, it mainly considers financial metrics such as interest coverage, and balance sheet leverage.
- it also factors in the country's risk and local government policies, which may result in a downgrade adjustment.
- ratings may reflect additional factors that are difficult to quantify or measure, such as the quality and experience of management.

<p align="center">
<img src="/images/posts_2024_07_01/moody_score_card.png" >
</p>

Despite the scorecard factors and their relative importance/weight differ across industries [2], it's helpful to summarize popular financial metrics without regard to industry classification. For instance, the table below presents the medians by broad rating category for global non-financial corporates as of Dec 2016 [3]. In general, the median for these metrics follows a monotonic relationship with ratings.
  
<p align="center">
<img src="/images/posts_2024_07_01/moody_rating_fin.png" >
</p>

A speculative-grade company appears to have  
  * **Balance Sheet Leverage**: Debt / Book_Cap > 46.4%
  * **Operating Leverage**:  Debt / EBITDA > 2.9x
  * **Debt Service Coverage**: EBITA / Interest_Expense < 6.3x, (FFO+Interest_Expense)/Interest_Expense < 8.1x
  * **Free Cash Flow Coverage**: FFO/Debt < 27.1%, Retained_Cash_Flow/Net_Debt < 25.3%  
  * **Profitability**:  EBITA / Avg_Assets < 8.7%, EBITA_Margin < 13.9%, Operating_Margin < 12.0%
  * **Others**:, CapEx / Depreciation < 1.2x, Revenue_volatility > 10.7x


<br>

## Top Investment Banking's Credit Ratings

Large banks also develop internal scorecards that are customized to align with the bank's credit philosophy and strategic objectives. 
One key difference lies in how a bank defines each risk factor and asssess its relative importance. 

Table below illustrates the allocation of weights assigned to risk areas based on the size of borrowers. 
| Risk Area | Large Corp <br> (ann. rev: $750+MM) | Upper Middle Market <br> (ann. rev: $20 ~ 750MM) | Lower Middle Market <br> (ann. rev: <$20MM) | Special Corp  <br> (Sponsored)| 
|----| :---: | :---: | :---: | :---: |
| Leverage    | 35%  | 40%  | 30% | 50%  |
| Coverage    | 40%  | 40%  | 30%  | 50%               |
| Profitability | -  | 15% | 10% | -                |
| Liquidity    | - | 5%  | 30% | - |
| Size    | 25% | - | - | - |

The borrower's size also influences the selection of metrics within each risk area, as does its threshold for highly leveraged borrowers. 

For Large-Corp,   
  * **Leverage**: Total_Debt/Adjusted_EBITDA > 3.75x (35%)
  * **Coverage**: (Net_cash_from_Op-CapEx)/Debt < 17x (25%)
  * **Coverage**: Adjusted_EBITDA/Interest_Expense < 5x (15%)
  * **Size**: net_profit_before_extra_items < $25MM (25%)

For Upper Middle Market, 
  * **Leverage**: Total_debt/Adjusted_EBITDA > 2.50x (20%),
  * **Leverage**: (Total_liabilities-Sub_debt)/(Tangible_net_worth-Sub_debt) > 2.50x (20%)
  * **Coverage**: (Net_income + D&A + Int_Exp +/- Net_distributions) / (CPLTD + CP_Finance_lease + Int_Exp) < 2.49x (20%)
  * **Coverage**: Adjusted_EBITDA / (CPLTD + CP_Finance_lease + Cash_Interest) < 2.75x (10%)
  * **Coverage**: (Adjusted_EBITDA - CapEx - Cash_Div -Cash_Taxes) / (CPLTD + CP_Finance_lease + Cash_Interest) < 1.60x (10%)
  * **Profitability**:  Net_income_before_tax / Total_Assets < 10% (15%)
  * **Liqudity**:, Current_Assets / Current_Liabilites < 2x (5%)

For Middle Market w/ Equity Sponsor, 
  * **Leverage**: (Total_Debt + Finance_Lease) /  Adjusted_EBITDA > 3.25x (40%)
  * **Leverage**: (Senior_Debt + Finance_Lease) /  Adjusted_EBITDA > 2.76x (10%) 
  * **Coverage**: (Adjusted_EBITDA - CapEx - Cash_Taxes) / (Cash_interest + Cash_distribution + 1/14thx(Total_debt+Finance_lease)) < 1.75x  (30%)
  * **Coverage**: Adjusted_EBITDA / Cash_interest < 5x  (20%) 


Likewise, the scorecards consider such qualitative factors as historical trends, management/equity sponsor strength, market position, industry outlook, access to capital markets, and legal/regulatory/operational/reputational risk, which can override the scorecard-induced ratings.  


<br>

## Credit Ratings vs Default Probability

Credit Rating by Moody's Investor Service is to rank creditworthiness, while default probability (e.g., EDF by Moody's Analytics) quantifies credit risk in more precise and timely manner. 
In other words ,credit rating is a relatively coarse measurement of default probability when compared to EDF.

Likewise, S&P global also published its rating-to-default_prob [linkages](https://www.spglobal.com/ratings/en/research/articles/240328-default-transition-and-recovery-2023-annual-global-corporate-default-and-rating-transition-study-13047827)
<br>



**Reference**

[1] Moody's, 2022, [Rating Methodology: Integrated Oil and Gas](https://ratings.moodys.com/api/rmc-documents/393389)

[2] Moody's Investor Service, 2024, [List of Rating Methodologies](https://ratings.moodys.com/documents/PBC_127479)

[3] Moody's Investor Service, 2017 [Moody's Financial Metrics™ Key Ratios
by Rating and Industry for Global Non-
Financial Corporates: December 2016]

