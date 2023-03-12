---
date: 2022-12-17

title: Project Success - One pager
subtitle: |
  “Foresight is not about predicting the future, it’s about minimizing surprise. - Karl Schroeder"

summary: |
  “Foresight is not about predicting the future, it’s about minimizing surprise. - Karl Schroeder"

description: |
    my journey managing a non-tech graduate in the tech field of data science.

author: Hamzah Javaid

show_post_date: true
show_author_byline: true

format: hugo

draft: false

freeze: auto
tags:
- behaviour
- pyscology

---

### Drawing the Map to Your Destination

>   **“Foresight is not about predicting the future, it’s about minimizing surprise.”** - Karl Schroeder

If there is anything 5 years of applied data science has taught me, it's so important to have a clear understanding of the destination you're aiming for. Just like planning a trip, this involves drawing a map that outlines the steps needed to get there. In the context of a Data Science project, this means defining your goals and outlining the key steps needed to achieve them.

- What's your Why?

> **“Management is doing things right; leadership is doing the right things.”** - Peter Drucker

It's so easy to jump straight into weeds - discussing the models, getting started with the EDA - without ever asking "Why?".
 - What is the problem you are trying to solve?
 - Is it even worth solving/solvable?
 - Why are we trying to solve it?

The data science solution could potentially impact only a small group of customers and have limited long-term potential. Perhaps the ask isn't even a problem or not significant enough to solve. It's crucial to take a step back and reflect on the project's purpose and rationale. Your plan should define clear goals for your project and break them into actionable steps. This can then be followed up with a one-page overview to communicate the steps and milestones to stakeholders and team members. Be sure to also identify potential roadblocks (e.g. data quality issues, technical constraints) and plan proactively for them to avoid project derailment.

{{< figure src="img/mapp.jpg" caption="Draw a map, have a clear goal and roadmap" >}}

--------------------
### Choose the approach wisely

- Working Backwards 

According the "Working Backwards" authors Colin Bryar and Bill Carr, "in a working-backwards world, starting with the customer and working backwards is the only way to build products and services that customers actually want." The approach is centered around the customer's needs and incorporates sentiments of testing and validation during the development process. As Bryar and Carr explain, "The sooner you can validate an assumption, the sooner you can move on to the next assumption or pivot your approach."

This is also emphasised by Peter Drucker in his writing:

> "The purpose of a business is to create a customer. The test of the organisation is its capacity to create customers."

"Build It And They Will Come" is an approach where the team develops the solution with the assumption that there is a demand for it. This approach is useful when there is a high level of certainty that the solution will be useful to customers, and there is no need for further validation.
The "Build It And They Will Come" approach assumes that there is a demand for the product or service, but this is not always the case

{{< figure src="img/working_backwards.jpg" caption="Working Backwards - Colin Bryar and Bill Carr" >}}

--------------------

### What will you deliver?

- Defining the Outcome (What)

Define success by specifying the desired outcome in quantifiable terms. This prevents chasing a moving target and helps decide which projects to pursue. Measuring success through business metrics such as conversion or savings from fraud reduction is crucial.

> ***“If you can’t measure it, you can’t change it.”*** - Peter Drucker

Limited resources (e.g. time, money, external support) require prioritisation, so it is critical to choose to invest in something more worthwhile instead of pursuing a problem that requires high accuracy.

- Creating a Deliverable: How to Proceed?

To achieve our desired outcomes, we must design a deliverable that meets our intentions and integrates with our current system. For example, an e-commerce platform may seek to improve product discovery and purchase experiences. We can choose to enhance search, recommendations, or email campaigns. If we opt for recommendations, we need to decide on the deployment method, such as using a daily updating cache or a service that accepts input and returns recommendations.

While a detailed plan is unnecessary, we should sketch out the basics to get buy-in from our business, product, and tech teams. 

> It's crucial to receive feedback on this plan to avoid creating a feature-rich deliverable that doesn't deliver results or can't be integrated. 

Avoid developing an overly complex recommender, for instance, if it cannot be integrated into the system.

