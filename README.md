# Group-cloud-QA3

## Introduction
### Design specification:
Design and implement a solution for automating the development workflows and deployments of an unfamiliar application in a restricted timeframe. 
We were given a vet clinic web app with separate front and backend infrastructures. This application was written in a mix of Java and TypeScript.
The goal was to create a CI/CD pipeline, utilising the tools, systems and principals we had learned up until now.
For this to work, the group has utilised the following architecture: <br/>
- IAAS - Terraform to create the AWS ecosystem and Configure the environment of the Virtual machines.
- EKS to orchestrate the containers which will run the applications.
- CI Server - Jenkins functioning as pipeline with Webhooks from the version control GIt Hub, to trigger builds.<br/>
Through this presentation we hope to demonstrate;
- A working knowledge of tools including terraform and kubernetes
- The ability to work effectively on the GCP plactform
- The use of Agile and DevOps principles
- The ability to work as a self-managed autonomous team
- An understanding of the importance and use of conventions<br/>
<br/>
<br/>

## Project Planning
We used a trello board to create a list of actions and instructions that must be executed in order for us to reach our objective. This was very beneficial as it helps us keep track of what we are doing and what we have left to do. Each person is able to access this board and place each work load in the sections they fit is right. When the designated person finishes the work they have been set, they are able to place it in the completed section.

<p align= "centre">
        <img width="600" height="300" src="images/board.PNG">

As part of our planning stage, a risk assessment was crutial to be carried out as we needed to know what potential hazards and incidents could occur as well as the impact it could leave. We have described a weide variety of scenarios that could occur along with the impact level and who would be responsible for the result which can all be seen below:

<p align= "centre">
        <img width="600" height="300" src="images/risk.PNG">


