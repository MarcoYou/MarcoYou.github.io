---
layout: post
toc: true
title: "Monetary Policy During Sanitary Crisis"
categories: Memo
tags: [Memo]
math: true
author:
  - Marco You
[comment]: <> (mathjax inline > \\(...\\) )
[comment]: <> (mathjax block  > $$...$$   )
[comment]: <> <p align="center"> <img src="/image/file_name.png" alt="file_name" width="420" height="300"> </p>
---

## Role of FED during Sanitary Crisis

The ultimate goal of any central bank is to make the economy to prosper in long run. One of the key requirements, or possibly the most important requirement, is the **full employment**.

Even though it is obvious to say that full employment is important and is a good thing for the economy, it is not obvious why it is important and how it is important. Let's first discuss that.

When the number of jobs decreases, the overall consumption decreases. A decrease in consumption implies a decrease in demand. A decrease in demand then causes a decrease in supply. If the supply decreases, companies stop or reduce their investment. And once they stop investing, then no jobs are created. If there are no jobs created, then again, it leads to another decrease in demand, so on and so forth. This is the phenomenon called **Secular Stagflation** that Lawrence Summers, 27th U.S Secretary of the Treasury, was worried about.

To stop this somewhat vicious cycle, a government can hire more people by itself. Or, it can force companies to hire more people. But they both sound ridiculous, right? So the best strategy would be to **encourage companies to invest**. To do so, in the case of the U.S, the FED can foster an environment that gives companies an incentive to invest more. And the incentive would be a **cheaper price of debt**. When debt is cheap enough relative to inflation rate, then at some point, it is same as just giving them (almost or literally) free money when companies decide to borrow money from banks.

**So how do you make debt cheaper?**

## Monetary Policy of FED

1일짜리 vs 10년짜리 (모기지는 10년짜리랑 연동)

I personally identify 3 tools that allow FED to make debt cheaper. But before getting into it, I have to explain what kind of debt I am talking about and why particularly that specific kind of debt is important.

**First, what kind of debt we are talking about?**

Here, we are talking about notes. It is not a commercial loan or any sorts like that. We are precisely talking about **the U.S. 10-year treasury note** (often called **10Y T-note** or by its ticker **^TNX**), which is a type of debt that can be traded and whose issuer is the federal government of the U.S. having a maturity equal to 10 years.

- **T-Bills**: short maturity terms, from 4 weeks to a year;
- **T-Notes**: middle maturity terms, from 2 to 10 years;
- **U.S. Bonds**: long maturity terms, from 20 to 30 years.

**Second, why is 10Y T-Note important?**

The type of Asset-Backed Security (ABS) that holds the **largest amount of capital** is the **Mortgage-Backed Security (MBS)** in the U.S.. It is incomparable with all the other types of ABSs as shows the chart below.

<p align="center"> <img src="/image/memo/MBS_vs_ABS.jpg" alt="MBS vs ABS" width="500" height="300"> </p>

