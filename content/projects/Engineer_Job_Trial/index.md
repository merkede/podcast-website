---
title: Engineer Job Trial
summary: |
  Productionisation of an end-to-end machine learning model built using Azure ML and Databricks, reducing allocated engineer job times by 15%, saving £2million per annum, driving efficiencies and cost savings. 
date: 2021-06-13
categories:
  - projects
  - engineer
  - machine learning
  - production

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


### Defining the problem

> The core business challenge that we are addressing lies in optimizing our processes and resources to address the issue of overbooking and rescheduling of appointments at British Gas, a Service function of Centrica. 

Our customers rely on us to resolve their problems quickly and efficiently, especially when it pertains to our Homecare product insurance offering that requires engineer visits for installation, repair, or service. To ensure customer satisfaction and timely resolution of their problems, it is imperative to optimize our processes and allocate resources efficiently.

Upon conducting a thorough analysis, we identified a key problem - engineers were completing their tasks much faster than the allotted time and on occasion 'gaming the system', which resulted in inefficiencies and a lack of accurate job time predictions.

> To address these issues, I proposed the business should optimize our resource allocation, and maximize our profitability by tackling the issue of overbooking and rescheduling of appointments head-on. 

This is achieved by reducing allocated job times in accordance with actual time spent on the job. By doing so, we can increase the number of jobs completed in a day and provide customers with more precise job time predictions, reducing the number of reschedules, and increasing customer satisfaction. Implementing guardrails and optimizing our systems will prevent any further gaming of the system by engineers.

### The approach 

### ML Model

To implement our Data Science solution, I leveraged an automated PySpark pipeline regression model on Azure Databricks to deliver optimised engineer job times. After evaluating multiple models, such as random forest, gradient boosting, and deep learning, I employed feature engineering to enhance the model's accuracy. By thoughtfully selecting and engineering these features, the model was able to deliver superior performance and provide significant value to our organization:

- Holidays
- Weather (incl. Temp, Solar Rad, Precip, Cloud Cover)
- UK Region
- Contractor v/s Non-Contractor
- Priority Appointment 
- Landlord Customer
- Business Customer
- Type of Appliance (Boiler)
- Many More 😀

Due to the large size of the dataset, traditional data processing tools such as pandas were not suitable for the task. I chose to use Databricks and PySpark to handle the data. Databricks is an optimal choice for working with Spark, providing a powerful and scalable environment that can handle large-scale data processing efficiently. By leveraging the capabilities of PySpark, I was able to perform complex transformations and feature engineering on the data, which would have been a challenge using traditional tools.

### Experimental Design

Implementing our model in the real world required careful consideration, including determining the performance metric, implementing the changes while ensuring guardrails were in place, and ensuring that the changes would be well-received by our engineers on the ground. To address these issues, I developed an experimental design that involved a two-step process:

- Soft Trial:

To measure performance, I ran my model alongside actual jobs for a period of two weeks without officially changing the times in the system. At the end of the trial, I compared the results against actual job times to assess performance.

- Hard Trial: 

Upon successful performance in the soft trial, changes were made to the live system, and monitoring and guardrails were put in place to assess performance. Changes required a 'change request' to be issued, and field managers were not able to inform any engineers to maintain confidentiality and avoid affecting morale.

- Test & Control Patch:

During the hard trial, I monitored the performance of the patches and compared it against a control patch of similar conditions that still used the old times to ensure that the changes were effective. This approach helped us implement the changes while minimizing disruption and ensuring that we delivered improvements that met our goals.

------------------------------------------------------------------------
{{< figure src="images/control.jpeg" caption="Designing an experiment in which engineers with new times form the test and engineers with standard times form control group" >}}
------------------------------------------------------------------------

### Soft Trial

- After conducting a 2-week trial, we found that our engineers were able to complete their tasks significantly faster using our new method, outperforming the current times at a ratio of 7 to 3. This time savings on each job adds up quickly when scaled across the total number of jobs we perform, resulting in substantial cost savings and increased capacity for additional jobs. Moreover, the improved efficiency of our engineers during winter backlog periods results in improved customer satisfaction by reducing forced errors.


------------------------------------------------------------------------
{{< figure src="images/Picture_1.jpg" caption="A well performing soft trial allowed for the progression to a hard trial and productionisation of the model" >}}
------------------------------------------------------------------------


### Hard Trial


- Mlflow 2.0

Mlflow was the secret sauce that helped me create a top-performing model. With its advanced tracking and organization capabilities, I was able to streamline my workflow and optimize my models, all while keeping my track of all my experiments is a neat and organized manner.

Mlflow enabled me to register the model, track metrics, and perform nested runs to compare different ensemble models. Mlflow's model registry and versioning capabilities ensured that my models were stored securely and easily accessible, and its integration with TensorFlow, PyTorch, and Scikit-learn made it easy to use. It's seamsless integration with pyspark was essential for this project, given the scale of the data. 

- Batch Inference

Due to infrastructure limitations, batch inference was the only viable option for this project. To enable batch inference, a series of notebooks were created to form the ML lifecycle, and were scheduled and triggered using Databricks workflow. The notebooks were stored in an Azure DevOps repository, allowing for testing pipelines to be triggered and facilitating complete CI/CD production.

- Databricks Workflow

Databricks Workflow allowed me to schedule and connect notebooks, creating an end-to-end pipeline that streamlined the entire process. The automation of the data ingestion pipeline and intermediary pipelines through to model registry, model performance, and unit/integration testing enabled me to track and monitor the performance of the models in real-time.

------------------------------------------------------------------------
{{< figure src="images/workflows.jpeg" caption="Databricks workflows allows you to schedule multiple scripts (ingestion to inference) to run on different clusters." >}}
------------------------------------------------------------------------


### Monitoring model performance

In order to effectively monitor the performance of the model, I engaged a data engineer to help connect Databricks with PowerBI to produce a dashboard that visualizes the mean absolute error (MAE) of the model over each run. By integrating these two powerful tools, I was able to create a seamless workflow that allowed for real-time monitoring of the model's performance. The dashboard provided stakeholders with a clear understanding of how the model was performing and helped to identify areas for improvement. 

To ensure seamless and accessible visualization of the project's progress, I decided to integrate PowerBI with Databricks. Although Databricks has in-built dashboard features, it would require stakeholders to obtain a license or for the dashboard endpoint to be hosted as a web service, which could be cumbersome. As each member of the company has access to PowerBI by default, integrating the two platforms was the most practical choice. 

------------------------------------------------------------------------
{{< figure src="images/powerbi.jpeg" caption="Databricks workflows allows you to schedule multiple scripts (ingestion to inference) to run on different clusters." >}}
------------------------------------------------------------------------

## Making an impact

I am incredibly proud of the impact that my project has had on our customers. As a data scientist, it's rare to see your work go beyond the experimentation stage and actually make it into production, but this project was different. I was able to deliver a top-performing model that provided real benefits to our customers, and knowing that my work was making a difference was an incredibly rewarding experience. Looking back on the project, I am grateful for the opportunity to work on something that had a real-world impact and for the support and collaboration of my team. It's moments like these that make me proud to be a data scientist and motivate me to continue pushing the boundaries of what's possible.
