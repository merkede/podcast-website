---
title: Engineer Job Trial
summary: |
  Productionisation of an end-to-end machine learning model built using Azure ML and Databricks, reducing allocated engineer job times by 15%, saving £2million per annum, driving efficiencies and cost savings. 
date: 2021-06-13
categories:
  - projects
  - engineer

links:
  - icon: link
    icon_pack: fas
    name: docs
    url: https://github.com/merkede3/Engineer_Job_Trial/blob/main/docs/project_plan.md
  - icon: github
    icon_pack: fab
    name: source
    url: https://github.com/merkede3/Engineer_Job_Trial/
---

# TL;DR

TL;DR - 

Productionisation of an end-to-end machine learning model built using Azure ML and Databricks, reducing allocated engineer job times by 15%, saving £2million per annum, driving efficiencies and cost savings.


# What is the problem, Is it a problem worth solving ...

The core business challenge that we are addressing lies in optimizing our processes and resources to address the issue of overbooking and rescheduling of appointments at British Gas, a Service function of Centrica. Our customers rely on us to resolve their problems quickly and efficiently, especially when it pertains to our Homecare product insurance offering that requires engineer visits for installation, repair, or service. To ensure customer satisfaction and timely resolution of their problems, it is imperative to optimize our processes and allocate resources efficiently.

Upon conducting a thorough analysis, we identified a key problem - engineers were completing their tasks much faster than the allotted time and on occasion 'gaming the system', which resulted in inefficiencies and a lack of accurate job time predictions.

> To address these issues, I proposed the business should optimize our resource allocation, and maximize our profitability by tackling the issue of overbooking and rescheduling of appointments head-on. 

This is achieved by reducing allocated job times in accordance with actual time spent on the job. By doing so, we can increase the number of jobs completed in a day and provide customers with more precise job time predictions, reducing the number of reschedules, and increasing customer satisfaction. Implementing guardrails and optimizing our systems will prevent any further gaming of the system by engineers.

## The approach 

### Model choice

In order to implement our Data Science solution, I needed to run an automated pyspark regression model on Azure Databricks that would provide optimised engineer job times. The model including some of the following features:




### Experimental Design

In order to implement our model in the real world, I had a few consideration

(1) What metric should I use to measure performance?
(2) How do we implement this whilst ensuring guardrails are present
(3) How will this be percieved by our engineers on the ground?

In order to answer the first - it was key to setup an experimental design and a two step process, soft trial & hard trial.


, I needed to engage with the stakeholders  first needed to 
Test Patch
Control Patch


## Soft Trial



## Hard Trial


## Mlflow



## Databricks Workflow



## Deep learning pyspark


## Job times per part required (fan vs PCB), Job times per boiler


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
