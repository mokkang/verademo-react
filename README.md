# Verademo React Application for Azure DevOps

## Project Description

This application repository was created to illustrate how to properly use Veracode Analysis tools within the a Software Development Lifecycle (SDLC). The examples illustrated here utilize the concept of separation of concerns for CI/CD administration.

The Verademo application example is a simple .NET Core web application with a Angular Front End. In this example both the front end content and simple back end content are bother submitted to the same application portfolio. In a larger application these should be further distributed out into more application portfolios.

>[!NOTE]
>The demo application does not have any major weaknesses or vulnerabilities reported within the main branch. As the purpose of this project is to illustrate integration of the Veracode Tools.

## Azure DevOps Project
The azure devops project and pipelines used to build and analyze this demonstration application is located within this project on Azure DevOps: [Veracodemo-React](https://dev.azure.com/veracode-demonstration/verademo-react)

### Pipeline Examples
The examples for each of the pipelines within the main line branch are only a demonstration of a successful path through the SDLC for each case. The Verademo application within the main branch does not container any weaknesses or vulnerabilities to demonstrate any strategy or flow to addressing weaknesses.

#### Azure Pipeline Activity
Pipeline | Script | Status
------ | ------   |----
Scheduled Daily Release Candidate Build from Main branch| azure-scheduled-pipelines.yml | [![Build Status](https://dev.azure.com/veracode-demonstration/verademo-react/_apis/build/status/Scheduled%20Daily%20Release%20Candidate%20Build%20from%20Main%20branch?repoName=dmedeiros-veracode%2Fverademo-react&branchName=main)](https://dev.azure.com/veracode-demonstration/verademo-react/_build/latest?definitionId=30&repoName=dmedeiros-veracode%2Fverademo-react&branchName=main)
Pull Requests Analyses |asure-pull-request-pipelines.yml|[![Build Status](https://dev.azure.com/veracode-demonstration/verademo-react/_apis/build/status/Pull-Request%20for%20Verademo-React?repoName=dmedeiros-veracode%2Fverademo-react&branchName=main)](https://dev.azure.com/veracode-demonstration/verademo-react/_build/latest?definitionId=29&repoName=dmedeiros-veracode%2Fverademo-react&branchName=main)
# Pipeline Examples

### SAST Plarform/Sandbox Analysis
To use the template for running Veracode Platform SAST analysis within Azure DevOps. The following information must be provided to the template during execution.
 - Artifact
 - Service Connection


In the Azure Domain Settings under Service Connection create a Veracode Analysis Center Service Connection. Configure with appropriate Veracode API ID and Veracode API Key.

[Service Connection](https://docs.veracode.com/r/Create_a_Service_Connection_in_Azure_DevOps)




### SAST Pipeline Analysis
To use the template for running Veracode Pipeline SAST analysis within Azure DevOps. The following information must be provided to the template during execution.
 - Artifact
 - VERACODE_API_ID
 - VERACODE_API_KEY
 - Policy
 - Baseline File


### SCA Agent
SRCCLR_API_TOKEN Set to the token value

 - Repo Url or Content
 - SRCCLR_API_TOKEN
  

The sample application

## Service Connection

Veracode SaaS Connection == id key
dmedeiros-veracode

azure-scheduled-pipeline.yml
azure-pull-request.pipelines.yml

#### Azure DevOps Pipeline as Code

The sample scripts ei

[Azure DevOps Script Repository](https://github.com/dmedeiros-veracode/devops-scripts-azure-devops.git)


https://dev.azure.com/veracode-demonstration/verademo-azure


Create in the Azure Project Library a library group that is called "Veracode Credentials". Configure the variable group to contain two secret variables:
- VERACODE_API_ID
- VERACODE_API_KEY

Enter in the values for each and select that the information is secret by clicking on the lock when done entering.

>[!NOTE] 
>More information about [Azure Library Groups](https://learn.microsoft.com/en-us/azure/devops/pipelines/library/?view=azure-devops)
