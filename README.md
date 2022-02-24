# Azure DevOps Template Scripts
These scripts are examples to performing Veracode SAST analysis within a Azure Devops Pipelines.

## Description
The examples templates produced within this repository are being with a simple .NET Core application project [verademo-core](https://github.com/dmedeiros-veracode/verademo-core). This project is used to demostrate intgration with Veracode security tools.

This repository has several Azure Devops yaml template scirpts that are referenced by the [verademo-core](https://github.com/dmedeiros-veracode/verademo-core) to perform both a SAST analysis with the Platform and Pipeline SAST tools.

## Goal and Requirments
The intent of this repository is to present templates to satisfy the goals and the requirement for the [verademo-core](https://github.com/dmedeiros-veracode/verademo-core) project as it evolves as a representation of CI/CD integration best practices using Veracode.

The examples within this repository show how an administrator can use seperation of concenrs to properly template basic steps. That can simplify and be reused for use of integration of Veracode tools wihin their SDLC. 

The seperation of Job Tasks and Steps to perform common tasks within an automated pipeline were derived out into two categories.

### Steps Templates 
- ***abstract-build-steps.yml***
: A steps template that abstracts out all the needed conditions to properly compile and prep the verademo-code application for both a production and debug build.

### Jobs Templates
- ***veracode-sast-platform-job.yml***
: A job template that performs a Veracode Platform SAST analysis for the artifact passed to it.
- ***veracode-sast-pipeline-job.yml***
: A job template that performs a Veracode Pipeline SAST analysis for the artifact passed to it.