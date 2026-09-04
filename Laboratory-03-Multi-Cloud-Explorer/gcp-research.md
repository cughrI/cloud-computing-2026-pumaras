# Google Cloud Platform (GCP) Research

## Brief Overview

Google Cloud Platform (GCP) is Google's public cloud offering, built on the same infrastructure that powers Google Search, YouTube, and Gmail. GCP is the youngest of the three major providers but is widely recognized as the leader in data analytics, machine learning, and container orchestration — GCP created and still leads development of Kubernetes.

## Global Infrastructure

As of 2026, GCP operates roughly 40+ regions and 130+ zones worldwide, with coverage across every continent except Antarctica, plus 200+ network edge locations for content delivery. While GCP has fewer regions than AWS or Azure, Google's private global fiber network is often cited as a performance advantage for cross-region traffic.

## Cloud Management Console

The **Google Cloud Console** is the web-based interface for managing GCP resources, alongside the `gcloud` CLI and Cloud Shell, a free browser-based terminal with pre-installed tools for managing GCP resources directly.

## Four Core Services

1. **Compute Engine** — customizable virtual machine instances.
2. **Cloud Storage** — object storage for unstructured data at any scale.
3. **Virtual Private Cloud (VPC)** — global-scoped virtual networking (a VPC in GCP can span multiple regions, unlike AWS/Azure).
4. **Cloud IAM** — identity and access management for controlling resource permissions.

## Three Advantages

1. **AI/ML leadership** — GCP offers TPUs (Tensor Processing Units), Vertex AI, and BigQuery ML, making it a top choice for machine learning-heavy workloads.
2. **Kubernetes and container expertise** — Google created Kubernetes, and GKE (Google Kubernetes Engine) is widely regarded as the most mature managed Kubernetes offering.
3. **Data analytics strength** — BigQuery is a leading serverless data warehouse for large-scale analytics.

## Typical Enterprise Use Cases

- AI and machine learning research and production workloads
- Big data analytics using BigQuery
- Container-native applications built on Kubernetes/GKE
- Organizations wanting a global-scoped network without managing per-region VPC peering
