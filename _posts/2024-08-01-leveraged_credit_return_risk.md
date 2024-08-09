---
layout: post
title: "[Leveraged Finance] Expected Return and Risk from Private Credit"
---

{{ page.title }}
================

<p class="meta">August 2024 - Charlotte, NC</p>

It's important for institutional investors to assess corporate credit investment relative to other asset classes before deciding its desirable allocation to private credit investment within an overall portfolio.   

This post describes the capital market assumptions on risk and return of different asset classes. I will also introduce one of the most popular theoretical underpinnings of credit pricing. 

<br>

## Expected Return and Risk: Private Credit vs Other Asset Classes

For institutional investors, one of key inputs to determine the asset allocation is long-term reutrn and risk for individual asset classes. 
Below is the 2024-2033 capital market assumptions from Callan, an investment consulting firm. 
Their calculation indicates Private Credit would earn 7.4%, slightly higher than High Yied bond as compensation for illiquidity and complexity

<p align="center">
<img src="/images/posts_2024_08_01/Callan_mkt_assumptions.png" width="700" >
</p>

## Expected Return Calculation: Private Credit - Corporate Lending

Nesbitt [1] provides an illustrative calculation for ten-year return forecasts for corporate lending based on eight key assumptions. 
- **Gross Yield** (Line 1) and **Credit Loss Rate** (Line 2) are two critical inputs that are estimates and hence subject to uncertainty.
- Leverage (Line 3) and Cost of Finance (Line 8) are equally important when leverage is used to enhance return. 

<p align="center">
<img src="/images/posts_2024_08_01/Nesbitt_private_debt.png" width="500" >
</p> 
   
<br>

## Merton's Option Theory for Credit

In Merton's world, the accounting equation and the put-call parity are married to birth a popular corporate credit theory. 
- **Accounting**: Asset = Equity + Liabilities 
- **Put-Call Parity**:  Call - Put = Discount * (Forward Price of Asset - Strike Price) 

Specifically, **Equity investors / Shareholders** pay some price to have a claim on the residual interest in the firm's assets after deducting liabilities. Shareholders can be thought of buying a call option. In the same spirit, **Corporate lenders / Creditors** sell a put option, receive a credit risk premium, and expect full repayment at maturity plus interest. For example, buy an AAA-graded (or B-graded) bond with a face value of $100 at $98 (or $90). 

$$
\begin{align*} 
\text{Discount} * \text{Forward Price of Asset} &= \text{Call} &+ \text{Discount} * \text{Strike Price} - \text{Put} \\
\text{Market Value of Asset} &=  \text{Market Cap of Equity} &+ \text{Total Liabilities} - \text{Credit Risk Premium}  \\ 
\end{align*}
$$

With this insight, the Black-Scholes formula is easily applicable for estimating gross yield and credit loss rate. 
- gross yield = risk-free rate + *credit risk premium*
- credit loss rate = *PD* * EAD * LGD

Per theory, *credit risk premium* responds to four risk factors; LTV, asset vol, risk-free interest, and time-to-maturity. Among others, the Debt-to-Asset ratio and asset volatility are particularly important in estimating the default probability. Distance-to-Default (DD), for instance, calculates the difference between asset and default point (e.g., current liability + 1/2 LT liability), scaled by unobservable asset volatility, and maps it to a probability value from [0, 1] via certain measurement (e.g., logistic function).    

<p align="center">
<img src="/images/posts_2024_08_01/Merton.png" width="800" >
</p> 

Empirically, the gross yield is eventually determined by market participants at origination and during trading. Some examples include   
- IB executed the reprice tight of talk, reducing the spread from S+300 bps to S+250 bps while removing the credit spread adjustment ("CSA"), achieving 75 bps of interest savings for the firm
- IB's execution resulted in final pricing of S+300 bps | 99.75 OID; compared to price talk of S+350-375 bps | 99.50 OID.
- Client announced $benchmark size trade spread across 2-40yr tenors, verbalizing size in $10MM with a skew of proceeds to the long end of the curve // The order books developed quickly, hitting $11bn within the first hour, eventually peaking at $40bn with demand skewed to maturities>10yrs // IB opted to push pricing 25 bps tighter on the 2yr and 20bps tighter on the remaining tranches.
- Client's Tranche A due June 1, 2027 ($825MM), Coupon: 4.375% (price talk: 3.875%-4.375%), Conversion Premium: 20.0% (Price Talk: 20.0%-25.0%), Call protection: Life Non-Call. 

Still, the concept remains useful in estimating the real-time credit loss rate and thus obtaining a reasonable expected return of credit investment. 

**Reference**

[1] Stephen L. Nesbitt, 2023, [Private Debt: Yield, Safety and the Emergence of Alternative Lending](https://www.amazon.com/Private-Debt-Emergence-Alternative-Lending/dp/1119944392)
