---
layout: post
title: "[MP] Shadow Banking: Who and How"
---

{{ page.title }}
================

<p class="meta">June 2022 - Charlotte, NC</p>

As discussed in the last post, **Shadow banks** or **Narrow Measure of NBFI** are financial intermediaries that involve *liquidity*, *maturity* and *credit* transformation as well as the build-up of *leverage*, without explicit access to central bank liquidity or public sector credit guarantees[1].  

In this post, I'd continue to discuss key participants in the shadow banking system and how they're chained up to grow strongly in recent decades. My discussion includes a summary of this brilliant work [1], as well as a case study.

## How did the shadow banking system work?

Unlike traditional banks who bring deposit-taking and credit-lending under one roof, the shadow banking system is **de-centralized** in a way that the credit intermediation is performed through "a chain of nonbank financial intermediaries in a multiple process"[1] as illustrated below.  


<p align="center">
  <a href="https://www.newyorkfed.org/medialibrary/media/research/economists/adrian/1306adri_A6.pdf">
    <img src="/images/posts_2022-06-01/NBFIs_Fed_how.png" width="900" >
  </a>
</p>




"The shadow banking system transforms risky, long-term loans into seemingly credit-risk free, short-term, money like instruments, ending in wholesale funding through stable net value shares issued by money market mutual funds"[1]. The first and last node pinpoint two distinctive features: securitization and wholesale funding. Also noted that the distance between two nodes could be varying, depending on complexity of the credit intermediation.

As a rule-of-thumb, "the intermediation of low-quality long-term loans (e.g., non-conforming mortgages) involved all seven or more steps, whereas the intermediation of high-quality short- to medium-term loans (e.g., credit card and auto loans) involved usually three steps and rarely more"[1].


## Who are shadow banks?  

The shadow banking system is made of multiple niche players, each specializing in a narrow area of credit intermediation. They function like a team, with each member acquiring specific assets using specific funding techniques, as reflected on their balance sheets.

<a href="https://www.newyorkfed.org/medialibrary/media/research/economists/adrian/1306adri_A6.pdf">
  <img src="/images/posts_2022-06-01/NBFIs_Fed_who.png">
</a>

*Acronym*: {CP = Commercial Paper, MTN = Medium-Term Note, ABCP = Asset-Back CP, ABS = Asset-Backed Securitiy, O/C = Over-Collateralized, CDS = Credit Default Swap, CDO = Collateralized Debt Obligation, RR = Reverse Repo}

## Case Study: Auto Loan From Toyota Dealership

Let's take a look at how shadow banks help financing the purchase of a Toyota vehicle.


| Step | Function          | Shadow Banks Type             | Counterparaty Name                         | Funding Techniques |
|------|-------------------|-------------------------------|--------------------------------------------|--------------------|
| 1    | Loan Origination  | Captive Finance Company       | Toyota Motor Credit Corp.                  | CP, MTN, BOND      |
| 2    | Loan Warehousing  | Single-seller Conduit         | Toyota Auto Receivables LLC                | ABCP               |
| 3    | ABS Issuance      | Special-purpose Vehicle (SPV) | Toyota Auto Receivables 2021-A Owner Trust | ABS                |
| 4    | Wholesale Funding | Ultra Short Bond Fund         | Putnam Ultra Short Duration Income Fund    | $1 NAV Shares      |
| 4    | Wholesale Funding | Fixed Income Mutual Fund      | Lord Abbett Core Fixed Income Fund Class A | CUSIP = 543916878  |


Say a consumer financed her new car purchase by an auto loan from the Toyota dealership, it's highly likely she was borrowing from the Toyota Motor Credit Corp or TMCC, a financial arm of the automaker. As of Mar-2021, TMCC has $133bn of total assets, of which $109bn or (82%) is funded by debts, $85bn coming from unsecured debts and the rest $24bn from secured debts, as displayed below.

