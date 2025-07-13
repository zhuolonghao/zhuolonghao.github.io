---
layout: post
title: "[Leveraged Finance] Defining Leveraged in Leveraged Finance"
---

{{ page.title }}
================

<p class="meta">July 2024 - Charlotte, NC</p>

A company is regarded as highly leveraged when it has a credit rating of speculative-grade assigned by Credit Rating Agencies. 
The ratings are often assigned using both quantitative measures and qualitative judgments. 

This post introduces two rating methodologies and explores their connection with probability of default (PD). The focus is on how a leveraged borrower is identified in each method.      

<br>

## Definition
There is no commonly agreed definition for leveraged loans. Based on the survey performed by FSB, these criteria are considered including 1) debt-to-ebitda, 2) credit ratings, 3) loan purpose, 4) presence of a private equity sponsor, and 5) high loan spread.  

<p align="center">
<img height="500"  src="/images/posts_2024_07_01/def_LevFin_data_provider.png" >
</p>

<p align="center">
<img height="500"  src="/images/posts_2024_07_01/def_LevFin_regulators.png" >
</p>

<br>

## Example: Moody's Credit Ratings

Moody's Investor Service **ranks** the creditworthiness of borrowers using a standardized rating scale from Aaa (the highest quality) to C (the lowest quality). 

These ratings are calculated as a weighted average of factors considered in the Scorecard, as illustrated below for Integrated Oil and Gas companies [1].
- At the top, it's a rule-based method that considers financial metrics such as interest coverage, leverage, size, and profitability.
- It also incorporates the country's risk and local government policies, which may result in an adjustment to the initial rating.
- The final rating can be further adjusted due to other considerations such as the management quality and experience.

<p align="center">
<img src="/images/posts_2024_07_01/moody_score_card.png" >
</p>

Despite Moody's scorecards being industry-specific [2], a quick look at all global non-financial corporates by broad rating category reveals the median for selected financials generally follows a monotonic relationship with rating [3]. 
  
<p align="center">
<img src="/images/posts_2024_07_01/moody_rating_fin.png" >
</p>

A speculative-grade company appears to have  
  * **Balance Sheet Leverage**: Debt/Book_Cap > 46.4%
  * **Operating Leverage**: Debt/EBITDA > 2.9x
  * **Debt Service Coverage**: EBITA/Interest_Expense < 6.3x, (FFO+Interest_Expense)/Interest_Expense < 8.1x
  * **Free Cash Flow Coverage**: FFO/Debt < 27.1%, Retained_Cash_Flow/Net_Debt < 25.3%  
  * **Profitability**:  EBITA/Avg_Assets < 8.7%, EBITA_Margin < 13.9%, Operating_Margin < 12.0%
  * **Others**:, CapEx/Depreciation < 1.2x, Revenue_volatility > 10.7x
<br>

## Example: top Investment Banking's Credit Ratings

Likewise, large banks also develop internal scorecards that 1) share many similarities with those of CRAs and 2) align with the banks' credit philosophy and strategic objectives.
For example, banks' scorecards can be segmented by borrowers' size and, within each segment, have different focus on risk areas.
| Risk Area | Large Corp <br> (ann. rev: $750+MM) | Upper Middle Market <br> (ann. rev: $20 ~ 750MM) | Lower Middle Market <br> (ann. rev: <$20MM) | Special Corp  <br> (Sponsored)| 
|----| :---: | :---: | :---: | :---: |
| Leverage    | 35%  | 40%  | 30% | 50%  |
| Coverage    | 40%  | 40%  | 30%  | 50%               |
| Profitability | -  | 15% | 10% | -                |
| Liquidity    | - | 5%  | 30% | - |
| Size    | 25% | - | - | - |

The following further details the metrics and their thresholds for highly leveraged borrowers.

For Large-Corp,   
  * **Leverage**: Total_Debt/Adjusted_EBITDA > 3.75x (35%)
  * **Coverage**: (Net_cash_from_Op-CapEx)/Debt < 17x (25%)
  * **Coverage**: Adjusted_EBITDA/Interest_Expense < 5x (15%)
  * **Size**: net_profit_before_extra_items < $25MM (25%)

