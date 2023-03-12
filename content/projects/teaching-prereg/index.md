---
title: HH short-term forecasting
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

# TL;DR

Produced a 


What is the problem, Is it a problem worth solving ...

The general purpose of this presentation is to ascertain the accuracy with which half-hour SMART meter data can be utilised to predict settlement values.


It would follow, that should half-hour be accurate enough to predict settlement values, so shall 10s SMART meter data.

In order to test this – SMART and Settlement values have been compared under 2 iteration.



### The settlement process

In the UK, the power market settles every half-hour, and the settlement process involves a complex chain of activities that determine the cost of electricity consumed during that period. The settlement process involves a range of participants, including power generators, power traders, energy suppliers, and the Balancing and Settlement Code Company (BSCCo). 

Energy suppliers play a crucial role in the settlement process as they are responsible for providing electricity to end-users and paying for the electricity they consume. The settlement process begins with the supplier reading the smart meter data of their customers every half-hour. This data is transmitted to the data collector, who aggregates the data from multiple smart meters and sends it to the data aggregator

The data aggregator then processes the data, validates it, and creates a set of half-hourly meter readings for each supplier. These readings are used to calculate the total energy consumed by each supplier during the half-hour period. The settlement system then calculates the charges that the supplier must pay for the energy consumed during that period.

The charges are calculated based on the imbalance between the energy consumed by the supplier's customers and the energy that the supplier contracted to buy from the wholesale market. If the supplier's customers consumed more energy than the supplier bought, the supplier incurs a deficit, and they must pay a penalty. Conversely, if the supplier bought more energy than their customers consumed, they have a surplus, and they receive a credit.

The settlement process also involves the use of various market indices and prices, including the National Grid Balancing Mechanism (BM) and the Day-Ahead Wholesale Market. These indices and prices are used to determine the cost of electricity during the settlement period and are factored into the calculation of the supplier's charges.

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

