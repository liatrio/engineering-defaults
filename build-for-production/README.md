# **Build for Production**

## Definition

Building for Production is about being proscriptive about how you are going to work and what it means for work to be done. Work is not done until it is ready to be operated and maintained in production. The team only builds software that it is prepared to deploy to production or throw away as a prototype.

Teams that build for production ensure that all the work they are building is observable and supportable in production. These expectations are part of the acceptance criteria for all stories. Logs are generated, traces are stitched, and metrics are gathered from the beginning and updated with each change as needed. The teams partners with product to know what is expected from the system. SLIs and SLOs are defined, dashboards created, and alerting configured. The team knows what to do when there is an alert.

It’s much harder to add observability and supportability ‘hooks’ after a feature is complete and usually requires significant refactoring. Putting a minimum set of observability and runbooks/KB in place before shipping to production increases resilience of the system, and allows for faster feedback.

The 2022 State of DevOps report found "when a service is unreliable, users won’t benefit from pushing code faster into that fragile context." This means that benefits of the other Sensible Defaults can be limited (or unlocked) by how the team is Building for Production.

## How to I achieve Build for Production?

### Story Level

Define a Definition of Done for stories that includes:

1. Observability:
   1. How the value provided by the story will be measured in metrics
   1. Logging, tracing, and metrics are emitted from the changed code
   1. Monitoring and alerting are configured for the metrics emitted
1. Supportability:
   1. The logs created are valuable and actionable.
   1. Runbooks are updated as needed for team member on-call

### Component Level

For each component the team owns there are Service Level Indicators (SLIs) defined and Service Level Objectives (SLOs) defined. These SLIs are determined and SLOs defined based on technical experience with the technologies used to build the component. An SLI dashboard exists for each component. Automatic alerting is established for SLOs.

### Service Level

For each service the team owns there are Service Level Indicators (SLIs) defined and Service Level Objectives (SLOs) defined. These SLIs are determined and SLOs defined in collaboration with the Product Owner based on business needs and expectations. An SLI dashboard exists for each service. Automatic alerting is established for SLOs.

### Team Level

A team building for production will regularly conduct Failure Mode and Effect Analysis (FMEA) to find and mitigate ways their systems might fail. They will also routinely conduct gameday exercises where they practice responding to failure.

## How do I measure outcomes of Build for Production?

The primary indicator of greater building for production is reduced Mean Time to Detect and Mean Time to Respond. Another measure is how often you are told by someone or someone else's metrics that there is a problem vs how often you are told directly there is a problem by your alerting.

### Mean Time to Detect

How long does it take for your monitoring and alerting detect a problem.

### Mean Time to Respond

How long does it take for your team to respond a problem.

## Crawl - Walk - Run

| Phase | Activity | Measure |
| ----- | -------- | ------- |
| **Crawl** | - Definition of Done includes Observability and Supportability checks. | - Mean Time to Detect: < 30 min <br> - Mean Time to respond: < 1 hour <br>-  Percent of incidents detected by team: > 50% |
| **Walk** | - SLIs and SLOs are defined for each service and component the team owns. <br>-  Dashboards and alerts exist for each service and component's SLIs and SLOs. <br> -  Definition of Done includes Observability and Supportability checks.   | -  Mean Time to Detect: < 10 min <br> - Mean Time to respond: < 30 min <br>-  Percent of incidents detected by team: > 80%  |
| **Run** | - SLIs and SLOs are defined for each service and component the team owns. <br>-  Dashboards and alerts exist for each service and component's SLIs and SLOs. <br> - Definition of Done includes Observability and Supportability checks. <br>-  Team regularly has FMEA with Reliability Engineering. <br> -  Team conducts Gameday Exercises on a routine basis.  | -  Mean Time to Detect: < 5 min <br> - Mean Time to respond: < 15 min <br>-  Percent of incidents detected by team: > 95%  |

## Useful Resources

* [Enterprise Roadmap to SRE](https://sre.google/resources/practices-and-processes/enterprise-roadmap-to-sre/)
