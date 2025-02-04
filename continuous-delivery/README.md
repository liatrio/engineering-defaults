# **Continuous Delivery**

## Definition

**Continuous Delivery** as a software engineering practice in which teams produce software in short cycles , ensuring that the software can be reliably released at any time and, when releasing the software, doing so automatically. It aims at building, testing, and releasing software with greater speed and quality. The term **Continuous Delivery** can be traced back to the first principal of the [Agile Manifesto (2001)](https://agilemanifesto.org/principles.html)

Continuous Delivery is based upon 3 key ideas

- The reliable, repeatable production of high quality software.
- The application of scientific principles, experimentation, feedback, and learning.
- The Deployment Pipeline as a mechanism to organize and automate the development process.

Here some benefits of Continuous Delivery

- **Accelerated Time to Market:** CD lets us deliver the business value inherent in new software releases to customers more quickly.
- **Building the Right Product & Fast Feedback:** Frequent releases let the product  teams obtain user feedback more quickly. We also find any problems early
- **Improved Productivity and Efficiency:** Significant time savings for developers, testers, operations engineers, etc. through automation.
- **Repeatable and Reliable Releases:** With CD, the deployment process and steps are tested repeatedly before deployment to production. Deploying frequently (whether features are ready to release or not) brings forward any problems with deployment
- **Improved Product Quality:** The number of open bugs and production incidents has decreased significantly.

> According to Dave Farley, in his book [Continuous Delivery Pipelines: How to Build Better Software Faster](https://www.amazon.com/Continuous-Delivery-Pipelines-Better-Software/dp/B096TTQHYM) there are some motivational data supporting Continuous Delivery. (Data is backed by research from "The State of DevOps Reports".
>
> - 44% more time spent on new features
> - 8000x faster deployment lead times
> - 50% less time spent fixing security defects
> - 50$ lower change-failure rate
> - 21% less time spent on unplanned & rework
> - 50% higher market cap growth over 3 years

And as the State of DevOps 2022 report says,
> Continuous delivery (CD) is a software development practice that:
>
> 1. Enables the team to deploy software to production or end users at any time
> 2. Ensures the software is in a deployable state throughout its life-cycle, including when working on new features
> 3. Establishes a fast feedback loop that enables the team to check the quality and deployability of the system, and prioritizes fixing issues blocking deployment.

## How do I achieve Continuous Delivery?

- Continuous Delivery is practiced, meaning each code/config push triggers an automated deployment to production once checks and tests have completed.​
  - When Continuous Delivery is not feasible, production deployments are at least weekly, preferably on-demand as stories/tasks are completed.  ​
- The first production deployment is performed in the first days/weeks of a new project, not deferred until late in delivery.  ​
- The team deploys to all environments, including production on a frequent basis.  ​
- No component goes undeployed for more than a month, even if no change has been required.​
  - Example includes security and patching – with the shift to microservices it's now part of product engineering responsibility
- Fast Feedback loops from our systems (pipelines) and our customers enable us to validate our theories / experiments and more rapidly course correct. Some of the system feedback examples include:
  - Unit Testing, Functional Testing, Non-functional testing, quality and security scanning, telemetry, etc.
- Automation of manual tasks is an enabler to Continuous Delivery, as it frees up time for engineers for solving higher order problems.

## How do I measure Continuous Delivery?

Measures for Continuous Delivery come from the [DORA Metrics](https://grainger.atlassian.net/wiki/spaces/EE/pages/162936363106/DORA+Metrics) which is actively being implemented and used by teams at Grainger. It's important to NOT over focus on speed at the cost of quality of vice versa they both are important and should be balanced.

### Efficiency (Speed)

- **Deployment Frequency** measure how often code is deployed to Production.
- **Lead Time for Change** measure the time between the first commit for a change in the Development environment and the time that change is applied in the Production environment.

### Quality (Safety)

- **Mean Time to Restore Service (MTTR** measure how long it takes an organization to recover from a failure (Incident) in production
- **Change Failure Rate** measure percentage of changes that go into prod that result in degraded service to the end user, and require a subsequent action (hotfix, emergency transport, back out of changes) to correct

## Crawl-Walk-Run

| Phase | Activity| Measure|
| ------ | ------- | ----- |
| **Crawl** | Team deploy to non-prod environments frequently <br> Production deployments are at least weekly | **Deployment Frequency:** Between once per week and once per month <br> **Lead Time for change:** Between 2 weeks and 1 month <br> **MTTR:** 1 business day <br> **Change Failure Rate:** 16-30% |
| **Walk** | Team deploy to non-prod environments frequently <br> Production deployments are on demand as stories are complete | **Deployment Frequency:** Between once per day and once per week <br> **Lead Time for change:** once per day and once per week <br> **MTTR:** 2-8 hours <br> **Change Failure Rate:** 16-30%   |
| **Run** |Team deploy to ALL environments including production daily to multiple times a day |**Deployment Frequency:** On demand and multiple times per day <br> **Lead Time for change:** Less than 1 hour <br> **MTTR:** 1-4 hours <br> **Change Failure Rate:** 0-15%  |

## Useful References

- [Continuous Delivery - Reliable Software Releases through Build, Test, and Deployment Automation](https://www.amazon.com/Continuous-Delivery-Deployment-Automation-Addison-Wesley/dp/0321601912).
- [Continuous Delivery Pipelines: How to Build Better Software Faster](https://www.amazon.com/Continuous-Delivery-Pipelines-Better-Software/dp/B096TTQHYM).
