---
layout: post
title: "[MP] Banking Regulations: Capital and Liquidity"
---

{{ page.title }}
================

<p class="meta">July 2022 - Charlotte, NC</p>

"*Stronger regulation and supervision aimed at problems with underwriting practices and lenders' risk management would have been a more effective and surgical approach to constraining the housing bubble than a general increase in interest rates.*"

― **Ben S. Bernanke**, at the 2010 AEA meeting, Atlanta, GA

Why does central bank regulate banks? The answer from Bank of England sheds some light: "*When a bank fails, it can create problems for the wider economy.*"

Two areas are under heavy regulations: capital and liquidity; capital aims to curb the excessive risk-taking behaviors, while liquidity helps reduce the chances of bank runs during the stress periods.

In this post, i will discuss the major regulatory metrics below used to evaluate banks' capital and liquidity situation.

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


# Capital

Capitals are predominantly in the form of equity shares and retained earnings. They are the cushion absorbing losses in the first place.

Capitals are often assessed as a fraction of risky assets. Among many ratios, the CET-1 ratio is the most important.

### *CET-1 Ratio*
CET-1 Ratio is the ratio of common equity tier-1 (CET-1) capital over the risk-weighted assets (RWA).

The required CET-1 ratio could vary for banks with different size and business. JPM, for example, has the advanced CET-1 Ratio of 12.7\% that is 1.2% higher than the required level.

<p align="center">
<a href="https://jpmorganchaseco.gcs-web.com/static-files/81a917bc-b9e1-42e6-bc7d-62ca47190b4a">
  <img src="/images/posts_2022-08-01 /JPM_CET1.png" width="1000">
</a>
</p>


RWA could be calculated using either the standardized method (i.e., a prescribed risk weight schedule by regulators) or the advanced method (e.g., model-based PD by [BofA](https://investor.bankofamerica.com/regulatory-and-other-filings/basel-pillar-3-disclosures))


<p align="center">
<a href="https://jpmorganchaseco.gcs-web.com/node/434316/html">
  <img src="/images/posts_2022-08-01 /required_cet1.png" width="1000">
</a>
</p>

Key components are explained one by one;

1. [G-SIB capital surcharge](https://www.bis.org/bcbs/gsib/index.htm) is additional capital requirement for Global Systemically Important Banks only. It considers many factors including bank's size, interconnectedness, cross-jurisdictional activity, substitutability, complexity, and reliance of short-term wholesale funding.

2. [Stress Capital Buffer (SCB)](https://www.bis.org/review/r190905b.htm) is a concept of the standardized CET-1 ratio. It is a bank-specific buffer based on its four quarters of planned common stocks dividends and the most recent stress test results (i.e., the decrease in risk capital ratio under the severely adverse scenario).

3. [Fixed Capital Conservation Buffer (CCB)](https://www.bis.org/fsi/fsisummaries/b3_capital.htm) is a concept of the advanced CET-1 ratio. It is manually fixed at 2.5% of total risk-weighted assets.

4. [Countercyclical buffer (CCyB)](https://www.bis.org/fsi/fsisummaries/b3_capital.htm) aims to protect the banking sector from periods of excess aggregate credit growth that have often been associated with the build-up of system-wide risks. The CCyB was 0.00% as of March-2022, and can go up to 2.50% at the Fed's discretion.    


### *SLR*
[SLR](https://www.davispolk.com/sites/default/files/09.12.14.Supplementary_Leverage_Ratio.pdf) expands to Tier-1 capital and uses total leverage exposure (i.e., on- and off- balance sheet exposures).

The G-SIB banks must maintain a \> 5% SLR on a consolidated basis. WFC, for example, has a SLR of 6.61%, above the minimum.

<p align="center">
<a href="https://www08.wellsfargomedia.com/assets/pdf/about/investor-relations/basel-disclosures/2022-first-quarter-pillar-3-disclosure.pdf">
  <img src="/images/posts_2022-08-01 /SLR.png" width="1000">
</a>
</p>

### *TLAC*
Shareholders and creditors should bail in before the govt. bails out in the presence of losses. Such bail-in money is called total loss absorbing capacity, and often in the form of Tier-1 capital and unsecured long-term debt.

[TLAC](https://www.bis.org/fsi/fsisummaries/tlac.htm) is scaled by either RWA or total leverage exposure.   

<p align="center">
<a href="https://www08.wellsfargomedia.com/assets/pdf/about/investor-relations/basel-disclosures/2022-first-quarter-pillar-3-disclosure.pdf">
  <img src="/images/posts_2022-08-01 /TLAC.png" width="1000">
</a>
</p>


# Liquidity

The liquidity management often lies within the responsibility of CIO and CFO.

The liquidity risk is about short-term resilience; it's elevated when a bank has difficulty converting its assets easily and quickly to cash in an amount sufficient to survive a significant stress scenario that often last 30 days.

Regulators monitor the liquidity risk via two key metrics; liquidity coverage ratio (LCR) and net stable funding ratio (NSFR).

### *LCR*
The metric measures if there's sufficient HQLA that can cover the net cash outflow over a 30-day stress periods. It is required for big banks that their ratio of HQLA to net cash outflow must be greater or equal to 100%.

High-quality liquid assets are selective b/c they must be easily and immediately converted into cash *at little or no loss of value*. The value of HQLA is measured based on fair value and could be subject to haircuts. For example, Agency MBS appears a safe asset, but it still needs to be weighted in HQLA with haircuts applied to fair value at 15%.

Therefore, the composition of HQLA is deemed as a strategic choice; Different bank appears to have different HQLA composition; looking at [WFC](https://www08.wellsfargomedia.com/assets/pdf/about/investor-relations/lcr-disclosures/2022-second-quarter-lcr-disclosure.pdf) and [JPM](https://jpmorganchaseco.gcs-web.com/static-files/9158e99a-c9a5-41d5-8a10-b0414c0fe0d6). This [article](https://research.stlouisfed.org/publications/review/2019/07/12/how-have-banks-been-managing-the-composition-of-high-quality-liquid-assets) attempts to explain why.


### *NSFR*

[NSFR](https://www.bis.org/bcbs/publ/d295.pdf) extends LCR and exhibits two distinct features;
1. It assesses the funding/liquidity risk over a longer horizon (1 year), rather than a short stress periods lasting 30 days;
2. It deep-dives and differentiate funding sources regarding its tenor (e.g., 10-year debt vs 1-year note) and type (e.g., retail deposits vs wholesale funding).

It's required that the NSFR is greater than or equal to 1, meaning the bank can make ends meet in one year using its available stable funding.
1. Available funding could be bank's capital (i.e., shareholders' equity) and deposits from household and business. Different weights will apply to these funding sources to reflect its stability.
3. On the other side, funding is required to fund various assets (loan, debt, and derivative contracts). Different assets require a stable funding to different extend. Hence, a weighting scheme is also applied to required stable funding for assets.   



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
