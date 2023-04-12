# DevOps Bootcamp Capstone Project
- [DevOps Bootcamp Capstone Project](#devops-bootcamp-capstone-project)
  - [Description](#description)
  - [Features and Requirements](#features-and-requirements)
  - [Guidelines](#guidelines)
  - [Resources](#resources)
  - [Pre-requisites](#pre-requisites)
  - [1. Setup your development environment](#1-setup-your-development-environment)
    - [Repository](#repository)
    - [Application](#application)
  - [2. Containerize the application](#2-containerize-the-application)
  - [3. Create a CI Pipeline](#3-create-a-ci-pipeline)
  - [4. Update "Hello World!" to "Hello DevOps!"](#4-update-hello-world-to-hello-devops)

## Description
In this project, you will be using some of the tools and technologies you have learned during the bootcamp.

## Containerizing an Application with Docker

The first step would be to identify the application to be containerized and prepare its environment, including installing all necessary dependencies and libraries. A Dockerfile would then be created, defining the container's configuration, including the base image, software dependencies (package), and any necessary settings.

[Dockerfile](https://github.com/jonathannava/DevOps/blob/main/capstone_project/hello-world/Dockerfile)

<p align="center">
<img src="https://user-images.githubusercontent.com/7119224/231537588-c170edfa-fefe-4912-a77b-be620795a257.png"  width="20%">
</p>
Once the Dockerfile is complete, the container can be built using Docker commands. After building the container, it can be run on a Docker engine, and the application can be accessed through the localhost.
Built using Docker
<p align="center">
<img src="https://user-images.githubusercontent.com/7119224/231540890-3796a8b3-eac0-4eee-9061-02b3d130aef2.png" width="80%">
</p>
Run a Docker container
<p align="center">
<img src="https://user-images.githubusercontent.com/7119224/231541687-22e8ab4e-76e8-4527-a337-a5cdee82f7dd.png" width="80%">
</p>
Aplication running (localhost:3000)
<p align="center">
<img src="https://user-images.githubusercontent.com/7119224/231542674-2edc992f-40f4-4338-9c93-28ea1e455f8a.png" width="50%">
</p>


## Building CI Pipeline with GitHub Actions
[workflow](https://github.com/jonathannava/DevOps/blob/main/.github/workflows/ci.yaml)

The pipeline will be set up to automatically trigger on every push and pull request to the repository (main). If the tests pass successfully, the pipeline will proceed to build the container for the application.

<p align="center">
<img src="https://user-images.githubusercontent.com/7119224/231545311-a0e65255-2788-40a3-85f7-4d98562af4e6.png" width="50%">
</p>
RUNS

<p align="center">
<img src="https://user-images.githubusercontent.com/7119224/231545928-eb5b490a-46ce-4314-b8c7-98b108ed30eb.png" width="50%">
</p>

## Update the node js application using ansible

[Playbook Ansible](https://github.com/jonathannava/DevOps/blob/main/capstone_project/hello-world/playbook.yml)

The final step of this project involves setting up an Ansible playbook to manage the Docker container running the Node.js application.
The inventory file was created to establish a local connection with the Docker container, after which the playbook was created using Ansible to make the text change. The SED command was then executed inside the Docker container.

<p align="center">
<img src="https://user-images.githubusercontent.com/7119224/231550126-0b708b5a-e671-4e0f-b773-7a74081ef33f.png" width="50%">
</p>
<p align="center">
<img src="https://user-images.githubusercontent.com/7119224/231547684-8dcb3910-c453-4223-8844-a8ea2f349293.png" width="50%">
</p>

Overall, this part demonstrates how to automate the process of updating a Node.js application running in a Docker container using Ansible, making it easy to maintain and update the application with minimal manual intervention.

<p align="center">
<img src="https://user-images.githubusercontent.com/7119224/231550330-58b91f06-9e62-4d92-863c-e51ba0eee7d1.png" width="50%">
</p>

## Features and Requirements
- Node Js application will be provided
- Containerization using docker
- CI pipeline using Github Actions (Including automated testing,build)
- Update the Node JS application content using Ansible

## Guidelines
- Instruction for the project will be available on Thursday, April 6th
- One week to deliver the project. Please deliver the project no later than Monday, April 17.
- Send the repo link or project to talent@itjuana.com
- After delivering the trainers will review the content, if you pass you’ll get a badge recognizing your knowledge as DevOps Engineer.
- You’ll know the results via email from the ITJ Talent Team.
- Any questions or comments, please post it in the [WhatsApp group](https://chat.whatsapp.com/KiirrKYAJ3SINrDn1pLZ7C)

## Resources
[Bootcamp Presentations](https://github.com/itjuana-bootcamp/DevOps/tree/main/Presentations)

## Pre-requisites

* [Docker](https://docs.docker.com/desktop/) installed
  * `docker --version` should show the docker version
* [Git](https://github.com/git-guides/install-git) installed
  * `git --version` should show the git version
* [Node JS](https://nodejs.org/en/download/package-manager/)
  * `npm version` should show the node version
* Have a [github account](https://github.com/join)
* Code editor of your preference - [VS Code](https://code.visualstudio.com/download) recommended

## 1. Setup your development environment

### Repository
- Go to the github repository https://github.com/itjuana-bootcamp/DevOps
- Fork the repository
NOTE: From here on, whenever we say repository , that refers to your forked repository.
- Clone the repository : `git clone git@github.com:<githubaccount>/DevOps.git`

### Application
- Go to folder `hello-world`
- Run `npm install` .
- Run `npm test` . All tests need to pass.
- Run `npm start` to run the application.
- Check http://localhost:3000 is reachable and displaying "Hello World!"

## 2. Containerize the application
- Using docker, containerize the application.
- Build the container and run it to make the application available on http://localhost:3000

## 3. Create a CI Pipeline 
- Create a CI pipeline which 
     - will trigger on push and on pull request
     - Run the tests
     - Only if tests are success, build the container

## 4. Update "Hello World!" to "Hello DevOps!"
- Update the node js application to display "Hello DevOps!" instead of "Hello World!" using ansible.

