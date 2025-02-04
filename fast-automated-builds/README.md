# **Fast Automated Builds**

## Definition

Fast automated builds are builds that quickly execute all the steps needed from commit to deployment of the changed code in the development environment.

Fast automated builds enable teams to get quick feedback on code changes. These builds execute on the developers machine providing quick feedback in short loops to the developer as the make changes. These steps are automated and are execute as the Continuous Integration process providing feedback about the change integrated with the rest of the team's work in a more controlled environment. Changes that pass these changes become release candidates in the Continuous Delivery process.

## How to I achieve fast automated builds

Automated builds occur locally and in the pipeline.

- Every developer should have the local environment setup with a build configuration (Gradle, Maven, Docker, etc)
- Utilize git pre-commit or pre-push hooks for validation
- Leverage existing platform pipeline for automated build, test, and deployment

## How do I measure outcomes of Fast Automated Builds?

- Primary Measurement: code change to dev deployment
  - Calculation (CircleCI): duration of jobs in workflow
  - Evaluation
    - Good : 5-15 minutes
    - Improvement: 15-30 minutes
    - Concern: 30+ minutes

A shorter build and pipeline run means faster feedback. However, teams should not be encouraged to skip necessarily testing and validation in order to get a faster time. For this reason, it should be expected that there is a minimum build time that accounts for adequate validation.

## Crawl - Walk - Run

| Phase | Activity | Measure |
| ----- | -------- | ------- |
| **Crawl** | - All steps needed to build and verify the deployment artifact are executed with a single command. <br> - The same command is used in the CI/CD pipeline to build and verify the artifact.  | - Build time in CI process is measured. <br>-  Failure rate in the CI process is measured. |
| **Walk** | - All steps needed to build and verify the deployment artifact are executed with a single command. <br>-  Git-hooks are configured to execute the build before changes leave a developers machine. <br> * The same command is used in the CI/CD pipeline to build and verify the artifact.  | -  Build time in CI process is measured. <br> - Failure rate in the CI process is measured. <br>-  Changes in build time and failure rate from trend are measured.   |
| **Run** | - All steps needed to build and verify the deployment artifact are executed with a single command. <br>-  Git-hooks are configured to execute the build before changes leave a developers machine. <br> - The same command is used in the CI/CD pipeline to build and verify the artifact. <br>-  Build times are regularly reviewed to find any opportunities to optimize build time. | - Build time in CI process and developer machines is measured. <br>-  Failure rate in the CI process and developer machines is measured. <br> -  Changes in build time and failure rate from trend are measured.  |

## What Others are Sayings

> Continuous Integration, often referred to as CI, is a part of the outer loop development process that automatically builds an artifact and runs a series of automated tests for every code commit in an effort to assess whether code is ready to be deployed. This process provides quick, automated feedback to the developer, allowing them to operate with higher levels of confidence. CI is a key part of taking code from a developer’s workstation to production. As in previous years, CI is shown to drive delivery performance. High performers who meet reliability targets are 1.4x more likely to use CI than others. -- State of DevOps 2022
