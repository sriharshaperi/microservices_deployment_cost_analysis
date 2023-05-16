# Microservices Application Deployment Cost Analysis

This project focuses on deploying a microservices application using various technologies, including Spring Boot, Python Flask, ASP.NET, and React. The application is containerized using Docker and deployed on different cloud platforms such as AWS (EC2, ECS, EKS) and Azure (VMs, Azure Container Service, Azure Kubernetes Service). This README.md file provides an analysis of the cost for each deployment option and predicts the cheapest solution.

# Deployment Options

## AWS Deployment

### EC2 (Elastic Compute Cloud)

Deployed the microservices application on EC2 instances.
Analyze the cost associated with running the required number of EC2 instances, including compute, storage, and network costs.

### ECS (Elastic Container Service)

Containerized the microservices using Docker and deploy them on ECS.
Analyze the cost of running ECS clusters, including the cost of EC2 instances, load balancers, and other associated resources.

### EKS (Elastic Kubernetes Service)

Containerized the microservices and deploy them on EKS.
Analyze the cost of running EKS clusters, including the cost of EC2 instances, load balancers, and other associated resources.

### Comparision & Cost Analysis of AWS ECS with AWS EKS

1. Networking

EKS allows up to 750 Pods per instance whereas ECS accommodates only up to a maximum of 120 tasks per instance, this is one of the important points to understand when considering the difference between Amazon ECS vs EKS.

2. Namespaces

Kubernetes has the concept of namespaces which isolates workloads running in the same cluster, whereas ECS does not have such a concept in it.

3. Ease of Use

ECS is very straightforward and does not have a lot of components to learn whereas EKS is more complex as it uses Kubernetes which is altogether a vast technology to learn and requires expertise for deployments. ECS does not have any control plane, unlike EKS.

4. Pricing and Costs

The pricing of ECS and EKS also depends on the infrastructure (AWS Fargate or Amazon EC2) being used to host containerized applications. On top of this, one needs to pay $0.10 per hour for each Amazon EKS cluster for its control plane. This makes clear that the **AWS Elastic Kubernetes Service is a costly service. **

5. Portability and Compatibility

Both, EKS and ECS, are managed services of AWS. ECS is an AWS proprietary service whereas EKS is a Kubernetes-as-a-platform service by AWS.

6. Community support

For any software, platform, or framework, community support is essential. Since Kubernetes is an open-source technology.

https://aws.amazon.com/blogs/containers/amazon-ecs-vs-amazon-eks-making-sense-of-aws-container-services/

## Azure

### Azure VMs (Virtual Machines)

Deployed the microservices application on Azure VMs.
Analyze the cost associated with running the required number of VMs, including compute, storage, and network costs.

### Azure Container Service

Containerized the microservices and deploy them on Azure Container Service.
Analyze the cost of running ACS clusters, including the cost of VMs, load balancers, and other associated resources.

### Azure Kubernetes Service

Containerized the microservices and deploy them on Azure Kubernetes Service.
Analyze the cost of running AKS clusters, including the cost of VMs, load balancers, and other associated resources.

### Azure Container Instances (ACI) vs. Azure Kubernetes Service (AKS)

When considering Azure Container Instances (ACI) and Azure Kubernetes Service (AKS) as deployment options for containerized workloads, there are several factors to compare. The following analysis explores the differences between ACI and AKS based on various aspects:

#### Architecture and Management

1. Azure Container Instances (ACI)

   a. ACI is a serverless container platform that eliminates the need to manage virtual machines (VMs) or complex container orchestration services.
   b. It offers quick startup times, making it suitable for smaller-scale applications, build jobs, and task automation.
   c. ACI does not require the use of Kubernetes or other orchestrators, but it can be integrated with them if desired.

2. Azure Kubernetes Service (AKS)

   a. AKS simplifies the deployment of managed Kubernetes clusters in Azure.
   b. It handles complex operational tasks related to managing Kubernetes, such as health monitoring, upgrades, and networking.
   c. AKS manages the Kubernetes master nodes, while customers are responsible for maintaining and managing the agent nodes.
   d. AKS is a managed service, and customers only pay for the agent nodes used by their clusters.

#### Scalability and Orchestration

1. Azure Container Instances (ACI)

   a. ACI is suitable for smaller-scale applications and workloads that require quick deployment and elasticity.
   b. It provides automatic scaling, allowing containers to be started or stopped based on demand.
   c. ACI does not provide built-in container orchestration features, but it can be integrated with Kubernetes for enhanced orchestration capabilities.

2. Azure Kubernetes Service (AKS)

   a. AKS is designed for scalable and complex containerized workloads that require advanced orchestration features.
   b. It provides robust container orchestration with Kubernetes, allowing for deployment and management of containerized applications across multiple nodes.
   c. AKS supports horizontal pod autoscaling, allowing for automatic scaling of applications based on resource utilization.

#### Cost

1. Azure Container Instances (ACI)
   a. ACI pricing is based on the number of containers deployed, the duration of container instances running, and the resources consumed by each container.
   b. ACI is generally more cost-effective for short-lived workloads or smaller-scale applications.

2. Azure Kubernetes Service (AKS)
   a. AKS pricing is based on the number and size of the agent nodes used in the cluster.
   b. AKS provides cost advantages for long-running or larger-scale workloads, as it offers more efficient resource utilization and scaling capabilities.

#### Complexity and Management Overhead

1. Azure Container Instances (ACI)

   a. ACI is straightforward to set up and manage, requiring minimal configuration.
   b. It abstracts away the complexities of managing Kubernetes clusters, making it ideal for developers or teams with limited DevOps expertise.

2. Azure Kubernetes Service (AKS)

   a. AKS requires more initial setup and configuration, including managing the cluster infrastructure and ensuring high availability.
   b. It provides more control and flexibility for advanced container orchestration scenarios but may require additional DevOps knowledge.

#### Use Cases

1. Azure Container Instances (ACI)

   a. ACI is suitable for smaller-scale applications, task automation, or containerized workloads with varying demand.
   b. It is ideal for quick prototyping, development environments, or scenarios that do not require advanced container orchestration.

2. Azure Kubernetes Service (AKS)

   a. AKS is well-suited for complex containerized workloads, large-scale applications, or production environments.
   b. It is recommended for scenarios that require advanced container orchestration, scalability, and resilience.

#### Conclusion

In summary, the choice between ACI and AKS depends on the specific requirements and characteristics of the workload:

1. Choose **Azure Container Instances** (ACI) for simpler, **smaller-scale applications** with quick deployment needs or when managing Kubernetes clusters is not necessary.

2. Opt for **Azure Kubernetes Service (AKS)** for **complex, scalable workloads that require advanced container orchestration**, resource efficiency, and long-running deployments.

Consider factors such as scalability, cost, complexity, and management overhead to make an informed decision based on your specific use case.

## Predicting the Cheapest Solution

Based on the cost analysis, compared the overall costs for each deployment option and predicted the cheapest solution for deploying the microservices application. Considered the performance,scalability, and flexibility aspects of each option, along with the cost factor, to make an informed decision.

# License

This project is licensed under the MIT License. Please see the LICENSE.md file for more details.
