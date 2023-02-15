---
title: Call Analysis Deep Dive
summary: |
  Understanding how to reduce OPEX with our call centres
  
date: 2011-01-13
categories:
  - R package

links:
  - icon: link
    icon_pack: fas
    name: docs
    url: https://jsmediation.cedricbatailler.me/
  - icon: github
    icon_pack: fab
    name: source
    url: https://github.com/cedricbatailler/jsmediation
---

# What is the problem, Is it a problem worth solving ...

# What is Hedging ...

- Our stakeholder approaches us with the problem 'Are breakdowns predictable?'

The short answer, if I was a betting man, would be 'I think so'. Perhaps another answer could involve
answering the questions with a series of questions:

1) Why are you asking?
2) What problem are you trying to solve?
3) Is it a problem worth solving?
4) Do we collect the data --- data collection is huge here!!

Effects things have on other are sometimes indirect. Let's take an example
involving a soccer ball and a broken glass. Sometimes, you will break a glass by
shooting the ball right onto it. But sometimes not. Sometimes, the ball will
land next to a cat, a cat peacefully sleeping on someone's lap. Sometimes, the 
cat will end up scared which will result in a jump right onto a table, table 
on which was the glass[^1]. Indirect.


------------------------------------------------------------------------

{{< figure src="img/Agent_Tenure.jpg" caption="Average Agent Tenure and volumes of Agents by Tenure" >}}

------------------------------------------------------------------------


# Is this a problem? Is it worth solving?

**Mediation analysis** is a statistical tool that can be use to find out that 
the reason why people are less likely to buy drugs with complex name is because 
they percieved the drugs as more dangerous. While there are several ways to
conduct mediation analysis, the `JSmediation` package implements the best one
of them[^3]: joint-significance.

Have a look at [the documentation](https://jsmediation.cedricbatailler.me/) and 
give it a shot!

[^1]: Yeah. It happens.

[^2]: Dohle, S., & Siegrist, M. (2014). Fluency of pharmaceutical drug names predicts perceived hazardousness, assumed side effects and willingness to buy. _Journal of Health Psychology_, _19_(10), 1241-1249. doi: 10.1177/1359105313488974

[^3]: This has to be understood as the one with the lowest number of false positive. Yzerbyt, V., Muller, D., **Batailler, C.**, & Judd, C. M. (2018). New recommendations for testing indirect effects in medi‑ational models: The need to report and test component paths. _Journal of Personality and Social Psychology_, _115_(6), 929–943. 10.1037/pspa0000132
