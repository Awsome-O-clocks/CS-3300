# Definition and Concept

***

## Concept

**Behavior Driven Development** (BDD) is a combination of **Test Driven Development** (TDD) and **Acceptance Test Driven Development** (ATDD). This is a ***BUISNESS-FACING MODEL***, that attempts to describe the behavior of a *Scenario* or *Story*. This is also referenced as the **user's presepective**, and *test-first* practice. BDD becomes a continuous integrated system with test*automation*, enabling an aspect of [***Continuous Delivery***](https://scaledagileframework.com/release-on-demand/).

There are 3 perspectives when BDD is being implemented:
- **Customer-base**: Understand the customer and business needs and the desirability and viability of requirements.
- **Development-base**: Solution and technological feasibility.
- **Test-based**: Considers exceptions, edge cases, and boundary conditions for the different behaviors.

The main goal of this process is to create a shared understanding of requirements between the business and the Developers. The following are goals to of BDD:

1. The goal is to apply the ***five why's*** or ***Given-When-Then (GWT)*** principles to each proposed user story.

![77f6fdd765f0aebd58dd6fb73ff7839d.png](../_resources/77f6fdd765f0aebd58dd6fb73ff7839d.png)

This is to relay clear and precise outcome to each user story.

2. Thinking and looking from "the outside in", in other words ensuring that only the behaviors which are suppose to reach the outcome the business wants.
3. Descriptive behavior in a single notation that is directly accessible to experts, testers, and developers, to improve communication.
4. Apply all the way to the lowest abstractions of the software.

[BDD Introduction](https://dannorth.net/introducing-bdd/)

[AgileFramework](https://scaledagileframework.com/behavior-driven-development/)

***

## The Process

There are three phases in the process, these are also know as ATDD and TDD or (***Specification by Example*** (SBE)):
1. Discovery
2. Formulation
	a. Acceptance criteria is made here
4. Automation
	a. Test Cases are formed here

There are many different methods of executing this process and working the same basic principles. Two were given at the top of the page **5W's** and **GWT**, keep in min **SRP** and **DRY**.

### Story Cases GWT BDD Discovery and Formulation Example

**Scenario**: Accessing user Bank Login

*USER view*
**As a {USER}**,
**I want to**: Access my web dashboard
**So That**: I can perform financial actions remotely

**Acceptance Criteria:**
**Given**: User name and password
**When**: The customer logs in successfully
**Then**: Allowed to perform financial actions
**and**: Keeps access till they logout
**and**: ...ETC

**Extended from first acceptance criteria**:
**Given**: User name no password
**When**: the customer logs in
**Then**: The user is denied access
**and**: Prompted to re-enter.

>:warning: **Key Steps From BDD**
>1. Think about the behaviors that the implementation requires. Select a behavior to implement.
>2. Write test that validates the behavior. **THIS IS THE ACCEPTANCE CRITERIA**
>3. Add only enough code to make new test case and all previous test cases pass
>4. Refactor code to create to keep with **DRY**.
>5. Select the next requirement and repeat.

***

## Automating Acceptance Tests

Automation frameworks like **Cucumber** and **Framework for Integrated Testing’ (FIT)**, can be used to support this syntax structure. Continuous delivery should be ensure and tests should be automated wherever possible.

***
***

## References:

### Readings

[IBM TDD](https://www.ibm.com/cloud/architecture/content/course/test-driven-development)
[IBM BDD](https://www.ibm.com/garage/method/practices/code/practice_behavior_driven_development/)
[Scaledagileframework](https://scaledagileframework.com/behavior-driven-development/)
[BDD Framework: A Complete Tutorial](https://www.softwaretestinghelp.com/bdd-framework/)
[Agile Alliance](https://www.agilealliance.org/glossary/bdd/)
[Geeks for Geeks](https://www.geeksforgeeks.org/behavioral-driven-development-bdd-in-software-engineering/#)

### Tools
[Cucumber](https://cucumber.io/)
[Behavior Driven Development - Tools](https://www.tutorialspoint.com/behavior_driven_development/behavior_driven_development_tools.htm)