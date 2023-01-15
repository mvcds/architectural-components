# Architectural Components

> Sofware architecture is about making choices that are costly to change once implemented

We can leverage such costs to our advantage to achieve the goal of the systems we create. For example, if one of our system's requirements is to be fast, we need to create and/or use components that make it fast, and make it difficult to create and/or use components that make it slow. This sounds obvious but is not always easy because a software tends to be non-trivial system.

Our goal with this project is helping you to keep your system requirements in mind, regardless of your experience as an architect.

## What is a system?

For us, a system might be made by 0 or more pieces of code, like the classical combo front- and backend-end, that's why we don't say "software" or "app" in most of this document.

And any system is made of 1 (itself) or more components. The tricky part is that each component is also a system, and converselly any system is a potential component in a different system.

The way components entagle will determine some of caracheteristics of the overall system, such as its predicability and testability, so it's worth exploring the same system from many perspectives in order to understand how you can tweak it for your benefit.

### Why focusing on components?

"Component" here is used loosely to refer to technical systems in order to achieve a good architecture for your systems' current goal.

But in this document we focus on technical components like, but not limited to:

- Language
- Dependencies
  - Products (softwares and apps)
  - Services
  - Libraries
  - Frameworks
- Design patterns
- Data structures
- Methodologies
- Architectural techniques
- Best practices

We strongly believe that by keeping a smart inventory on such components, you can study them to create a good project.

## System Requirement (SR)

A SR is simply what we want our system to do and/or be, business- and/or technical-wise. They are necessary to guide discussions and development towards the goal of the system.

It's also important to say that different parts of the same system might have different SRs, for example, in an e-commerce project, persistency might be interesting for the virtual cart but legally forbidden for saving the user's credit card information. And that SRs can change over time.

### Functional Requirement (FR)

A FR translates into what a user can do within the system. Normally, it will be given by people in non-technical roles.

Examples of FRs include things like: a customer can...

- add a book to their virtual cart
- remove a book from their virtual cart
- checkout their virtual cart

Systems intended to be used by devs/architects also have FRs.

### Cross-Functional Requirement (CFR)

A CFR is generally a purelly-technical type of requirement, you might know it as a "Non-Functional Requirement". They are present in many of our FRs, for example, in a systen where auditability is important, all actions a user takes is logged.

In some cases, we can monitor and measure CFRs to know if a system is healthy.
