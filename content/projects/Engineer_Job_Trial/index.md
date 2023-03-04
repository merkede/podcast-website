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

------------------------------------------------------------------------
{{< figure src="images/control.jpeg" caption="Designing an experiment in which engineers with new times form the test and engineers with standard times form control group" >}}
------------------------------------------------------------------------

## Soft Trial

- A 2 week trial showed we outperformed current times at a ratio of 7 to 3, saving time on each and every job performed by our engineers. Scaling these times up represents huge savings in the additional number of jobs we can perform, the speed at which we can tackle our backlog during winter and customer satisfaaction in reducing forced errors.

------------------------------------------------------------------------
{{< figure src="images/Picture_1.jpg" caption="A well performing soft trial allowed for the progression to a hard trial and productionisation of the model" >}}
------------------------------------------------------------------------


## Hard Trial


## Mlflow 2.0

Mlflow was the secret sauce that helped me create a top-performing model. With its advanced tracking and organization capabilities, I was able to streamline my workflow and optimize my models, all while keeping my track of all my experiments is a neat and organized manner.

Mlflow enabled me to register the model, track metrics, and perform nested runs to compare different ensemble models. Mlflow's model registry and versioning capabilities ensured that my models were stored securely and easily accessible, and its integration with TensorFlow, PyTorch, and Scikit-learn made it easy to use. It's seamsless integration with pyspark was essential for this project, given the scale of the data. 


## Databricks Workflow

Tatabricks Workflow allowed me to schedule and connect notebooks, creating an end-to-end pipeline that streamlined the entire process. The automation of the data ingestion pipeline and intermediary pipelines through to model registry, model performance, and unit/integration testing enabled me to track and monitor the performance of the models in real-time.

------------------------------------------------------------------------
{{< figure src="images/workflows.jpeg" caption="Databricks workflows allows you to schedule multiple scripts (ingestion to inference) to run on different clusters." >}}
------------------------------------------------------------------------


## Monitoring model performance






## Making an impact

I am incredibly proud of the impact that my project has had on our customers. As a data scientist, it's rare to see your work go beyond the experimentation stage and actually make it into production, but this project was different. I was able to deliver a top-performing model that provided real benefits to our customers, and knowing that my work was making a difference was an incredibly rewarding experience. Looking back on the project, I am grateful for the opportunity to work on something that had a real-world impact and for the support and collaboration of my team. It's moments like these that make me proud to be a data scientist and motivate me to continue pushing the boundaries of what's possible.
