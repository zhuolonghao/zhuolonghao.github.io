---
layout: post
title: "[MP] Shadow Banking: What and Why"
---

{{ page.title }}
================

<p class="meta">May 2022 - Charlotte, NC</p>

**Shadow banks** are not banks, but act like banks when it comes to credit intermediations (i.e., making loans to household and business and/or underwrite debt securities). The term "shadow bank" is coined in 2007 by Paul McCulley to describe its then nature of being levered, under-regulated and distant to the public [1]. It is really the 2008's Great Financial Crisis (GFC) that brings the shadow banking system to light, as it was later recognized as one of key factors leading up to the crisis[2].

In this post, I was sharing what I learned about what's about shadow banking and why it's interesting/important.


## What are shadow banks?

At the risk of oversimplication, let me first put up a few observations:

* shadow banks do not take deposits from households. Instead, they rely on short-term funding, which make themselves sensitive to market conditions.  

* shadow banks are more likely to use the "*originate to distribute*" strategy; E.g., they make loans to leveraged borrowers with the intention of selling them to third parties like institutional investors.

* shadow banks do have value proposition: *improving the efficiency of credit markets* and *market clearing*. In the meantime, they're also criticized for their imperfect credit risk transfer (e.g., institutional investors take excessive risks, while shadow bankers are overpaid after risk-adjustment).

* shadow banks operate under minimal government oversight, and have non-guaranteed government backstopping during the stress periods.

A thorough study on shadow banks was found in a series of works done by brilliant economists such as [3]. In the meantime, the shadow banking system has been closely monitored by the Financial Stability Board ([FSB](https://www.fsb.org/)) since 2011 [4][5]. After 7 years' tracking and monitoring, the FSB decided in 2018 to move away from the term “shadow banking” and adopt “*nonbank financial intermediations*”([NBFIs](https://en.wikipedia.org/wiki/Non-bank_financial_institution)) to reflect its "*emphasis the forward-looking aspect of the FSB’s work.*"[6]. In particular, the FSB watches closely three aggregates, defined by their business models, activities and associated vulnerabilities, that include *non-bank financial intermediation (NBFI)*, *other financial intermediaries(OFIs)*, and *narrow measure of NBFI*.  

**Narrow Measure of NBFI** are financial intermediaries that involves *liquidity*, *maturity* and *credit* transformation as well as the build-up of *leverage*, without explicit access to central bank liquidity or public sector credit guarantees[3]. Traditional banks, on the other hand, benefit from their privileged accesses to, say, FDIC's deposit insurance and Federal Reserve's discount windows and various lending programs (e.g., the Main Street Lending Program).

In my eyes, shadow banks and narrow measure of NBFI are twin concepts that i will use them interchangeably.     


## Why are shadow banks important?

In the 2020 annual monitoring report [7], nearly half (48.3%) of total global financial assets comes from the NBFIs; it is reported to have $226.6 trillion for overall NBFI, of which the narrow NBFIs or shadow banking have $63.2 trillion. A further breakdown indicates the collective investment vehicles (e.g., money market funds (MMFs), fixed income funds, and some hedge funds) makes up the majority of the narrow NBFIs.

<a href="https://www.fsb.org/2021/12/global-monitoring-report-on-non-bank-financial-intermediation-2021/">
  <img src="/images/posts_2022-05-01/NBFIs_FSB.png">
</a>

<br><br>

Unfortunately, FSB's annual reports has a laser focus on global welfare with limited details on individual countries. To fill the gap, I make/replicated calculations for U.S. shadow banking system using Fed's Flow of Funds.

Per my worksheet [8], the shadow banks outsized the traditional banks; as of Dec-2021, the shadow banks have $31.5 trillion in financial assets, $1.4 trillion higher than banks and credit combined. Looking back on history, the shadow banks' asset has consistently surpassed traditional banks since the mid-1995. Their difference reaches the peak during the 08's crisis, and keeps shrinking since then.

<a>
  <img src="/images/posts_2022-05-01/NBFIs_FRED.png">
</a>

It should also be noted that the asset size should not be interpreted as a proxy for the net supply of credit provided by shadow banks for many reasons such as the originated credit has been sold and offload from their balance sheet.

In the next post, i will try to explain how the shadow banking system are chained up in credit intermediation and related activities.


Note:

The definition of entities involved in the FSB calculation could be found [here](https://www.oecd.org/statistics/data-collection/Guidelines-on-Non-Bank-Financial-Intermediation.pdf).

**Reference**

[1] Paul McCulley, 2009, ['The Shadow Banking System and Hyman Minsky’s Economic Journey'](https://www.pimco.com/en-us/insights/economic-and-market-commentary/global-central-bank-focus/the-shadow-banking-system-and-hyman-minskys-economic-journey/)

[2] The Financial Crisis Inquiry Commission, 2011, ['The Financial Crisis Inquiry Report'](https://www.govinfo.gov/content/pkg/GPO-FCIC/pdf/GPO-FCIC.pdf)

[3] Pozsar, Adrian, Ashcraft, and Boesky, 2012, ['Shadow Banking'](https://www.newyorkfed.org/medialibrary/media/research/staff_reports/sr458.pdf)

[4] Financial Stability Board, 2011 ['Shadow Banking: Strengthening Oversight and Regulation'](https://www.fsb.org/wp-content/uploads/r_111027a.pdf?page_moved=1)

[5] Financial Stability Board, 2012 ['Global Shadow Banking Monitoring Report 2012'](https://www.fsb.org/wp-content/uploads/r_121118c.pdf)

[6] Financial Stability Board, 2019 ['Global Monitoring Report on Non-Bank Financial Intermediation 2018'](https://www.fsb.org/wp-content/uploads/P040219.pdf)

[7] Financial Stability Board, 2021 ['Global Monitoring Report on Non-Bank Financial Intermediation 2020'](https://www.fsb.org/2021/12/global-monitoring-report-on-non-bank-financial-intermediation-2021)

[8] [Author's worksheet based on fed data](https://github.com/zhuolonghao/zhuolonghao.github.io/tree/main/_images/posts_2022-05-01)
