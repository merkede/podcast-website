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

- Karl Popper

Karl Popper's view of falsification and his theory of knowledge had a profound impact on my understanding of the philosophy of science. Popper believed that scientific theories should not be based on verification but on falsifiability. In other words, it is impossible to prove a theory correct, but it is possible to prove it false. 

Popper's theory of knowledge emphasizes the importance of critical thinking and openness to criticism. He argued that knowledge is not absolute, but rather tentative and subject to change based on new evidence. This idea is particularly relevant in this project and helped me develop a more critical and rigorous mindset, always questioning and testing my assumptions to ensure that I was making accurate predictions and delivering value to our customers.

### TL;DR



**Business perspective - **



**Customers perspective - **



**How is the problem allowed to happen?'**

The challenge of repeat breakdowns at British Gas persists due to several contributing factors, including deficient procurement checks and insufficient field training. Furthermore, as the customers' homes operate as black boxes, it becomes arduous to track and monitor all activities, leading to a dearth of knowledge concerning the cause of breakdowns. This inadequate understanding makes it difficult to forestall these issues from arising.

**How is something allowed to persist?'**

It is imperative that we adopt a scientific and data-driven approach to comprehensively understand our current situation.

Lacking a comprehensive system for tracking and monitoring the parts installed and improving the notes taken by engineers during their visits to identify the causes of breakdowns, we will continue to lack the necessary data collection to enhance our service offering. 

{{< figure src="image001-01.png" caption="Breaking down a problem" >}}


### What is the problem, Is it a problem worth solving ...

# What is Hedging ...

- Our stakeholder approaches us with the problem 'Are breakdowns predictable?'

The short answer, if I was a betting man, would be 'I think so'. Perhaps another answer could involve
answering the questions with a series of questions:

1) Why are you asking?
2) What problem are you trying to solve?
3) Is it a problem worth solving?
4) Do we collect the data --- data collection is huge here!!

Effects things have on other are sometimes indirect. Let's take an example
involving a soccer ball and a broken glass. Sometimes, you will break a glass by
shooting the ball right onto it. But sometimes not. Sometimes, the ball will
land next to a cat, a cat peacefully sleeping on someone's lap. Sometimes, the 
cat will end up scared which will result in a jump right onto a table, table 
on which was the glass[^1]. Indirect.


------------------------------------------------------------------------

{{< figure src="img/Agent_Tenure.jpg" caption="Average Agent Tenure and volumes of Agents by Tenure" >}}

------------------------------------------------------------------------


# Is this a problem? Is it worth solving?

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
