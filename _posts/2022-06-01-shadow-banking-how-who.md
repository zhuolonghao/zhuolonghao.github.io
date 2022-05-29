---
layout: post
title: "[MP] Shadow Banking: Who and How"
---

{{ page.title }}
================

<p class="meta">June 2022 - Charlotte, NC</p>

As discussed in the [last post](https://zhuolonghao.github.io/2022/05/01/shadow-banking-what-why.html), **Shadow banks** or **Narrow Measure of NBFI** are financial intermediaries that involve *liquidity*, *maturity* and *credit* transformation as well as the build-up of *leverage*, without explicit access to central bank liquidity or public sector credit guarantees[1].  

In this post, I'd continue to discuss key participants in the shadow banking system and how they are chained up to grow strongly in recent decades. My discussion includes a summary of this brilliant work [1], as well as a case study.

## How did the shadow banking system work?

Unlike traditional banks who bring deposit-taking and credit-lending under one roof, the shadow banking system is **de-centralized**, where the credit intermediation is performed by  "a chain of nonbank financial intermediaries"[1].  


<p align="center">
  <a href="https://www.newyorkfed.org/medialibrary/media/research/economists/adrian/1306adri_A6.pdf">
    <img src="/images/posts_2022-06-01/NBFIs_Fed_how.png" width="900" >
  </a>
</p>


In this multistage process, risky, long-term loans are transformed into seemingly credit-risk free, short-term, money like instruments, ending in a $1 net value shares issued by money market mutual funds and held by households[1]. Two distinctive features here are securitization and wholesale funding; the securitization makes illiquid debts more marketable, while the wholesale funding makes the business model viable and sustainable.

The length of the process above depends on the complexity of credit deal. For example, the intermediation of high-quality short- to medium-term loans (e.g., credit card and auto loans) involved usually three steps and rarely more"[1].


## Who are shadow banks?  

They are niche players, each specializing in a narrow area of credit intermediations; They work closely like a team, acquiring specific assets from one by using money from another, as indicated by their interconnected balance sheets.

<a href="https://www.newyorkfed.org/medialibrary/media/research/economists/adrian/1306adri_A6.pdf">
  <img src="/images/posts_2022-06-01/NBFIs_Fed_who.png">
</a>

*Acronym*: {CP = Commercial Paper, MTN = Medium-Term Note, ABCP = Asset-Back CP, ABS = Asset-Backed Securitiy, O/C = Over-Collateralized, CDS = Credit Default Swap, CDO = Collateralized Debt Obligation, RR = Reverse Repo}

## Case Study: Auto Loan From Toyota Dealership

Say a consumer needs to borrow money to buy a car at the Toyota dealership. She may get an auto loan from the Toyota Motor Credit Corp or TMCC, a financial arm of the automaker. But where does TMCC get the money? Below is a sample of firms that help complete transactions.


| Step | Function          | Shadow Banks Type             |  Firm                          | Funding Techniques |
|------|-------------------|-------------------------------|--------------------------------------------|--------------------|
| 1    | Loan Origination  | Captive Finance Company       | Toyota Motor Credit Corp.                  | CP, MTN, BOND      |
| 2    | Loan Warehousing  | Single-seller Conduit         | Toyota Auto Receivables LLC                | ABCP               |
| 3    | ABS Issuance      | Special-purpose Vehicle (SPV) | Toyota Auto Receivables 2021-A Owner Trust | ABS                |
| 4    | Wholesale Funding | Ultra Short Bond Fund         | Putnam Ultra Short Duration Income Fund    | $1 NAV Shares      |
| 4    | Wholesale Funding | Fixed Income Mutual Fund      | Lord Abbett Core Fixed Income Fund Class A | CUSIP = 543916878  |

TMCC is the loan originator, with $133bn of total assets; of which $109bn or (82%) is funded by debts, $85bn coming from unsecured debts and the rest $24bn from secured debts.

<p align="center">
  <a href="https://www.toyotafinancial.com/content/dam/tmcc-webcommons/toyotafinancial/documents/investor-relations/sec-filings/2021/Annual%20Reports%20on%20Form%2010-K/june/FY%202021%20ended%20March%2031,%202021.html#CONSOLIDATED_BALANCE_SHEET">
  <img src="/images/posts_2022-06-01/NBFIs_TMCC_debt.png" width="800" >
  </a>
</p>

Its investment-graded credit rating allows TMCC to borrow from both private and public debt markets, including short-term unsecured commercial papers backstopped by its relationship banks' credit facilities.

TMCC also works with other shadow banks, mainly for its medium-term funding needs.

One such example is a $1,620MM asset-backed security (ABS) named *TOYOTA AUTO RECEIVABLES 2021-A OWNER TRUST*. The Prospectus (Form 428B5) exhibits all the relevant stakeholders in the deal:

1. *TMCC* transfering the right of collecting receivables to the *Toyota Auto Receivables LLC. (or the LLC)*;
2.  *The LLC.* tasking the *TOYOTA AUTO RECEIVABLES 2021-A OWNER TRUST (or the Trust)* for securitization, including;
  - structuring cashflow from loans (e.g., principal and interests) into multiple tranches or classes of debts that customize risk, rating, timing of repayment, and lien seniority on the collateral
  - using credit enhancement techniques like a reserve account, overcollateralization, and subordinations;
3. *The Trust* handing back the newly created security to *the LLC.*;
4. LLC. recruiting underwriters like *MUFG* and *BMO Capital Markets* for marketing and sale;
5. Mutual Funds like [*Lord Abbett Core Fixed Income Fund Class A*](https://www.lordabbett.com/en/strategies/mutual-funds/core-fixed-income-fund.class-a.html) and [*Putnam Ultra Short Duration Income Fund*](https://www.putnam.com/individual/mutual-funds/funds/746-ultra-short-duration-income-fund/A) buying/trading different tranches of the ABS.


<p align="center">
 <a href="https://sec.report/Document/0000929638-21-000207/">
  <img src="/images/posts_2022-06-01/NBFIs_TMCC_ABS.png", height="600">
</a>
</p>

Note:

[Commercial Paper, CP](https://en.wikipedia.org/wiki/Commercial_paper): unsecured and short-term (<270 days) debt instrument used to fund operating expense, inventory, and receivables. As a CP matures it is often replaced with newly issued CP (often called as rollover).

[Asset-backed Commercial Paper, ABCP](https://en.wikipedia.org/wiki/Asset-backed_commercial_paper): short-term debt instrument that is collateralized against other financial assets (e.g., loans). Often used by structured investment vehicles to fund their purchase of financial assets.

[Repurchase Agreement, REPO](https://en.wikipedia.org/wiki/Repurchase_agreement): short-term borrowing by "giving" lenders high-quality collateral (e.g., US Treasury) and agreeing to buy it back at some point in future.  

[Asset-Back Securities](https://en.wikipedia.org/wiki/Asset-backed_security): a tradable debt instrument that is collateralized (or "backed") by a specified pool of underlying assets. It can mean auto ABS, mortgage-backed Securities(RMBS,CMBS), Collateralized Loan Obligation (CLO), and collateralized debt obligation (CDO, underlying could be multiple asset classes).   


**Reference**

[1] Pozsar, Adrian, Ashcraft, and Boesky, 2012, ['Shadow Banking'](https://www.newyorkfed.org/medialibrary/media/research/staff_reports/sr458.pdf)
