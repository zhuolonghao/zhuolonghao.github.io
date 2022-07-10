---
layout: post
title: "[MP] Shadow Banking: Money Market Funds and Monetary Policy"
---

{{ page.title }}
================

<p class="meta">June 2022 - Charlotte, NC</p>

In this post, let's look at money market mutual funds (MMFs) and its role in the Fed's ["Balance Sheet Normarlization"](https://www.federalreserve.gov/monetarypolicy/policy-normalization-discussions-communications-history.htm).


## What Is Money Market Fund(MMF)?

A MMF is a kind of mutual fund that
- issues shares to retail and institutional investors.  
- invests in short-term (often < 1 year) assets such as US Treasuries and commercial papers.

[Fidelity Money Market Fund](https://fundresearch.fidelity.com/mutual-funds/summary/31617H201), for example, holds assets in commercial papers (26.43%, combined), certificate of deposit (22.88%), Repo (19.16%) and etc, as of April-2022.

<p align="center">
<a href="https://fundresearch.fidelity.com/mutual-funds/composition/31617H201">
  <img src="/images/posts_2022-07-01/one_mmmf.png" width="300">
</a>
</p>

The portfolio composition is subject to change at the discretion of the fund managers. For instance, one year earlier, the fund invested more in risker CP (41.2%) and less in low-yield CDs (12.7%), as a result of benign economic environment and low market volatility.

## Money Market Fund Industry

Now, let's turn to the whole MMFs industry and how its composition evolves over the time.  

<p align="center">
<a href="https://fred.stlouisfed.org/graph/?g=Pgow">
  <img src="/images/posts_2022-07-01/MMMF.png">
</a>
</p>

Like other financial institutions(FI), the 2008 GFC has fundamentally changed the MMF industry.
- The share of risky assets decreased significantly post 2008.  
- Safe assets like US Treasury and Agency securities are the lion's share today.    

One key event that has a profound influence on the industry is the unprecedented collapse of the Reserve Primary Fund in 2008.

### <ins>Reserve Primary Fund and two Reforms</ins>

* On Sunday, September 14, the Reserve Primary Fund held debt securities (mainly CPs) issued by Lehman Brothers with a face value of $785 million[1][2].
* On Monday, September 15, Lehman announced it had filed for bankruptcy protection. In response to this annoucement, on the same day, the Fund faced a tidal wave of redemption requests.
* On Tuesday, September 16, the Fund announced that it had broken the 1.00 net asset value mark (aka, break the buck) and was now valued at 0.97, a new NAV that attributed a zero value to the Lehman holdings[1][2]. On the same day, the $62.5 billion dollar fund was forced to pay out $10.8 billion in redemptions and faced about $28 billion of further withdrawal requests[3].
* In the next two weeks, the run quickly spread to other money funds, who had to seek sponsor support by means of either capital infusion or purchase of discounted paper at book value, during this period. Still, $400 billion was pulled out of the funds, and flow of short-term credit from the funds to companies froze [4].

The SEC has implemented a number of reforms over the past decade aimed at making MMFs more resilient to credit and liquidity stresses and addressing structural vulnerabilities in MMFs that were evident in the 2008 financial crisis, particularly the substantial reforms the SEC adopted in 2010 and 2014.

On February 23, 2010, the SEC adopted three amendments to rule 2a-7 which governs money market funds. The rules were effective from June 30, 2010 onwards.

1. To address credit risks, a new 120-day limit on funds’ portfolio weighted average life (WAL) to limit
exposure to credit spreads, as well as a reduction in the limit on funds’ portfolio weighted average maturity (WAM) from 90 days to 60 days to limit interest rate risk[2][5].
2. Liquidity buffers are introduced for taxable money market funds (a minimum 10% of assets must be cash, treasury securities, or securities that convert to cash in one day; a minimum 30% of assets must be cash, treasury securities or certain government securities with remaining maturities of 60 days or less, or securities that convert to cash within one week.)[2]
3. Tighter restrictions on the amount of higher risk second-tier securities a money fund can hold (now a maximum limit of 3% from the former limit of 5%; and a maximum limit of 0.5% to any single issuer, from a prior limit of 1%.) Investment in second tier securities is restricted to maturities of 45 days or less.[2]

On July 14, 2014 the SEC issued final rules that were effective from October 14, 2016 onwards.

1. adopt a floating net asset value (NAV) for institutional prime money market funds
2. provide non-government money market fund boards new tools – liquidity fees and redemption gates – to address runs.

    1. a liquidity fee $$$ may be levied (i.e. investors might be required to pay a fee if they redeem shares during this time).
    2. a redemption gate may be implemented to limit redemptions in a fund for a short period of time (up to 15 business days in a 90-day period).


### <ins>MMFs and Fed's Reverse Repo</ins>

Overnight Reverse Repo (RRP) is employed by Fed to drain excess liquidity from MMFs.

In concept, the ON RRP facility acts like interest on reserve balances (IORB) rate for a set of [nonbank money market participants](https://www.newyorkfed.org/markets/rrp_counterparties). That is, the Fed offers a broad range of financial institutions that are ineligible to earn IORB, an alternative risk-free investment option. *Together, the IORB rate and the ON RRP set a floor under overnight rates, beneath which banks and non-bank financial institutions should be unwilling to invest funds in private markets*.[6]

## Money Market Funds and "Balance Sheet Normalization"

[The financial crisis of 2008](https://en.wikipedia.org/wiki/Financial_crisis_of_2007%E2%80%932008) and [the COVID-19 recession](https://en.wikipedia.org/wiki/COVID-19_recession) in 2020 had forced the Federal Reserve to purchase large quantities of financial assets, known as "Quantitative Easing" or [QE](https://www.visualcapitalist.com/the-feds-balance-sheet-the-other-exponential-curve/). This expansionary monetary policy has expanded the Fed’s balance sheet from less than $900 billion before 2008 to about $8.9 trillion as of May, 2022; The majority is US Treasuries of $5.7 trillion, followed by the agency mortgage-backed securities of $2.7 trillion.

In the meantime, there're ongoing efforts to keep the Fed's balance sheet as lean as possible, beginning in January, 2014, known as [tapering](https://advisor.visualcapitalist.com/a-visual-introduction-to-fed-tapering/).


<p align="center">
<a href="https://fred.stlouisfed.org/graph/?g=PrBp">
  <img src="/images/posts_2022-07-01/fed_balance.png">
</a>
</p>

### <ins>What is the long-run optimal size of its balance sheet?</ins>

What we know today is that Fed decides to continue to implement monetary policy in a regime with an ample supply of reserves[7]. What we didn't know is how large should the Fed's balance sheet be?

Not long ago, Fed was ev  en debating two options:

1. shrink the balance sheet to the pre-2008 level, and control short-term rates through the supply of reserve.

2. keep the balance sheet reasonably large, and control the short-term rates through the Fed's administered rates (e.g., IOER for banks and ON RRP for MMFs).

This [article](https://www.frbsf.org/economic-research/wp-content/uploads/sites/4/el2019-16.pdf) explains the different channel through which the monetary policies affect/control the short term rates. In short, the Option 1 is to use Quantity to affect Price, while the Option 2 it to use one Price to affect another Price.

<p align="center">
<a href="https://fundresearch.fidelity.com/mutual-funds/composition/31617H201">
  <img src="/images/posts_2022-07-01/fed_balance_sheet.png">
</a>
</p>

[This](https://www.brookings.edu/blog/ben-bernanke/2016/09/02/should-the-fed-keep-its-balance-sheet-large/) and [this](https://www.sipa.columbia.edu/sites/default/files/greenwood_final.pdf) articulate the rationales of why the option 2 should be preferred, including

- [+] There is a strong demand from the private sector for safe, liquid, short-term securities.
  - The Govt. short-term claims (US Bills and Notes) should crowd out private-sector-created short claims (e.g., CP and ABCP). Doing so would make the Fed take on more fiscal (interest-rate) risks.
- [+] Only banks can earn interest on reserves (i.e., IOER).
  - Fed should use Reverse Repurchase (RRP) facility should be used to control the short-term rate MMFs earn.
- [+] Fed can better handle bank runs and/or MMF runs as a lender of last resort.
  - The incentive to insufficient liquidity management in private sector could be curbed by regulations such as Liquidity Coverage Ratio ([LCR](https://www.bis.org/fsi/fsisummaries/lcr.htm)) and Net stable funding ratio([NSFS](https://www.bis.org/fsi/fsisummaries/nsfr.htm)).
- [-] Fed is taking on more fiscal risk, as its balance sheet expands. (Chris Sims)
  - Mitigant: the asset mix may reduce such risk ???? (Jeremy Stein)


### <ins>A close look at balance sheet normalization</ins>

The Federal Open Market Committee (FOMC) discusses and designs Principles and Plans in normalizing the stance of monetary policy. Historically, there principles and plans are implemented via
- set a federal fund target rate;
- tapering (i.e., slow the pace of the asset purchase)
- balance sheet run-off (i.e., reduce the balance sheet size b

*Tapering: Fed Monthly Asset Purchase*

|  Statement Date | Action Date | UST | Agency MBS | Total |
|----------------:|------------:|----:|-----------:|------:|
| First-tine  | Before Tapering       | $45 |        $40 |   $85 |
|        Dec-2013 |    Jan-2014 | $40 |        $35 |   $75 |
|        Jan-2014 |    Feb-2014 | $35 |        $30 |   $65 |
|                 |    Mar-2014 | $35 |        $30 |   $65 |
|        Mar-2014 |    Apr-2014 | $30 |        $25 |   $55 |
|        Apr-2014 |    May-2014 | $25 |        $20 |   $45 |
|                 |    Jun-2014 | $25 |        $20 |   $45 |
|        Jun-2014 |    Jul-2014 | $20 |        $15 |   $35 |
|        Jul-2014 |    Aug-2014 | $15 |        $10 |   $25 |
|                 |    Sep-2014 | $15 |        $10 |   $25 |
|        Sep-2014 |    Oct-2014 | $10 |         $5 |   $15 |
|                 |    Nov-2014 |  $0 |         $0 |    $0 |
|                 |             |     |            |       |
| Second-tine | Before Tapering         | $80 |        $40 |  $120 |
|        Nov-2021 |    Nov-2021 | $70 |        $35 |  $105 |
|                 |    Dec-2021 | $60 |        $30 |   $90 |
|        Dec-2021 |    Jan-2022 | $40 |        $20 |   $60 |
|                 |    Feb-2022 | $20 |        $10 |   $30 |
|                 |    Mar-2022 |  $0 |         $0 |    $0 |

*Balance Sheet Run-off: Monthly Caps On SOMA Securities Reductions*

| From      | To       | UST | Agency Debt and Agency MBS |
|-----------|----------|:---:|:--------------------------:|
| Oct 2017  | Dec 2017 |  $6 |             $4             |
| Jan 2018  | May 2018 | $12 |             $8             |
| Apr 2018  | Jun 2018 | $18 |             $12            |
| Jul 2018  | Sep 2018 | $24 |             $16            |
| Oct 2018  | Apr 2019 | $30 |             $20            |
| May 2019  | Sep 2019 | $15 |             $20            |
| Sep 2019* | Mar 2020 |  $0 |             $20            |
|           |          |     |                            |
| Jun 2022  | Aug 2022 | $30 |            $17.5           |
| Sep 2022  | TBA      | $60 |             $35            |

[This](https://libertystreeteconomics.newyorkfed.org/2022/04/the-feds-balance-sheet-runoff-and-the-on-rrp-facility/) and [this](https://libertystreeteconomics.newyorkfed.org/2022/04/the-feds-balance-sheet-runoff-the-role-of-levered-nbfis-and-households/) discussed the role of MMFs in the balance sheet runoff.

Note:

For more data on MMFs, I'd recommend to check out the website of [the Office of Financial Research](https://www.financialresearch.gov/money-market-funds/us-mmfs-investments-by-fund-category/).

"interest rate cap"
https://www.federalreserve.gov/econres/notes/feds-notes/what-happened-in-money-markets-in-september-2019-20200227.htm
https://libertystreeteconomics.newyorkfed.org/2022/01/the-feds-latest-tool-a-standing-repo-facility/

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
