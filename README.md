# Verademo React Application for Azure DevOps

## Project Description

This application repository was created to illustrate how to properly use Veracode Analysis tools within the a Software Development Lifecycle (SDLC). The examples illustrated here utilize the concept of separation of concerns for CI/CD administration.

The Verademo application example is a simple .NET Core web application with a Angular Front End. In this example both the front end content and simple back end content are bother submitted to the same application portfolio. In a larger application these should be further distributed out into more application portfolios.

>[!NOTE]
>The demo application does not have any major weaknesses or vulnerabilities reported within the main branch. As the purpose of this project is to illustrate integration of the Veracode Tools.

## Azure Pipeline Activity

Pipeline | Script | Status
------ | ------   |----
Scheduled Daily Release Candidate Build from Main branch| azure-scheduled.yml | [![Build Status](https://dev.azure.com/veracode-demonstration/verademo-react/_apis/build/status/Scheduled%20Build%20and%20Analysis%20for%20Verademo%20React?repoName=dmedeiros-veracode%2Fverademo-react&branchName=main)](https://dev.azure.com/veracode-demonstration/verademo-react/_build/latest?definitionId=22&repoName=dmedeiros-veracode%2Fverademo-react&branchName=main)
Pull Request |asure-pull-request.yml|[![Build Status](https://dev.azure.com/veracode-demonstration/verademo-react/_apis/build/status/Pull%20Request%20Build%20and%20Analysis%20for%20Verademo-React?repoName=dmedeiros-veracode%2Fverademo-react&branchName=main)](https://dev.azure.com/veracode-demonstration/verademo-react/_build/latest?definitionId=23&repoName=dmedeiros-veracode%2Fverademo-react&branchName=main)
# Pipeline Examples

The examples for the pipelines within the main line branch are only a demonstration of a successful path through the SDLC in each case. The Verademo application within this branch does not container any weaknesses or vulnerabilities to demonstrate any strategy.

# Setup and Usage

#### SAST Plarform/Sandbox Analysis
In the Azure Domain Settings under Service Connection create a Veracode Analysis Center Service Connection. Configure with appropriate Veracode API ID and Veracode API Key.

#### SAST Pipeline Analysis
Create in the Azure Project Library a library group that is called "Veracode Credentials". Configure the variable group to contain two secret variables:
- VERACODE_API_ID
- VERACODE_API_KEY

#### SCA Agent
SRCCLR_API_TOKEN Set to the token value

The sample application

## Service Connection

Veracode SaaS Connection == id key
dmedeiros-veracode

azure-scheduled-pipeline.yml
azure-pull-request.pipelines.yml

# Azure DevOps Pipeline as Code

The sample scripts ei

[Azure DevOps Script Repository](https://github.com/dmedeiros-veracode/devops-scripts-azure-devops.git)


https://dev.azure.com/veracode-demonstration/verademo-azure
