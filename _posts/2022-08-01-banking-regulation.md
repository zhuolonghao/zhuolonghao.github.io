---
layout: post
title: "[MP] Banking Regulations: Capital and Liquidity"
---

{{ page.title }}
================

<p class="meta">July 2022 - Charlotte, NC</p>

"*Stronger regulation and supervision aimed at problems with underwriting practices and lenders' risk management would have been a more effective and surgical approach to constraining the housing bubble than a general increase in interest rates.*"

― **Ben S. Bernanke**, at the 2010 AEA meeting, Atlanta, GA

The Federal Reserve influences the macroeconomics through its conventional monetary policies (e.g., FFT) as well as unconventional measures (e.g., QE and QT). Apart from these tools, the Fed also exerts regulations on the banking industry as an response to the 2008's crisis. As Bank of England explained why central bank regulates banks, it said "When a bank fails, it can create problems for the wider economy."

Currently, the focuses are to ensure capital adequacy and improve liquidity position; the former aims to curb the excessive risk-taking behaviors, while the latter helps reduce the chances of bank runs during the stress periods. In this post, i will discuss the major regulatory metrics below used to evaluate banks' capital and liquidity situation.

$$
\begin{split}
\text{Common Equity Tier-1 Ratio} \quad &= \quad \frac{\text{Common Equity Tier-1 Capital}}{\text{Risk Weighted Assets}} \\
\\
\text{Supplementary Leverage Ratio} \quad &= \quad \frac{\text{Tier 1 Capital}}{\text{Total Leverage Exposure}} \\
\\
\text{Total Loss Absorbing Capacity, ver. 1} \quad &= \quad \frac{\text{Tier 1 Capital + Unsecured LT Debt}}{\text{Risk Weighted Assets}} \\
\\
\text{Total Loss Absorbing Capacity, ver. 2} \quad &= \quad \frac{\text{Tier 1 Capital + Unsecured LT Debt}}{\text{Total Leverage Exposure}} \\
\\
\text{Liquidity Coverage Ratio} \quad &= \quad \frac{\text{High-Quality Liquid Assets}}{\text{Net Cash Outflow Over The Next 30 Days}} \\
\\
\text{Net Stable Funding Ratio} \quad &= \quad \frac{\text{Available Amount Of Stable Funding}}{\text{Required Amount of Stable Funding}} \\
\end{split}
$$


## Capital

Capitals are predominantly in the form of equity shares and retained earnings that can absorb losses in the first place.

The 2007-09 Great Financial Crisis prompted a series of reforms in defining/refining the capital requirement for banks; known as the regulatory capital. It is the amount of capital that a bank has to have maintained, and often expressed as the ratio of equity as a percentage of risk-weighted assets.

### *CET-1 Ratio*
The most important capital adequacy ratio is the CET-1 Ratio, the ratio of common equity tier-1 capital over the risk-weighted assets (RWA). RWA could be calculated in two ways, depending on the use of a prescribed risk weight schedule by regulators (i.e., standardized) or the use of internal rating system (i.e., advanced). 

JPM, for example, has the advanced CET-1 Ratio of 12.7\% that is 1.2% higher than the required level.

<p align="center">
<a href="https://jpmorganchaseco.gcs-web.com/static-files/81a917bc-b9e1-42e6-bc7d-62ca47190b4a">
  <img src="/images/posts_2022-08-01 /JPM_CET1.png" width="1000">
</a>
</p>

It's interesting to know a few things about internal risk rating system;

1. Different types of risk rating methodologies may co-exist for a bank. Bank of America, for example, [recognized publicly](https://investor.bankofamerica.com/regulatory-and-other-filings/basel-pillar-3-disclosures) that they are using 1) internally developed scorecards, 2) external mappings, and 3) judgmental approach at the same time.

2. PD is an through-the-cycle (TTC) estimate of the probability that an obligor will default over a one-year horizon, EAD is an point-in-time (PIT) estimate of the amount that would be owed to the bank if the obligor were to default, and LGD is also an PIT estimate of the portion of the EAD that would be lost in a stressed environment with high default rates.    

<p align="center">
<a href="https://jpmorganchaseco.gcs-web.com/node/434316/html">
  <img src="/images/posts_2022-08-01 /required_cet1.png">
</a>
</p>

Key components in the required capital are explained below;

1. [G-SIB capital surcharge](https://www.bis.org/bcbs/gsib/index.htm) is the greater of 1) the value considering the bank's size, interconnectedness, cross-jurisdictional activity, substitutability, and complexity, and 2) similar inputs but replaces substitutability with use of short-term wholesale funding.

2. [Stress Capital Buffer (SCB)](https://www.bis.org/review/r190905b.htm) is a concept only for the standardized CET-1 ratio. It is a bank-specific buffer based on its most recent stress test results (i.e., the decrease in risk capital ratio under the severely adverse scenario), plus four quarters of planned common stocks dividends.

3. [Capital Conservation Buffer (CCB)](https://www.bis.org/fsi/fsisummaries/b3_capital.htm) is a concept only for the advanced CET-1 ratio, and set at 2.5% of total risk-weighted assets. It should be regarded as an additional layer of usable capital that can be drawn down when losses are incurred.

4. [Countercyclical buffer (CCyB)](https://www.bis.org/fsi/fsisummaries/b3_capital.htm) aims to protect the banking sector from periods of excess aggregate credit growth that have often been associated with the build-up of system-wide risks. The CCyB was 0.00% as of March-2022, and can go up to 2.50% at the Fed's discretion.    


### *SLR*

### *TLAC*

## Liquidity

### *LCR*

### *NSFR*




**Reference**

[1] SEC Sue Reserve Primary Fund, 2011 [Lawsuit](https://www.sec.gov/spotlight/reserve_primary_fund_investors/gardephe_opinion.pdf)

[2] Bogglehead, ["The_2008_money_market_crisis"](https://www.bogleheads.org/wiki/The_2008_money_market_crisis)

[3] Kacperczyk and Schnabl, 2010, ['When Safe Proved Risky: Commercial Paper during the Financial Crisis of 2007–2009'](https://pubs.aeaweb.org/doi/pdfplus/10.1257/jep.24.1.29)

[4] The Editors, 2011, [Bloomberg's Opinion](https://www.bloomberg.com/opinion/articles/2011-12-23/money-market-mutual-funds-that-break-the-buck-can-become-a-memory-view)

[5] President Working Group, 2020, [Overview of Recent Events and Potential Reform
Options for Money Market Funds](https://home.treasury.gov/system/files/136/PWG-MMF-report-final-Dec-2020.pdf)

[6] Liberty Street Economics, 2022, [How the Fed’s Overnight Reverse Repo Facility Works](https://libertystreeteconomics.newyorkfed.org/2022/01/how-the-feds-overnight-reverse-repo-facility-works/)

[7] Board of Federal Reserve, [January 2019 FOMC meeting](https://www.federalreserve.gov/monetarypolicy/policy-normalization-discussions-communications-history.htm)

[8] Ben Bernanke, 2016, [Should the Fed keep its balance sheet large?](https://www.brookings.edu/blog/ben-bernanke/2016/09/02/should-the-fed-keep-its-balance-sheet-large/)
