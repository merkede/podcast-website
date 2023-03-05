---
title: Predictive Maintanence
summary: |
  Using IoT and data analytics to predict and prevent breakdowns can reduce overall downtime by 50%. [McKinsey].
date: 2021-06-14
categories:
  - R package


links:
  - icon: link
    icon_pack: fas
    name: docs
    url: https://github.com/merkede3/predictive_maintenance/blob/main/docs/project_plan.md
  - icon: github
    icon_pack: fab
    name: source
    url: https://github.com/merkede3/predictive_maintenance/blob/main/src/shiny_dashboard.R
---

### TL;DR

TL;DR - I developed an R Shiny app that assists field engineers choose the best parts for repairs, available on their tablets during a job, to enhance customer satisfaction. The app influenced business decisions on the procurement and installation of original parts, reducing repeat appointments and boosting customer NPS.


## AFT and Cox-Propotional Hazard (CPH) ... survival analysis using SPARK

### Defining the probem

- Managing stakeholders

> Our stakeholder approaches us with the problem 'Are breakdowns predictable?'

Upon initial review of the issue, two potential solutions presented themselves: utilizing historical time-series data to forecast equipment breakdowns or implementing a time-to-failure algorithm. However, prior to pursuing these technical approaches, it is crucial to gain a thorough understanding of the business problem being addressed. 

This includes conducting a cost-benefit analysis to determine the potential impact of a solution and to weigh the resources required against the value they will bring to the organization. By taking a strategic and data-driven approach, we can ensure that any solution we implement aligns with our overall business goals and delivers a meaningful return on investment.

- First Principles Thinking


[Have](https://www.databricks.com/glossary/predictive-maintenance)

### Unearthed instance of inadequate procedures.

The picture below is of a motorised valve.  

{{< figure src="image001.png" caption="A motorised valve, typically costing £25" >}}

A motorised valve is comprised of the following:
 
- (1) Powerhead also known as an actuator (the silver box at the top)
- (2) The 2 or 3 port body (the brass part underneath)
 
In addition, the actuator (silver box on top) contains the follow and more inside it
 
- Micro switch
- Spring return
- Synchron motor
 
Engineers attempted cost-saving by modifying motorised valve parts instead of replacing them for £25. However, this was identified as a false economy as fixing the part led to future breakdowns within 2 months. By replacing the part, significant cost savings were achieved, and future breakdowns prevented. This change was one of the successful outcomes of the project.


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
