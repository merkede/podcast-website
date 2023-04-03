---
title: Call Analysis Deep Dive
summary: |
  Understanding how to reduce OPEX with our call centres
  
date: 2011-01-13
categories:
  - Analysis

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

### Inspiration

This project sparked my interest in the philosophy of science, leading me to take a course on the subject at Oxford University's Department for Contiuning Education. As part of my coursework, I wrote an assignment entilted 'The demarcation between science and pseudoscience', which relates to the importance of falsifiability and testability of hypotheses. This concept proved relevant in the project, as various opinions on the causes of rising AHT were expressed without adequate evidence. 

Karl Popper's view of falsification and his theory of knowledge suggest scientific theories should not be based on verification but on falsifiability. In other words, it is impossible to prove a theory correct, but it is possible to prove it false. Popper's theory of knowledge, in particuar, emphasizes the importance of critical thinking and openness to criticism. He argued that knowledge is not absolute, but rather tentative and subject to change based on new evidence. This idea is particularly relevant in this project and helped me develop a more critical and rigorous mindset, always questioning and testing my assumptions to ensure that I was making accurate predictions and delivering value to our customers.

### TL;DR

As a result of my efforts to address problematic behaviours and retrain call agents at specific call sites, average call handling times at British Gas were reduced by an average of 2 minutes. These changes also led to a significant decrease in wrap times and eliminated bad practices of agents prematurely ending calls or transferring them. 

I developed and implemented an anomaly detection algorithm that performed batch inference on D+2 (day +2) data to identify unusually high numbers of "short calls" - the best indicator of agent malpractice. Significant system changes were implemented, rerouting calls tagged as 'Null' to the dial pad selection option, instead of sending them to the 'General Enquiries', preventing unnecessary call transfers.
 
**Business perspective - **



**Customers perspective - **



**How is the problem allowed to happen?'**

A vast number of our calls do not contain NLCS (natural language call steering) tags and even more contain the tag 'NONE COLLECTED' suggesting either the customer was silent or the speech recognition was not upto task.


**How is something allowed to persist?'**

Questions also remain regarding 

It is imperative that we adopt a scientific and data-driven approach to comprehensively understand our current situation.

Lacking a comprehensive system for tracking and monitoring the parts installed and improving the notes taken by engineers during their visits to identify the causes of breakdowns, we will continue to lack the necessary data collection to enhance our service offering. 



### Defining the problem



{{< figure src="img/Agent_Call_Types_copy.jpeg" caption="Agent Call Types" >}}


### Changes to Agent Tenure

After analyzing the data, I observed a decline in agent tenure starting from the winter of 2018. In addition, two significant findings emerged:

The percentage of long-serving agents is diminishing.
The retention of new agents is inadequate.


{{< figure src="img/Agent_Tenure.jpg" caption="Average Agent Tenure and volumes of Agents by Tenure" >}}

This finding is of great importance as it establishes a null hypothesis: does an increase in call agent turnover result in a higher average handling time (AHT)?

### Agent New Starters

{{< figure src="img/Agent_New_Starter.jpg" caption="Average Agent Tenure and volumes of Agents by Tenure" >}}

Below is a graph of AHT attrition with no. of interactions (2018-2019 combined) - across three different call types

- The first graph indicates that new starters face a steep and prolonged learning curve, which eventually levels off into a steady improvement. To cope with this learning curve, it is recommended to assign a specialist to handle this particular call type since new starters need a considerable amount of practice interactions before reaching a stable performance level.

- The second graph indicates new starters face a steep but brief learning curve, which is followed by a gradual but consistent improvement. This call type is better suited for new starters who receive some additional initial training since it does not demand as many practice interactions before performance levels become stable.

- The third graph indicates new starters face a shallow but long learning curve, followed by a steadily slow improvement. To cope with this learning curve, it is recommended to assign a specialist to handle this particular call type since new starters need a considerable amount of practice interactions before reaching a stable performance level.

### Agent Performance

{{< figure src="img/Attempt_1.jpg" caption="" >}}

An ellipse algorithm was employed to overlay the first graph and identify the 'normal' population in terms of agent performance, as evaluated by the average handling time.

{{< figure src="img/Attempt_2.jpg" caption="" >}}

Agent performance in 2019 (orange) is worse - has a higher mean AHT - than compared with agent performance in 2018 (blue)

{{< figure src="img/Attempt_3.jpg" caption="" >}}

Although the key has been removed from this graph, it displays the performance of every agent, with each call center location represented by a distinct colour. The graph indicates that agents in the Leeds call center handle calls with significantly shorter duration compared to agents in the Manchester call center.

{{< figure src="img/Attempt_4.jpg" caption="" >}}

The graph illustrates the performance of each agent across a sample of call types, enabling me to identify call types that exhibit consistent agent performance.

### Agent - Engage Time




{{< figure src="img/Agent_Engage.jpg" caption="Agent engage time" >}}



### Agent - Wrap Time




{{< figure src="img/Agent_Wrap.jpg" caption="Agent wrap time" >}}





<div>
  <div style="float:left; width:60%;">
    Effects things have on other are sometimes indirect. Let's take an example
    involving a soccer ball and a broken glass. Sometimes, you will break a glass by
    shooting the ball right onto it. But sometimes not. Sometimes, the ball will
    land next to a cat, a cat peacefully sleeping on someone's lap. Sometimes, the 
    cat will end up scared which will result in a jump right onto a table, table 
    on which was the glass[^1]. Indirect.
  </div>
  <div style="float:right; width:40%;">
    {{< figure src="img/Agent_Tenure.jpg" caption="Average Agent Tenure and volumes of Agents by Tenure" >}}
  </div>
</div>

