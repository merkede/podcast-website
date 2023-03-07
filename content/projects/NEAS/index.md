---
title: Fuel-level & trade optimisation
summary: |
  Generating £10k profit for NEAS Energy's ATS team
  
date: 2011-01-13
categories:
  - forecasting
  - trading
  - R package

links:
  - icon: link
    icon_pack: fas
    name: docs
    url: 
  - icon: github
    icon_pack: fab
    name: source
    url: 
---

### TL;DR

Through collaboration between Centrica's Data Science team and NEAS Energy's ATS in Denmark, the development of an R fuel-level forecasting package was achieved, resulting in a significant profit increase of £10k for NEAS Energy's ATS team. This innovative solution not only increased profits for NEAS Energy's ATS team but has also paved the way for future collaborations and advancements in the field of energy trading.

**Business perspective**

NEAS Energy's Algorithmic Trading Solutions (ATS) team sought to acquire and manage energy generating assets that were often overlooked by larger energy companies due to their problems. By acquiring seemingly undesirable assets at scale with small profit margins, NEAS Energy could generate significant profits at scale. 

To achieve this strategy, they acquired a biogas asset with a faulty sensor and turned to Centrica's Data Science team to create a more accurate prediction model for the biogas fuel level. The resulting R package contained a model that detected anomalies and predicted future fuel levels, allowing NEAS Energy to sell the generated power at optimal spot prices using the Lebrade trading algorithm. 


**Customers perspective**

The successful collaboration on this project between NEAS Energy and the customer has solidified the relationship and fostered a collaborative approach that benefits both parties. As a result, the project has opened up many new opportunities for future projects and further collaboration. This has resulted in a stronger, more profitable relationship between the two companies. The project's success demonstrates the value of a collaborative and straightforward approach to business relationships, leading to mutual benefits and long-term success.

### Defining the problem

NEAS Energy was facing a significant business problem in acquiring biogas assets that were not turning a profit due to faulty sensors and inaccurate fuel level readings. This lack of visibility into fuel levels made it difficult to determine how much fuel could be fed into the CHP engines to generate power for the Lebrade algorithm to hedge. 

> Faulty sensor readings in a biogas asset hinder efficient power production and sales due to uncertainty in fuel level.

This information is then fed into NEAS Energy’s Lebrade trading algorithm, which leverages optimal spot prices and employs hedging strategies to determine the most profitable time to sell power generated.

The development of a reliable and accurate forecasting solution was critical to enable NEAS Energy to acquire seemingly undesirable assets on a large scale for a small profit margin and generate significant profits when these assets are effectively managed.

{{< figure src="img/biogas.jpg" caption="My simplified understanding of the end-to-end process" >}}

### Privacy agreement

The model incorporates client data such as input biomass, daily schedule, and location-specific weather information, as well as sensitive information related to NEAS Energy's proprietary Lebrade algorithm. To ensure the security of this data, a privacy impact assessment (PIA) was conducted, and secure measures were implemented for safe data transfer and automatic deletion.

### Data Cleaning

My approach to cleaning the biogas asset data involved implementing a smoothing technique called loess smoothing. This technique allowed me to eliminate the volatility in the fuel level data, which could have resulted in inaccurate predictions of power generation and decreased profits for NEAS Energy.

To ensure the accuracy of my model, I calculated the mean square error (mse) between the original data and the loess line. I then split the entire time series into multiple chunks and calculated the mean square error per chunk. This helped identify and remove any outliers that could have skewed the results.

{{< figure src="img/svm.jpg" caption="A one-class SVM identifying cases where mean square error between loess trend and actuals are extreme" >}}

Another important task was differentiating between charging and discharging of the fuel tank. When fuel levels are increasing with time, I flag this as charging and when fuel levels decrease with time the tank level is discharging.

> Constant values in the production table signal a connection loss

By creating an increasing and decreasing label for the fuel levels, I was able to identify significant periods of time where the levels remained constant. This was a critical step as it allowed me to identify that these periods of constant values represented a disconnection with the faulty sensor - often followed by a sudden spike or dip in the fuel level, indicating an incorrect reading. This helped me to more accurately clean the data and remove outliers, leading to more reliable and accurate predictions.

{{< figure src="img/outlier.jpg" caption="Observing cases when the sensor is behaving odd and providing faulty readings" >}}

### Noise v/s signal

Constant values in the production table signal a connection loss. To maintain a continuous time-series view of the data, I identified periods of signal loss in the production table as 'FALSE' or noise and inferred these values. The signal was referred to as 'TRUE'.

{{< figure src="img/correct.jpg" caption="Constant values in the production table signal a connection loss" >}}

### Model





{{< figure src="img/iter.jpg" caption="Constant values in the production table signal a connection loss" >}}




{{< figure src="img/mae.jpg" caption="Constant values in the production table signal a connection loss" >}}


{{< figure src="img/validation.jpg" caption="Constant values in the production table signal a connection loss" >}}
