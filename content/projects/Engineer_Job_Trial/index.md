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

### TL;DR

Productionisation of an end-to-end machine learning model built using Azure ML and Databricks, reducing allocated engineer job times by 15%, saving £2million per annum, driving efficiencies and cost savings.


## What is the problem, Is it a problem worth solving ...

> The core business challenge that we are addressing lies in optimizing our processes and resources to address the issue of overbooking and rescheduling of appointments at British Gas, a Service function of Centrica. 

Our customers rely on us to resolve their problems quickly and efficiently, especially when it pertains to our Homecare product insurance offering that requires engineer visits for installation, repair, or service. To ensure customer satisfaction and timely resolution of their problems, it is imperative to optimize our processes and allocate resources efficiently.

Upon conducting a thorough analysis, we identified a key problem - engineers were completing their tasks much faster than the allotted time and on occasion 'gaming the system', which resulted in inefficiencies and a lack of accurate job time predictions.

> To address these issues, I proposed the business should optimize our resource allocation, and maximize our profitability by tackling the issue of overbooking and rescheduling of appointments head-on. 

This is achieved by reducing allocated job times in accordance with actual time spent on the job. By doing so, we can increase the number of jobs completed in a day and provide customers with more precise job time predictions, reducing the number of reschedules, and increasing customer satisfaction. Implementing guardrails and optimizing our systems will prevent any further gaming of the system by engineers.

## The approach 

### Model

In order to implement our Data Science solution, I needed to run an automated pyspark regression model on Azure Databricks that would provide optimised engineer job times. Various models were compared against each other, including random forest, gradient boosting and deep learning - even stacking a few with each other. The model including some of the following features created with some engineering:

- Holidays
- Weather (Temp, Solar Rad, Precip, Cloud Cover)
- Location
- Contractor Y/N
- Priority Y/N
- Landlord Y/N
- Type of Boiler
- Many More :)

### Experimental Design

In order to implement our model in the real world, I had a few consideration

(1) What metric should I use to measure performance?
(2) How do we implement this whilst ensuring guardrails are present
(3) How will this be percieved by our engineers on the ground?

In order to answer the first - it was key to setup an experimental design and a two step process - namely a soft trial & hard trial.

 - Soft Trial: I would simulate the changes by running my model side-by-side with the actual jobs for a period of 2 weeks, without officially changing the times in the system. In doing so, at the end of the two weeks I would compare my results against actual job times and assess performance.
 
 - Hard Trial: Upon sucessful performance from the Soft Trial, changes would be made to the live system and monitoring and guardrails in place to assess performance. The changes would require a 'change request' being issued and field managers were not able to inform any engineers, as this was confidential and could affect engineer morale.

- Test & Control Patch : During the hard trial, I would monitor the performance of the patches but also compare it's performance against another patch of similar conditions that were still using the old times. The patch changed served as the 'Control Patch' whilst the patch of similar conditions would become the 'Test Patch'

## Soft Trial

- A 2 week trial showed we outperformed current times at a ratio of 7 to 3, saving time on each and every job performed by our engineers. Scaling these times up represents huge savings in the additional number of jobs we can perform, the speed at which we can tackle our backlog during winter and customer satisfaaction in reducing forced errors.


------------------------------------------------------------------------

{{< figure src="images/picture_1.jpg" caption="A well performing soft trial paved the way for a hard trial and productionisation." >}}

------------------------------------------------------------------------

## Hard Trial


## Mlflow

Mlflow was used to track model metrics and artifcats, manage ML end-to-end 

## Databricks Workflow

The model was scheduled using Databricks Workflows - this allows you to schedule your tasks


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
