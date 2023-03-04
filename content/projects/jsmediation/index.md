---
title: Predictive Maintanence
summary: |
  Let's not work to solve a problem, let us try In social science, statistical mediation models are a popular method to show
  causality. The `JSmediation` package implements mediation models in an 
  easy-to-use R package.
date: 2019-06-13
categories:
  - R package


links:
  - icon: github
    icon_pack: fab
    name: source
    url: https://github.com/
---

### TL;DR

TL;DR - I developed an R Shiny app that assists field engineers choose the best parts for repairs, available on their tablets during a job, to enhance customer satisfaction. The app influenced business decisions on the procurement and installation of original parts, reducing repeat appointments and boosting customer NPS.


## AFT and Cox-Propotional Hazard (CPH) ... survival analysis using SPARK

### Defining the probem

- Managing stakeholders

> Our stakeholder approaches us with the problem 'Are breakdowns predictable?'

Upon initial review of the issue, two potential solutions presented themselves: utilizing historical time-series data to forecast equipment breakdowns or implementing a time-to-failure algorithm. However, prior to pursuing these technical approaches, it is crucial to gain a thorough understanding of the business problem being addressed. 

This includes conducting a cost-benefit analysis to determine the potential impact of a solution and to weigh the resources required against the value they will bring to the organization. By taking a strategic and data-driven approach, we can ensure that any solution we implement aligns with our overall business goals and delivers a meaningful return on investment.

### First Principles Thinking



The short answer, if I was a betting man, would be 'I think so'. Perhaps another answer could involve
answering the questions with a series of questions:

1) Why are you asking?
2) What problem are you trying to solve?
3) Is it a problem worth solving?
4) Do we collect the data --- data collection is huge here!!


> Using IoT and data analytics to predict and prevent breakdowns can reduce overall downtime by 50%. (McKinsey)

[Have](https://www.databricks.com/glossary/predictive-maintenance)



### Time to failure


------------------
{{< figure src="excel_graph.jpg" caption="Analysing time to failure of a particular part used by British Gas engineers during boiler repair visits" >}}
------------------


### Refurbushed vs. Non-refurbished parts




------------------

{{< figure src="excel_graph6.jpg" caption="Comparing lifetime of two different PCB brand parts for a BAXI boiler & a refubished equivalent (blue)" >}}


{{< figure src="excel_graph5.jpg" caption="Comparing lifetime of two different PCB brand parts for a Gloworm boiler & a refubished equivalent (blue)" >}}

------------------

### Association rule mining



------------------

{{< figure src="excel1.jpg" caption="Association between parts that are ordered together by field engineers during a domestic boiler gas repair" >}}


{{< figure src="excel2.jpg" caption="Association maps between parts that are ordered together during a domestic boiler gas repair" >}}

------------------


### Anomaly part order detection



------------------

{{< figure src="excel3.jpg" caption="A control chart highlighting unusually high / low part orders made by field engineers, triggering alert notifications " >}}

------------------

### Literature review

Predictive maintenance is a critical aspect of modern businesses, aimed at proactively identifying potential failures in complex systems and reducing downtime, thus providing a competitive edge. By leveraging data science and machine learning techniques, predictive maintenance enables organizations to make informed decisions about maintenance operations, minimize unplanned downtime, and optimize resource utilization.

As highlighted by M.M. de Oliveira et al. in their paper "A Machine Learning-Based Predictive Maintenance Framework for Industrial Plants," "predictive maintenance helps organizations to reduce the risk of unexpected breakdowns, improve the availability and performance of critical assets, and lower maintenance costs." This leads to increased customer satisfaction, improved operational efficiency, and a reduction in overall maintenance costs, making predictive maintenance a key component of a successful business strategy.

Predictive maintenance begins with the installation of sensors on systems, which continuously collect operational data, typically in the form of time series data, including timestamps, sensor readings, and device identifiers. This data is analyzed using machine learning algorithms, with the goal of predicting equipment failures and determining the Remaining Useful Life (RUL) of the equipment. Predictive maintenance can be implemented using either a classification or regression approach.

The classification approach, as outlined by J. Kim et al. in their paper "Anomaly Detection for Predictive Maintenance using Deep Convolutional Neural Networks," predicts the likelihood of failure in the next n-steps, providing a binary answer to the possibility of failure. The regression approach, as described by Y. Jiang et al. in their paper "Predictive Maintenance for Industrial Assets Using LSTM Recurrent Neural Networks," predicts the RUL, providing a more precise estimate of the time before the next failure.

As stated by S. Aswathy et al. in their paper "Predictive Maintenance for Industrial Equipment: A Review of Machine Learning Approaches," "predictive maintenance is an essential aspect of modern businesses, providing organizations with a competitive edge by enabling proactive maintenance planning, reducing downtime and maximizing resource utilization." By harnessing the power of data science and machine learning, predictive maintenance provides organizations with the tools they need to make informed decisions, reduce costs, and improve the performance and availability of their critical assets.
