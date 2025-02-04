# **Automated Deployments**

## Definition

Automated Deployments are a pipeline of self-validating builds and subsequent deployment process to test environments and production that is fully scripted. Deployable artifacts are built once, then the same versioned artifact is deployed in each environment with environment-specific configuration.

We need fast feedback to ensure changes that we are making function correctly and do not introduce defects. To have confidence in this feedback, we need the repeatability from scripted environment configuration and deployment.

## How to I achieve Automated Deployments?

Automated Deployments depend on deployment artifacts being build once. This release candidate artifact is then deployed using scripted steps to deploy the software, configuration, and infrastructure for a component to all environments using a deployment pipeline.

Because manual input is prone to error and leads to unrepeatable processes, there is no manual intervention for this pipeline. This pipeline includes stages to verify that the deployment was successful and the component is performing as expected in each environment. If the deployment is not operating as expected the pipeline stops.

## How do I measure outcomes of Fast Automated Deployments?

Automated Deployments have deployment errors from humans making mistakes. Where there are mistakes they are easy to revert by redeploying the previous commit or candidate in production using the automated pipeline.

DORA4 measures of Mean Time to Recovery and Change Failure Rate are both good measures for Automated Deployments.

## Crawl - Walk - Run

| Phase | Activity | Measure |
| ----- | -------- | ------- |
| **Crawl** | -Application is deployed via a pipeline without further input from a human. <br>- Configuration is deployed to all environments without further input from a human.  |  **MTTR:** 2+ hours <br> **Change Failure Rate:** 16-30%  |
| **Walk** | -Application is deployed to all environments via a pipeline without further input from a human. <br>- Configuration is deployed to all environments  via a pipeline without further input from a human. | **MTTR:** 1+ hours <br> **Change Failure Rate:** 7-15% |
| **Run** | -Application is deployed to all environments via a pipeline without further input from a human. <br>- Configuration is deployed to all environments  via a pipeline without further input from a human. <br> * Infrastructure is deployed to all environments  via a pipeline without further input from a human.  | **MTTR:** <15 min <br> **Change Failure Rate:** 0-7%  |
