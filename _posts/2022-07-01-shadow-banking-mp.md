---
layout: post
title: "[MP] Shadow Banking: MMMF and Monetary Policy"
---

{{ page.title }}
================

<p class="meta">June 2022 - Charlotte, NC</p>

In this post, I'd narrow down the focus to money market mutual funds (MMMFs) and its role in the Fed's ["Balance Sheet Normarlization"](https://www.federalreserve.gov/monetarypolicy/policy-normalization-discussions-communications-history.htm).

A MMMF is a kind of mutual fund that issues shares to investors and invests in a diverse set of short-term (often less than 1-year) assets such as US Treasuries and commercial papers. [Fidelity Money Market Fund](https://fundresearch.fidelity.com/mutual-funds/summary/31617H201), for example, holds assets in commercial papers (26.43%, combined), certificate of deposit (22.88%), Repo (19.16%) and etc, as of April-2022.

<p align="center">
<a href="https://fundresearch.fidelity.com/mutual-funds/composition/31617H201">
  <img src="/images/posts_2022-07-01/one_mmmf.png" width="300">
</a>
</p>

The portfolio composition is sensitive to market condition and subject to change at the discretion of the fund managers. A year earlier, for instance, the fund allocated more in CP at 41.2%, while less in CDs at 12.7%, partly due to more credit appeitite and ample liquidity.

## MMMF Industry

Now, let's turn to the portfolio composition of the whole MMMFs industry and how it evolves over the time.  

<p align="center">
<iframe src="https://fred.stlouisfed.org/graph/graph-landing.php?g=Pgow&width=670&height=475" scrolling="no" frameborder="0" style="overflow:hidden; width:670px; height:525px;" allowTransparency="true" loading="lazy">
</iframe>
</p>

### Reserve Primary Fund and two Reforms:

A key event that has a profound influence on the industry is the unprecedented collapse of the Reserve Primary Fund.

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
  1. a liquidity fee may be levied in order to pay for that access (i.e. investors might be required to pay a fee if they redeem shares during this time).
  2. a redemption gate may be implemented to limit redemptions in a fund for a short period of time (up to 15 business days in a 90-day period).


### Reverse Repo to MMMFs is like bank reserve to commercial banks.


## MMMFs and "Balance Sheet Normalization"

### Tapering
Fed Monthly Asset Purchase
|  Statement Date | Action Date | UST | Agency MBS | Total |
|----------------:|------------:|----:|-----------:|------:|
| Before Tapering |             | $45 |        $40 |   $85 |
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
| Before Tapering |             | $80 |        $40 |  $120 |
|        Nov-2021 |    Nov-2021 | $70 |        $35 |  $105 |
|                 |    Dec-2021 | $60 |        $30 |   $90 |
|        Dec-2021 |    Jan-2022 | $40 |        $20 |   $60 |
|                 |    Feb-2022 | $20 |        $10 |   $30 |
|                 |    Mar-2022 |  $0 |         $0 |    $0 |

### Balance Sheet Run-off
Monthly Caps On SOMA Securities Reductions
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

https://www.federalreserve.gov/econres/notes/feds-notes/what-happened-in-money-markets-in-september-2019-20200227.htm

Note:

[Commercial Paper, CP](https://en.wikipedia.org/wiki/Commercial_paper): unsecured and short-term (<270 days) debt instrument used to fund operating expense, inventory, and receivables. As a CP matures it is often replaced with newly issued CP (often called as rollover).


**Reference**

[1] SEC Sue Reserve Primary Fund, 2011 [Lawsuit](https://www.sec.gov/spotlight/reserve_primary_fund_investors/gardephe_opinion.pdf)

[2] Bogglehead, ["The_2008_money_market_crisis"](https://www.bogleheads.org/wiki/The_2008_money_market_crisis)

[3] Kacperczyk and Schnabl, 2010, ['When Safe Proved Risky: Commercial Paper during the Financial Crisis of 2007–2009'](https://pubs.aeaweb.org/doi/pdfplus/10.1257/jep.24.1.29)

[4] The Editors, 2011, [Bloomberg's Opinion](https://www.bloomberg.com/opinion/articles/2011-12-23/money-market-mutual-funds-that-break-the-buck-can-become-a-memory-view)

[5] President Working Group, 2020, [Overview of Recent Events and Potential Reform
Options for Money Market Funds](https://home.treasury.gov/system/files/136/PWG-MMF-report-final-Dec-2020.pdf)
