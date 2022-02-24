# Azure DevOps Template Scripts
These scripts are examples to performing Veracode SAST analysis within a Azure Devops Pipeline.

## Description
The examples templates produced within this repository are being used against a simple .NET Core application [Verademo](https://github.com/dmedeiros-veracode/verademo-core). This project has several Azure Devops yaml scirpts that use these templates to perform both a scheduled and triggered SAST analysis using the Veracode tools.

## Requirments and Goals
The intent of ...



These examples show how an administrator can use seperation of concenrs to properly template basic steps for use of integration of Veracode SAST tools wihin their SDLC. 

The seperation of Job Tasks and Steps to perform common tasks within an automated pipeline were derived out into two meaningful categories in this example.

### Steps Template 
One of the first templates to produce was the abstract-build steps needed to properly build Verademo for both a production use and a debug version for use with Veracode SAST analysis. 

### Jobs Template
The second set of templates produce were the job templates to perform either a Veracode Pipeline SAST analysis or that of a Veracode Platform SAST analysis. 
