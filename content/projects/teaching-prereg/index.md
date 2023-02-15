---
title: HH Settlement short term forecasting
summary: |
  Real-time optimization & Balancing using Smart Meters
date: 2019-06-13
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

The general purpose of this presentation is to ascertain the accuracy with which half-hour SMART meter data can be utilised to predict settlement values.


It would follow, that should half-hour be accurate enough to predict settlement values, so shall 10s SMART meter data.

In order to test this – SMART and Settlement values have been compared under 2 iteration.


------------------------------------------------------------------------

{{< figure src="img/HH_Settlement_1.jpg" caption="HH Smart consumption v/s settlement values" >}}

------------------------------------------------------------------------




------------------------------------------------------------------------

{{< figure src="img/HH_Settlement_2.jpg" caption="Leveraging local weather station data as input features" >}}

------------------------------------------------------------------------





------------------------------------------------------------------------

{{< figure src="img/HH_Settlement_3.jpg" caption="%MAPE, delta between SMART & Settlement values" >}}

------------------------------------------------------------------------




------------------------------------------------------------------------

{{< figure src="img/HH_Settlement_4.jpg" caption="Different Settlement Runs" >}}

------------------------------------------------------------------------





------------------------------------------------------------------------

{{< figure src="img/HH_Settlement_5.jpg" caption="GSP and the corresponding map" >}}

------------------------------------------------------------------------




------------------------------------------------------------------------

{{< figure src="img/HH_Settlement_6.jpg" caption="NBP consumption v/s Meter consumption" >}}

------------------------------------------------------------------------


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

And, sometimes, it is important to investigate how these indirect effets are 
chained. It is known that people are less likely to buy drugs with complex 
name[^2]. But why? What is the chain behind this effect?


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