-------------------------------

### Constraints vs. Boundaries

One of the most important considerations in any Data Science project is the distinction between constraints and boundaries. While constraints refer to limitations imposed by the available data, resources, and time, boundaries refer to ethical and moral considerations that guide your approach and decision-making.

**Constraints** - such as limited data availability, computing resources, or time constraints. It's important to be realistic about these constraints and to adjust your approach accordingly. This may involve prioritizing certain data sources or analysis techniques, or finding creative solutions to work within your constraints.

The three different types of constraints in a data science project are business, technical, and resource constraints. 

- Business constraints provide a budget and freedom to experiment while adhering to specific limitations.
- Technical constraints involve limitations on latency, throughput, interface, schema, or format that must be adhered to. 
- Resource constraints involve limitations on the amount of compute, platform and memory resources available for the project,

**Boundaries** - refer to ethical and moral considerations that guide your approach and decision-making. This could include considerations around data privacy, bias and fairness, and transparency in your analysis and decision-making. 

{{< figure src="img/boundaries-vs-constraints.jpg" caption="Avoid the constraints, stay within boundaries" >}}

**Growth mindset** - Don't let the concept of boundaries restrict your mindset! When defining boundaries, ensure that you're approaching your project with a growth mindset, rather than a fixed mindset. A growth mindset involves a willingness to learn and adapt based on feedback and new information, while a fixed mindset can lead to rigid and inflexible approaches that are often ineffective.

Finally, it's important to consider the broader societal impacts of your project and to ensure that your approach is aligned with your values and goals. This may involve engaging with stakeholders and experts in your field to gain a deeper understanding of the potential impacts of your work, as well as considering the potential unintended consequences of your approach.

### Part 4: "Steering the Future"

Karl Schroeder's book "Steering the Future" provides valuable insights into the process of planning and executing successful projects. One of the key insights from the book is the importance of working backwards from your goals to determine the steps needed to achieve them.

> Schroeder describes this approach as "backcasting", where you start with a clear vision of your desired end state and work backwards to determine the steps needed to get there. 

This approach can be particularly valuable in Data Science projects, where the complexity of the data and analysis can make it difficult to determine the most effective path forward.

Another important insight from Schroeder's book is the importance of taking a systems thinking approach to your project. This involves looking beyond the immediate problem you're trying to solve and considering the broader context in which your project exists.

> ***By taking a systems thinking approach, you can identify potential risks and opportunities that may impact your project, and develop strategies to mitigate these risks and capitalize on these opportunities.***

### Time-boxing

Part 5: Parkinson's Law and the Importance of Constraints

The traditional approach to project management involves starting with a solution and then estimating the time and resources required for each component. However, this approach is flawed as it can result in an open-ended commitment to resources. 

> "Parkinson's Law states that work expands to fill the time available for its completion."

In the context of Data Science projects, this means that without clear constraints and deadlines, projects can easily become bloated and never reach completion.To avoid this trap, it's important to set clear constraints and deadlines for your project. This may involve defining a clear scope and timeline for your project, and identifying key milestones and deliverables that need to be completed within specific timeframes.

{{< figure src="img/timeboxing.png" caption="Time box your tasks based on your boundaries and constraints" >}}

The time-box will vary across project stages. At the start, tighter time-boxes are required to limit wild goose chases and ensure that the project stays on track. Once there is more certainty of going into production, bigger time-boxes can be allocated.

In addition to setting constraints and deadlines, it's important to embrace the idea of working with limited resources. This may involve using existing data and tools rather than building everything from scratch, or focusing your analysis on a specific subset of data rather than trying to analyze everything at once.

Here could be a few steps:

  1 - Feasibility assessment
  2 - Proof of Concept (POC)
  3 - Deploy to production
  4 - Operational Maintenance

{{< figure src="img/time-boxed-iterations.jpg" caption="Examples of stages Time-boxed events" >}}

### Concluding remarks

Taking the additional thinking and efforts can save a huge amount of effort!
