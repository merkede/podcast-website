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

Through collaboration between Centrica's Data Science team and NEAS Energy's ATS in Denmark, the development of an R forecasting package was achieved, resulting in a significant profit increase of £10k for NEAS Energy's ATS team. This innovative solution not only increased profits for NEAS Energy's ATS team but has also paved the way for future collaborations and advancements in the field of energy trading.

The forecasting package is highly scalable and applicable across various biogas assets. The solution includes an anomaly detection model that applies SVM filters to clean data and a predictive model that accurately forecasts future biogas tank fuel levels. This information is then fed into NEAS Energy's Lebrade trading algorithm, which leverages optimal spot prices and employs hedging strategies to determine the most profitable time to sell power generated.

**Business perspective**

NEAS Energy's Algorithmic Trading Solutions (ATS) team sought to acquire and manage energy generating assets that were often overlooked by larger energy companies due to their problems. To achieve this strategy, they acquired a biogas asset with a faulty sensor and turned to Centrica's Data Science team to create a more accurate prediction model for the biogas fuel level. The resulting R package contained a model that detected anomalies and predicted future fuel levels, allowing NEAS Energy to sell the generated power at optimal spot prices using the Lebrade trading algorithm. 

By acquiring seemingly undesirable assets at scale with small profit margins, NEAS Energy could generate significant profits when aggregated. This project resulted in a net profit of 10k for NEAS Energy's ATS team and the development of a universal forecasting package that could be scaled across multiple biogas assets, providing long-term value for the company.

**Customers perspective**

The successful collaboration on this project between NEAS Energy and the customer has solidified the relationship and fostered a collaborative approach that benefits both parties. As a result, the project has opened up many new opportunities for future projects and further collaboration. This has resulted in a stronger, more profitable relationship between the two companies. The project's success demonstrates the value of a collaborative and straightforward approach to business relationships, leading to mutual benefits and long-term success.

### Defining the problem

NEAS Energy was facing a significant business problem in acquiring biogas assets that were not turning a profit due to faulty sensors and inaccurate fuel level readings. This lack of visibility into fuel levels made it difficult to determine how much fuel could be fed into the CHB turbine to generate power for the Lebrade algorithm to hedge. 

> Faulty sensor readings in a biogas asset hinder efficient power production and sales due to uncertainty in fuel level.

The development of a reliable and accurate forecasting solution was critical to enable NEAS Energy to acquire seemingly undesirable assets on a large scale for a small profit margin and generate significant profits when these assets are effectively managed.

{{< figure src="img/biogas.jpg" caption="My simplified understanding of the end-to-end process" >}}



