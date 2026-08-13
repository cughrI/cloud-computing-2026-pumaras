# Cloud Provider Comparison

A comparison of core infrastructure services offered by the three leading public cloud providers.

| Infrastructure Component | AWS | Microsoft Azure | Google Cloud Platform |
|---|---|---|---|
| Compute | EC2 (Elastic Compute Cloud) | Virtual Machines | Compute Engine |
| Storage | S3 (Simple Storage Service) | Blob Storage | Cloud Storage |
| Networking | VPC (Virtual Private Cloud) | Virtual Network (VNet) | VPC (Virtual Private Cloud, global-scoped) |
| Identity and Access Management (IAM) | AWS IAM | Microsoft Entra ID (formerly Azure AD) | Cloud IAM |

## Guide Questions

**1. Which cloud provider offers the broadest range of services? Explain your answer.**

AWS offers the broadest range of services, with 200+ managed offerings spanning compute, storage, databases, networking, and AI/ML. As the first major public cloud provider, it has had the longest time to build out niche and specialized services, so almost any cloud pattern already has a mature, well-documented AWS implementation.

**2. Which cloud platform would you recommend for an organization that primarily uses Microsoft products? Why?**

Microsoft Azure is the natural fit for an organization built around Microsoft products. It integrates tightly with Active Directory/Entra ID, Office 365, and .NET workloads, giving a single sign-on and management experience across on-premises and cloud resources that AWS or GCP can't match as directly.

**3. Which platform is widely recognized for Artificial Intelligence (AI), Machine Learning (ML), and Kubernetes services?**

Google Cloud Platform is widely recognized for AI/ML and Kubernetes — it created and still leads development of Kubernetes (via GKE, its managed offering), and its TPUs and BigQuery ML are strong differentiators for machine learning workloads. (Azure is also strong here through its OpenAI integration, and AWS through SageMaker, so all three are competitive, but GCP's roots in Kubernetes give it a distinct edge on orchestration.)

**4. What similarities did you observe among the three cloud providers?**

All three providers offer functionally equivalent building blocks — virtual machine compute, object storage, virtual networking, and identity/access management — following a pay-as-you-go pricing model. The core concepts transfer between providers even though the service names, consoles, and pricing details differ, which is why cloud skills are largely portable across AWS, Azure, and GCP.