<p align="center">
  <a href="https://www.toyotafinancial.com/content/dam/tmcc-webcommons/toyotafinancial/documents/investor-relations/sec-filings/2021/Annual%20Reports%20on%20Form%2010-K/june/FY%202021%20ended%20March%2031,%202021.html#CONSOLIDATED_BALANCE_SHEET">
  <img src="/images/posts_2022-06-01/NBFIs_TMCC_debt.png" width="800" >
  </a>
</p>

Thanks to its [investment-grade](https://global.toyota/en/ir/stock/rating/) credit rating, TMCC was able to use unsecured debts as major funding source. For example, TMCC relies on commercial papers as an importance source for working capital. The market confidence in these CPs are further boosted by its abundant liquidity from banks' credit facilities, that are used in support of TMCC's CP issuances and rollover. Some of these high-quality high-yield securities could end up being held by prime money market funds like [*Putnam Ultra Short Duration Income Fund*](https://www.putnam.com/individual/mutual-funds/funds/746-ultra-short-duration-income-fund/A).

At the same time, TMCC taps asset-back securities(ABS) through the shadow banking system's channels: To isolate its securitization activity from its loan operations, it created variable interest entities(VIEs) for pooling loans receivables and issuing ABS on the behalf of TMCC.

One such example is *Toyota Auto Receivables LLC.* and *TOYOTA AUTO RECEIVABLES 2021-A OWNER TRUST*, who issued a $1,620MM asset-based security named *TOYOTA AUTO RECEIVABLES 2021-A OWNER TRUST* (Yes, it has the exactly same name as one of two VIEs). From the Prospectus (Form 428B5) of the ABS, this deal started with the TMCC transfering the right of collecting receivables to the LLC., who in turn transfers the right to the Trust. The Trust is structuring  loans' principal and interest into multiple tranches or classes of debts that customize risk, rating, timing of repayment, and lien seniority on the collateral, using credit enhancement techniques like a reserve account, overcollateralization, and subordinations. Once it's done, a new ABS was created and handed over back to the LLC. With the help of underwriters like *MUFG* and *BMO Capital Markets*, the LLC could gain access to a broad spectrum of institutional and retail investors.


<p align="center">
 <a href="https://sec.report/Document/0000929638-21-000207/">
  <img src="/images/posts_2022-06-01/NBFIs_TMCC_ABS.png", height="600">
</a>
</p>

<br/>

For example, the two largest institutional investors are [*Lord Abbett Core Fixed Income Fund Class A*](https://www.lordabbett.com/en/strategies/mutual-funds/core-fixed-income-fund.class-a.html) and [*Putnam Ultra Short Duration Income Fund*](https://www.putnam.com/individual/mutual-funds/funds/746-ultra-short-duration-income-fund/A). Details can be found in each fund's page.


Note:

[Commercial Paper, CP](https://en.wikipedia.org/wiki/Commercial_paper): unsecured and short-term (<270 days) debt instrument used to fund operating expense, inventory, and receivables. As a CP matures it is often replaced with newly issued CP (often called as rollover).

[Asset-backed Commercial Paper, ABCP](https://en.wikipedia.org/wiki/Asset-backed_commercial_paper): short-term debt instrument that is collateralized against other financial assets (e.g., loans). Often used by structured investment vehicles to fund their purchase of financial assets.

[Repurchase Agreement, REPO](https://en.wikipedia.org/wiki/Repurchase_agreement): short-term borrowing by "giving" lenders high-quality collateral (e.g., US Treasury) and agreeing to buy it back at some point in future.  

[Asset-Back Securities](https://en.wikipedia.org/wiki/Asset-backed_security): a tradable debt instrument that is collateralized (or "backed") by a specified pool of underlying assets. It can mean auto ABS, mortgage-backed Securities(RMBS,CMBS), Collateralized Loan Obligation (CLO), and collateralized debt obligation (CDO, underlying could be multiple asset classes).   


**Reference**

[1] Pozsar, Adrian, Ashcraft, and Boesky, 2012, ['Shadow Banking'](https://www.newyorkfed.org/medialibrary/media/research/staff_reports/sr458.pdf)
