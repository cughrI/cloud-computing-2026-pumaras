# Microsoft Azure Research

## Brief Overview

Microsoft Azure is Microsoft's cloud computing platform, launched in 2010. Azure is distinguished by its deep integration with Microsoft's existing enterprise software ecosystem — Windows Server, Active Directory, Office 365, and .NET — making it a natural fit for organizations already invested in Microsoft technologies.

## Global Infrastructure

Azure reports the largest number of regions among the three major providers — over 60 — though this partly reflects how Azure defines a "region" compared to AWS and GCP's region/zone structure. Azure regions are grouped into geographies to meet data residency and compliance requirements, with a particularly dense footprint across North America and Europe.

## Cloud Management Console

The **Azure Portal** is the web-based dashboard for managing Azure resources. Azure also provides Azure CLI, Azure PowerShell, and Azure Cloud Shell for command-line and scripted management, all tightly integrated with Microsoft's broader developer tooling (like Visual Studio).

## Four Core Services

1. **Azure Virtual Machines** — on-demand, scalable compute instances.
2. **Azure Blob Storage** — object storage for unstructured data such as documents, images, and backups.
3. **Azure Virtual Network (VNet)** — isolated networking for Azure resources.
4. **Microsoft Entra ID** (formerly Azure Active Directory) — identity and access management, natively linked to on-premises Active Directory.

## Three Advantages

1. **Best-in-class Microsoft integration** — seamless single sign-on and management across Office 365, Windows Server, and Active Directory for organizations already using Microsoft products.
2. **Strong hybrid cloud support** — tools like Azure Arc and Azure Stack let organizations manage on-premises and cloud resources under one control plane.
3. **Enterprise compliance and governance** — a wide range of compliance certifications and governance tooling geared toward large, regulated organizations.

## Typical Enterprise Use Cases

- Organizations migrating an existing Windows Server / Active Directory environment to the cloud
- Enterprises standardized on Microsoft 365 wanting unified identity and security management
- Hybrid cloud deployments that need to keep some infrastructure on-premises
- .NET application hosting and modernization
