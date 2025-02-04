# **Team Ownership of Quality**

## Definition

Team ownership of quality means that all team members share equal accountability for their responsibilities and the quality of their work. In order to achieve continuous delivery and reduce the mean time to validate a change and enable fast feedback at every phase of the software delivery life cycle (SDLC) team should embrace a team ownership of quality mindset and continuous testing practices​.

One of main attributes of Team ownership of quality is achieving continuous testing

**Continuous testing** is a software testing methodology that helps identify and address risks at all stages of the development pipeline. In other words, it means testing all potential code changes as early as possible. The goal of continuous testing is to minimize business risk and impact on users.​

Continuous testing is critical to continuous delivery so that we can: ​

- Improve Quality​
- Accelerate Releases​
- Reduce Cost of Failure ​
- Improve Business Outcomes ​

## How to achieve Team Ownership Of Quality

Commitment for quality from the team, leadership and product​

- Every team member is responsible for quality, and testing should not be treated as a task or as a activity performed by a specific role​
- Everyone on the team is responsible to code, test & deliver including unit, functional and non-functional tests​
- Enable QA professional to be voice of the customer and demonstrate quality at every phase of the SDLC​

Teams need to own the outcomes, this includes delivering with quality and reducing the mean time to validate a change​

- Test your app/app components independently and completely including integration with upstream, downstream, external systems, etc.​
- Follow Continuous testing practices by testing early and often, integrate with CI/CD pipeline to enable continuous delivery.​
- Enable QA professional to be voice of the customer and demonstrate quality at every phase of the SDLC

## How to measure outcomes of Team Ownership of Quality

- **Escaped Defect Rate:** Reduction in the number of bugs that reach production. Escaped defect rate is calculated by the percentage of defects found in testing before production (See Resource link below).
- **Lead Time:** Reduction in lead time for changes
- **Change Failure Rate**  Percentage of changes to release need to be rolled back or cause a service outage?

## Crawl - Walk - Run

| Phase     | Activity                                                                                                                                                                                                                                                                                                                                   | Measure                                                                                                                               |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| **Crawl** | - Establish continuous testing as a goal. <br> - Increase test automation coverage. <br> - Establish unit testing for commits. <br> - Leverage CI/CD tools for build, testing, and deployment. <br> - Establish measurements for escaped defect rate and change failure rate. <br> - Reduce reliance on manual testing and external teams. | - Change failure rate is measured. <br> - Escaped defect rate is measured. <br> - Lead time for change is between 1 week and a month. |
| **Walk**  | - Establish continuous testing as a best practice. <br> - Integrate all automated testing into CI/CD pipeline <br> - Testing every commit through full stack test automation. <br> - Identify defects during and after production deployment. <br> - Minimize reliance on manual testing phase and external teams.                         | - Change failure rate is 16-30%. <br> - Escaped defect rate is > 85%.<br> - Lead time for changes is between 1 day and 1 week.        |
| **Run**   | - Establish continuous testing as the norm. <br> - Practice TDD, testing locally and on every commit. <br> - Fully automated CI/CD pipeline with high test coverage. <br> - Eliminate reliance on external team testing and manual testing phase.                                                                                          | - Change failure rate is 0- 15%. <br> - Escaped defect rate > 90%.<br> - Lead time for change is between hours and 1 day.             |

## Useful resources

- [How to Measure Defect Escape Rate](https://stackify.com/measure-defect-escape-rate/)
