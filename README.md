# Microservices Application Deployment Cost Analysis

This project focuses on deploying a microservices application using various technologies, including Spring Boot, Python Flask, ASP.NET, and React. The application is containerized using Docker and deployed on different cloud platforms such as AWS (EC2, ECS, EKS) and Azure (VMs, Azure Container Service, Azure Kubernetes Service). This README.md file provides an analysis of the cost for each deployment option and predicts the cheapest solution.

# Deployment Options

## AWS Deployment

### EC2 (Elastic Compute Cloud)

Deploy the microservices application on EC2 instances.
Analyze the cost associated with running the required number of EC2 instances, including compute, storage, and network costs.

### ECS (Elastic Container Service)

Containerize the microservices using Docker and deploy them on ECS.
Analyze the cost of running ECS clusters, including the cost of EC2 instances, load balancers, and other associated resources.

### EKS (Elastic Kubernetes Service)

Containerize the microservices and deploy them on EKS.
Analyze the cost of running EKS clusters, including the cost of EC2 instances, load balancers, and other associated resources.

## Azure

### Azure VMs (Virtual Machines)

Deploy the microservices application on Azure VMs.
Analyze the cost associated with running the required number of VMs, including compute, storage, and network costs.

### Azure Container Service

Containerize the microservices and deploy them on Azure Container Service.
Analyze the cost of running ACS clusters, including the cost of VMs, load balancers, and other associated resources.

### Azure Kubernetes Service

Containerize the microservices and deploy them on Azure Kubernetes Service.
Analyze the cost of running AKS clusters, including the cost of VMs, load balancers, and other associated resources.

# Cost Analysis

Performed a cost analysis for each deployment option, taking into consideration the following factors:

## Compute resources:

Analyzed the cost of running the required number of instances/VMs for each deployment option.

## Storage:

Considered the cost of storage for persistent data used by the microservices.

## Network:

Evaluated the cost of data transfer and network resources.

## Load balancing:

Factored in the cost of load balancers or ingress controllers, if applicable.

## Other associated services:

Considered other additional services or resources required for each deployment option.

## Predicting the Cheapest Solution

Based on the cost analysis, compared the overall costs for each deployment option and predicted the cheapest solution for deploying the microservices application. Considered the performance, scalability, and flexibility aspects of each option, along with the cost factor, to make an informed decision.

# License

This project is licensed under the MIT License. Please see the LICENSE.md file for more details.