For Upper Middle Market, 
  * **Leverage**: Total_debt/Adjusted_EBITDA > 2.50x (20%),
  * **Leverage**: (Total_liabilities-Sub_debt)/(Tangible_net_worth-Sub_debt) > 2.50x (20%)
  * **Coverage**: (Net_income+D&A+Int_Exp+/-Net_distributions)/(CPLTD+CP_Finance_lease+Int_Exp) < 2.49x (20%)
  * **Coverage**: Adjusted_EBITDA/(CPLTD+CP_Finance_lease+Cash_Interest) < 2.75x (10%)
  * **Coverage**: (Adjusted_EBITDA-CapEx-Cash_Div-Cash_Taxes)/(CPLTD+CP_Finance_lease+Cash_Interest) < 1.60x (10%)
  * **Profitability**:  Net_income_before_tax/Total_Assets < 10% (15%)
  * **Liqudity**:, Current_Assets/Current_Liabilites < 2x (5%)

For Middle Market w/ Equity Sponsor, 
  * **Leverage**: (Total_Debt+Finance_Lease)/Adjusted_EBITDA > 3.25x (40%)
  * **Leverage**: (Senior_Debt+Finance_Lease)/Adjusted_EBITDA > 2.76x (10%) 
  * **Coverage**: (Adjusted_EBITDA-CapEx-Cash_Taxes)/(Cash_interest+Cash_distribution+1/14thx(Total_debt+Finance_lease)) < 1.75x  (30%)
  * **Coverage**: Adjusted_EBITDA/Cash_interest < 5x  (20%) 

These scorecards also consider such qualitative factors as historical trends, management/equity sponsor strength, market position, industry outlook, access to capital markets, and legal/regulatory/operational/reputational risk, which can override the scorecard-induced ratings.  

<br>

## Credit Rating != Default Probability

Credit rating and default probability are often considered twin concepts with nontrivial nuances: 
- Credit ratings are over-the-time ratings for ranking the creditworthiness of borrowers.
- Default probabilities are point-in-time forecasts of default likelihood.

Therefore, Default probabilities provide more timely and detailed information than credit ratings: 
- **Across different ratings within a given year, a higher rating tends to have a lower default probability, and**
- **For a given rating, the default probability can fluctuate from year to year, and**
- **The same rating category from different CRAs can have different default probabilities** 

Annual and cumulative default rates are useful and reported by CRAs:
- S&P Global's research [4] shows the *annual default rates* for BB (CCC) are 0.00% (29.61%) in 2019, 0.94% (47.88%)  in 2020, 0.00% (10.99%)  in 2021, and 0.32% (13.84%) in 2022.
- Moody's Investor Service [5] publishes the *cumulative default rates* based on history from 1970 to 2022.  
  <p align="center">
  <img src="/images/posts_2024_07_01/moody_cum_pd.png" >
  </p>

In short, credit ratings are more relevant to credit underwriting and investment decision-making, while default probabilities are more important to portfolio management. 
<br>


**Reference**

[1] Moody's, 2022, [Rating Methodology: Integrated Oil and Gas](https://ratings.moodys.com/api/rmc-documents/393389)

[2] Moody's Investor Service, 2024, [List of Rating Methodologies](https://ratings.moodys.com/documents/PBC_127479)

[3] Moody's Investor Service, 2017 [Moody's Financial Metrics™ Key Ratios
by Rating and Industry for Global Non-
Financial Corporates: December 2016]

[4] S&P Global, 2024, [Default, Transition, and Recovery: 2023 Annual Global Corporate Default And Rating Transition Study](https://www.spglobal.com/ratings/en/research/articles/240328-default-transition-and-recovery-2023-annual-global-corporate-default-and-rating-transition-study-13047827)

[5] Moody's Investor Service, 2017 [US municipal bond defaults and recoveries, 1970-2022](https://www.fidelity.com/bin-public/060_www_fidelity_com/documents/fixed-income/moodys-investors-service-data-report-us-municipal-bond.pdf)