[Source](https://jsf.pm-research.com/content/early/2019/11/11/jsf.2019.1.089)

Because of its size and also the fact that it is "Mortgage-Backed", it made it so important in the U.S. Economy. And why am I talking about MBS? it is because, as the chart below shows, **_30-Year Fixed Average Mortgage Rate_ is tightly coupled with the _10Y T-Note Rate_**.

<p align="center"> <img src="/image/memo/FRED_10TY_30MR.png" alt="T-Note and MBS" width="500" height="300"> </p>

[Source](https://fred.stlouisfed.org/series/MORTGAGE30US#0)


Now we understand what kind of debt that FED targets and why it is important. We can proceed to discuss the 3 tools that I mentionned at the beginning of this section.

Let me list them first.

1. Controling the Benchmark Interest Rates
2. Quantitative Easing
  - QE with Federal Bonds
  - QE with Corporate Bonds
3. Alternative Long-Term Yield Direct Intervention:
  - Yield Curve Control (YCC)
  - Operation Twist

### 1. Controling the Benchmark Interest Rates

In the U.S, the benchmark interest rates are called **Federal Funds Rate**. Federal funds rate (FFR) is the target interest rate set by the Federal Open Market Committee (FOMC) at which commercial banks borrow and lend their excess reserves to each other **overnight**. So this is an extremely short-term interest rate. Since all the interest rates of different maturities are increasingly aligned according to the maturity term risk, by lowering or lifting the FFR, the FED can, in theory, control all the other interest rates of longer maturity terms.

Let's take a look at the image below.

<p align="center"> <img src="/image/memo/FFR.jpeg" alt="FFR" width="500" height="360"> </p>

(forget about my bad drawing skill)

If FED Chairman Powell pulls down FFR, then all the other interest rates on the rope, including the 10Y T-Note rate, will come down altogether. This is how FED controls the money supply in the market.

But when the economic burden is too heavy, it is hardly possible to control the long term rates as they tend to resist more when the economy is going through a recession and also naturally the impact of change in FFR is less direct on them.

This is why Quantiative Easing is necessary. It is as if Powell goes up on a ladder and pulls down the rope at 10Y T-Note level. This is why we often say this method is not conventional.

### 2. Quantitative Easing
#### QE with Federal Bonds

Let's recall that FED wants to encourge companies to invest more therefore to create more jobs. And they encourage companies by (let's be simple) providing them low-price liquidity.

Let's see how QE works:

<p align="center"> <img src="/image/memo/How_QE_works.png" alt="How_QE_works" width="370" height="500"> </p>

[Source](https://boycewire.com/how-does-quantitative-easing-work/)

In the step number 2, we see that FED purchases government denominated debt. By the law of supply and demand, **extra demand for these government bonds lowers the interest rate of bonds** in the first round of this operation (FED must have lowered the FFR before QE so this is also another explanatory factor of decreasing bond interest rate).

In addition, **QE will reduce the supply of long-term bonds in the secondary market since a huge part of these bonds will be bought by the FED**. This, in second round, **causes bond prices to increase**. But you might ask why should anypne buy these expensive bonds. It is because huge financial instituations like pension funds or life insurance companies must comply to liquidity and solvency regulations. Moreover, it is better to hold bonds because it guarantees an additional cash flows in the future no matter how marginal that is. If these institutions hold cash, then some of its value will be lost in the next year because of the inflation.

In combination, **bond yields will go down, which makes other risky assets more attractive, such as stocks**.

Another question that could arise is "_If the FED inject this much of cash into the economy, wouldn't it risk high inflation?_". Actually, there is no **high** inflation caused by QE because no money goes into people's hands. FED buys bonds from financial institutions, not from people. So no direct cash is injected into daily economy but is injected into corporate and financial economy.

#### QE with Corporate Bonds

The final goal of FED is to create job in companies, by giving them money. QE with federal bonds has to go through an intermediary which is a financial instituations. QE with corporate bonds will purchase bonds issued by companies directly providing them direct liquidity. But this operation is unlikely to happen as first, it is very risky to hold corporate bonds as you don't know what is going to happen to those companies in 10 years, whereas a country, especially the U.S, is very lkely, almost certainly, will still exist. Also, this can face political polemics because only some companies will be selected to do QE.


_On a side note, FED can also buy MBSs alongside national bonds. This is another reason why MBS rate and 10Y T-Note rate are important_

### 3. Alternative Long-Term Yield Direct Intervention
#### Yield Curve Control

Yiled Curve Contral (YCC) is one of monetary policy options that works in the same way as the QE. The principal difference is that YCC sets a target bond yield not allowing the yield curve to go beyond the threshold set by FED.

A yield curve is a line that plots yields (interest rates) of bonds having equal credit quality but differing maturity dates (the fact that maturities differ could imply they do not have same credit quality but the difference is marginal). The slope of the yield curve gives an idea of future interest rate changes and economic activity. 

**Normally**, an yield curve is concave and monotonously increasing. It is normal because bonds with longer maturity should be remunerated more than bonds with shorter maturity. Because time has value.

<p align="center"> <img src="/image/memo/US_yield_curve.png" alt="US_yield_curve" width="500" height="360"> </p>

[Source](http://www.worldgovernmentbonds.com/country/united-states/)

But, sometimes this curve can twisted following a monetary policy operation called **Operation Twist**.

#### Operation Twist

Operation Twist refers to a Federal Reserve monetary policy initiative designed to lower long-term interest rates to further stimulate the U.S economy. The initiative is done by selling short-term bonds and buying long-term bonds. This in result lifts short-term rates. Therefore it reduces the spread between short-term rate and long-term rate, which is sort of controversial.

The difference between QE and Operation Twist resides in the balance sheet of FED. The former necessarily expands the FED's balance sheet, whereas the latter does not expand the FED's balance sheet. Therefore, it is considered to be less aggressive form of easing.

## Insufficiency of Monetary Policy

2009 Subprime Crisis was caused by financial institutions and affected them the most. It was sufficient(?) to finance them, or in other words, **bail out** them, with **tendered Quantitative Easing**, which is the basic QE explained in the previous section above.

But the Covid-19 Pandemic Crisis is not a financial crisis. It is a real economy crisis that affects daily workers directly. That is why Trump and Biden wrote/writes stimulus check to give cash to people directly. And this comes from budget deficit which is a **fiscal policy** financed with federal bonds, which are bought by the FED.

This structure necessarily brings inflation.