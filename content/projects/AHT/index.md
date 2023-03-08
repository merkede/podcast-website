---
title: Call Analysis Deep Dive
summary: |
  Understanding how to reduce OPEX with our call centres
  
date: 2011-01-13
categories:
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



Effects things have on other are sometimes indirect. Let's take an example
involving a soccer ball and a broken glass. Sometimes, you will break a glass by
shooting the ball right onto it. But sometimes not. Sometimes, the ball will
land next to a cat, a cat peacefully sleeping on someone's lap. Sometimes, the 
cat will end up scared which will result in a jump right onto a table, table 
on which was the glass[^1]. Indirect.




{{< figure src="img/Agent_Tenure.jpg" caption="Average Agent Tenure and volumes of Agents by Tenure" >}}



{{< figure src="img/Agent_Call_Types_copy.jpeg" caption="Agent Call Types" >}}

### Agent New Starters



{{< figure src="img/Agent_New_Starter.jpg" caption="Average Agent Tenure and volumes of Agents by Tenure" >}}




{{< figure src="img/Attempt_1.jpg" caption="" >}}

{{< figure src="img/Attempt_2.jpg" caption="" >}}

{{< figure src="img/Attempt_3.jpg" caption="" >}}

{{< figure src="img/Attempt_4.jpg" caption="" >}}




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

