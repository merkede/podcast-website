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

I developed an R Shiny app that assists field engineers in choosing the best parts for repairs, whilst at the customers property, to enhance customer satisfaction. The app presented at the highest 'Services & Logistics Management' meetings influenced business decisions on the procurement and installation of original parts, reducing repeat appointments and boosting customer NPS.

**From a business perspective:**

The business was able to make better procurement decisions, negotiate with suppliers and claim back costs for parts still within warranty period. The part associations and refurbished analysis prevented customer inbound contact and repeat visits by our engineers. This creates a cycle, allowing for more engineer capacity in the field to better serve our customers.

**From a customer perspective:**

With better part procurement, association insights and increased engineer field capacity, customers are able to enjoy uninterrupted supply of heat and hot water and not troubled into contacting our contact centres. 

### Defining the problem

**A senior business stakeholder approaches me with the problem 'Are breakdowns predictable?'**

The impetus for this project was the rise in repeat breakdowns at British Gas, without a clear understanding of the root cause. 

To address this issue, I sought to predict when customers would experience a breakdown by taking a first principles approach - identifying that a breakdown occurs when a part within the boiler fails. By predicting when a part would fail, I could predict, with some probability, when a breakdown would likely occur.

> The first principles approach is a problem-solving methodology that involves breaking down a complex problem into its fundamental elements and then reassembling them to arrive at a solution.

