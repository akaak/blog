---
layout: post
title: Workflow Systems Anti-Patterns 
categories: [architecture]
---


> **Anti-Pattern** -- An antipattern is just like a pattern, except that instead of a solution it gives something that looks superficially like a solution but isn't one.
    -- Andrew Koenig

When building software applications for workflows and transactional systems involving multiple user roles/personas, several anti-patterns can emerge. These anti-patterns can lead to non-optimal performance, poor user experiences, and overall maintenance challenges. 

These anti-patterns could span different areas of a project: Architectural, Process/User-flow, User Experience/Design, Software Development.



## Architectural/Software Design Anti-Patterns

You architect a **distributed monolith**. This anti-pattern occurs when an application is designed as a distributed system but consists of `tightly` coupled components that lack true independence. This is manifests as high interdependency between services thus changes to one service requires you to update multiple other tightly coupled services. Slows down development, deployment, scaling individual components. 

Over reliance on **Microservices**. Use of microservices even for simple operations or functions of the software leads to unnecessary complexity. This anti-pattern results in excessive number of small services, complicates service management and orchestration requiring higher skill level of your engineers and increased network overhead.

Violation of **Single Responsibility**. The architecture entrusts a single function or microservice take on multiple responsibilities when in fact they should be separated. One example is mixing data access, business logic, and presentation logic within the same component.

- In software design, a single class or object takes too many responsibilities violating the Single Responsibility Principle. Without proper separation of concerns and/or modular architecture, the system becomes hard to understand (`spaghetti code`), maintain and extend.


## Workflow-Specific Anti-Patterns

Ignoring User Roles and Permissions. Failing to properly implement role-based access control (RBAC) can lead to security vulnerabilities and usability issues. A good RBAC model helps organizations to easily manage a governance solution and scales with the organization. This anti-pattern manifests as all users having access to all features, regardless of their role; NOT a good idea in any system. Some arcane code customization is required to allow workflows based on user roles. 

Lack of Flexibility in Workflow Design and required stage gates. Creating overly rigid workflows that don't account for exceptions or variations can result in user frustration and inefficiency. Software updates or customizations to handle various special scenarios. When the project deadlines are in jeopardy, users asked to resort to workarounds to complete tasks.


## User Experience Anti-Patterns

Overemphasizing Persona Details. While personas are essential for understanding user needs, focusing too much on irrelevant details can lead to misguided design decisions[3]. Teams end up creating too many personas, making it difficult to design for specific user needs. Emphasizing demographic information over behavioral data and user tasks and goals.

Ignoring Negative or Non-User Feedback. Failing to consider feedback from users who don't fit the target persona can result in missed opportunities for improvement[3]. This anti-pattern leads to overlooking potential issues that may not be apparent to the target audience. Not able to expand the product's appeal to a broader user base.

NN/g article[4] has a Summary that reads:
> Summary: When based on user research, personas support user-centered design throughout a project’s lifecycle by making characteristics of key user segments more salient.

## Development Process Anti-Patterns

The topic of **Software Development Process** requires its own set of blog articles. But, a couple of items to consider are: software code without meaningful names or explanations can make the code difficult to understand and maintain. Some examples are constants are used throughout the code without context. Lack of code reviews and necessary refactoring as code is evolved over a period of time. Not realizing or having the visibility into the accumulation of technical debt. This decreased code quality over time and increases difficulty in adding new features or fixing bugs. This affects release times and time to market.

For projects that are building workflow systems (for that matter any software applications), it is important to be aware of these anti-patterns. The project team(s) must actively work to avoid them. Quality Assurance (QA) teams and business users covering multiple user roles and personas should test and validate emd-to-end scenarios. A project may introduce these anti-patterns at various phases of the project and it is advisable to be mindful and proactively look for these anti-patterns in your projects. 

**References:**

[1] Anti Pattern
<br>
<a href="https://martinfowler.com/bliki/AntiPattern.html">https://martinfowler.com/bliki/AntiPattern.html</a>

[2] Microservices adoption antipatterns
<br>
<a href="https://microservices.io/microservices/antipatterns/-/the/series/2019/06/18/microservices-adoption-antipatterns.html_">https://microservices.io/microservices/antipatterns/-/the/series/2019/06/18/microservices-adoption-antipatterns.html_</a>

[3] The Ultimate Guide to Developing Personas for a Custom Software Development Project
<br>
<a href="https://www.npgroup.net/blog/ultimate-guide-developing-personas-custom-software-development-project/">https://www.npgroup.net/blog/ultimate-guide-developing-personas-custom-software-development-project/</a>

[4] Personas Make Users Memorable for Product Team Members
<br>
<a href="https://www.nngroup.com/articles/persona/">https://www.nngroup.com/articles/persona/</a>

[5] The Joel Test: 12 Steps to Better Code
<br>
<a href="https://www.joelonsoftware.com/2000/08/09/the-joel-test-12-steps-to-better-code/">https://www.joelonsoftware.com/2000/08/09/the-joel-test-12-steps-to-better-code/</a>