Our project began by analyzing the time to failure of common parts in our customer base's boilers. We then expanded it to include part associations, preventing multiple engineer visits due to missing parts, and anomaly part order detection, allowing us to manage our inventory and stock our engineers' vans efficiently[.](https://www.databricks.com/glossary/predictive-maintenance)

> Our customers take out boiler breakdown insurance cover hoping to enjoy uninterrupted supply of heat and hot water. What better way to achieve this then antcipating a breakdown and preventing it from happening!

**How is the problem allowed to happen?'**

The challenge of repeat breakdowns at British Gas persists due to several contributing factors, including deficient procurement checks and insufficient field training. Furthermore, as the customers' homes operate as black boxes, it becomes arduous to track and monitor all activities, leading to a dearth of knowledge concerning the cause of breakdowns. This inadequate understanding makes it difficult to forestall these issues from arising.

**How is something allowed to persist?'**

It is imperative that we adopt a scientific and data-driven approach to comprehensively understand our current situation.

Lacking a comprehensive system for tracking and monitoring the parts installed and improving the notes taken by engineers during their visits to identify the causes of breakdowns, we will continue to lack the necessary data collection to enhance our service offering. 

{{< figure src="image001-01.png" caption="Breaking down a problem" >}}


### Uncovering poor procedures (EDA)

The picture below is of a motorised valve.  

{{< figure src="image001.png" caption="A motorised valve, typically costing £25" >}}

A motorised valve is comprised of the following:
- (1) Powerhead also known as an actuator (the silver box at the top)
- (2) The 2 or 3 port body (the brass part underneath)
 
In addition, the actuator (silver box on top) contains the follow and more inside it:
- Micro switch
- Spring return
- Synchron motor
 
Engineers attempted cost-saving by modifying motorised valve parts instead of replacing them for £25. However, this was identified as a false economy as fixing the part led to future breakdowns within 2 months. By replacing the part, significant cost savings were achieved, and future breakdowns prevented. This change was one of the successful outcomes of the project.

### Time to failure

- Cox Hazard

The Cox proportional hazards model, also known as the Cox regression model, is a type of survival analysis method used to model time-to-event data. It's particularly useful when examining the relationship between predictor variables and a time-to-event outcome, such as predicting when a part in a boiler will fail.

{{< figure src="excel_graph2.jpg" caption="Comparing lifetime of different Synchron motors aiding engineers and procurement teams in making critical decisions" >}}

- Left and Right censoring

Left censoring occurs when some of the event times are not known precisely but only known to be at least as large as some value. 
Right censoring, on the other hand, occurs when some of the event times are not observed because the study ends before they occur. 

In this project, I used the Cox-Hazard method to run a survival analysis on the time-to-failure of common parts across boiler makes in our customer base. By taking left and right censoring into account and scaling the model using sparklyR, I was able to accurately predict when a part was likely to fail, allowing us to schedule preventative maintenance and reduce the number of breakdowns.

{{< figure src="excel_graph.jpg" caption="Analysing time to failure of a particular part used by British Gas engineers during boiler repair visits" >}}

### Refurbushed vs. Non-refurbished parts

I led the charge in extracting key insights into the performance of refurbished versus non-refurbished parts, ultimately driving cost savings and enhanced customer satisfaction for British Gas.

When comparing the lifetime of refurbished parts v/s non-refurbished parts, it became evident that refurbished parts had considerably less capacity, causing more freauent breakdowns and ultimately leaving the customer without heating and hot water. Armed with this critical information, I presented our findings at Services Management meetings and made a compelling case to the Managing Director for prioritizing solutions that put our customers first.

Here are a few examples of the wealth of insights gleaned:

- There is a 10% difference in survival rate on a Glow-worm 796957 and BAXI 379031 using the same PCB part
- PCB Alpha models have quite have a volatile lifespan that is highly unpredictable. This model should be avoided
- Parts E68349 & 743001 are poor brands for replacement Synchron motors and fail twice as fast as other brands 

> A synchron motor can cost between £7-£35, however the cost of visiting a customer can be £100 (costs incl. labour,parts and travel). By avoiding synchron motor parts E68349 & 743001, the business can prevent a customers boiler breaking down within the contractual period and save £100!

These insights enabled our procurement and services management team to craft a value proposal that is expected to save our business £200m per annum. By avoiding problematic parts and prioritizing solutions that enhance customer satisfaction, we are able to deliver better outcomes for our customers and our business. Working backwards from the customer's needs and priorities continues to drive our innovation and success at British Gas.

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

> Monitoring anomaly part order detection was tricky as engineers have stock of parts in the van. Therefore an engineer may order 

------------------

{{< figure src="excel3.jpg" caption="A control chart highlighting unusually high / low part orders made by field engineers, triggering alert notifications " >}}

------------------

### Literature review

Predictive maintenance is a critical aspect of modern businesses, aimed at proactively identifying potential failures in complex systems and reducing downtime, thus providing a competitive edge. By leveraging data science and machine learning techniques, predictive maintenance enables organizations to make informed decisions about maintenance operations, minimize unplanned downtime, and optimize resource utilization.

As highlighted by M.M. de Oliveira et al. in their paper "A Machine Learning-Based Predictive Maintenance Framework for Industrial Plants," "predictive maintenance helps organizations to reduce the risk of unexpected breakdowns, improve the availability and performance of critical assets, and lower maintenance costs." This leads to increased customer satisfaction, improved operational efficiency, and a reduction in overall maintenance costs, making predictive maintenance a key component of a successful business strategy.

Predictive maintenance begins with the installation of sensors on systems, which continuously collect operational data, typically in the form of time series data, including timestamps, sensor readings, and device identifiers. This data is analyzed using machine learning algorithms, with the goal of predicting equipment failures and determining the Remaining Useful Life (RUL) of the equipment. Predictive maintenance can be implemented using either a classification or regression approach.

The classification approach, as outlined by J. Kim et al. in their paper "Anomaly Detection for Predictive Maintenance using Deep Convolutional Neural Networks," predicts the likelihood of failure in the next n-steps, providing a binary answer to the possibility of failure. The regression approach, as described by Y. Jiang et al. in their paper "Predictive Maintenance for Industrial Assets Using LSTM Recurrent Neural Networks," predicts the RUL, providing a more precise estimate of the time before the next failure.

As stated by S. Aswathy et al. in their paper "Predictive Maintenance for Industrial Equipment: A Review of Machine Learning Approaches," "predictive maintenance is an essential aspect of modern businesses, providing organizations with a competitive edge by enabling proactive maintenance planning, reducing downtime and maximizing resource utilization." By harnessing the power of data science and machine learning, predictive maintenance provides organizations with the tools they need to make informed decisions, reduce costs, and improve the performance and availability of their critical assets.
