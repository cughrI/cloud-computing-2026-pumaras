# Client Recommendations

## Checkpoint 4 — Cloud Platform Recommendation Challenge

### Client A — Startup Company (limited budget, expects rapid growth)

**Recommended Platform: AWS**

AWS is the strongest fit for a budget-conscious startup expecting rapid growth because of its pay-as-you-go pricing, free tier, and the ability to scale from a handful of users to millions without re-architecting. Its huge ecosystem also means the startup can find pre-built solutions and tutorials for nearly any feature they want to build, reducing engineering time and cost early on. As the company grows, AWS's breadth of services means they won't need to migrate to a different provider to access more advanced capabilities later.

**Services the client could use:**
- **Amazon EC2** — flexible, low-cost compute that scales with demand
- **Amazon S3** — cheap, durable storage for user uploads and app assets
- **AWS Lambda** — serverless functions to avoid paying for idle infrastructure while the app is small

### Client B — University (Windows Server, Microsoft 365, Active Directory)

**Recommended Platform: Microsoft Azure**

Azure is the clear recommendation since the university is already standardized on Microsoft technologies. Migrating to Azure lets them extend their existing Active Directory into the cloud via Microsoft Entra ID rather than replacing their identity system, and Microsoft 365 integration means faculty and students keep a familiar experience. This significantly lowers both the technical risk and the retraining cost of the migration compared to switching to a non-Microsoft provider.

**Services the client could use:**
- **Azure Virtual Machines** — to lift-and-shift existing Windows Server workloads
- **Microsoft Entra ID** — to extend on-premises Active Directory into the cloud
- **Azure Virtual Desktop** — to give students/staff cloud-hosted desktops accessible from anywhere

### Client C — AI Research Company (high-performance computing for AI/ML)

**Recommended Platform: Google Cloud Platform**

GCP is the best fit for an AI research company because of its purpose-built machine learning infrastructure — including Tensor Processing Units (TPUs), which are custom hardware accelerators designed specifically for training large ML models faster and often more cost-effectively than general-purpose GPUs. GCP's tooling (Vertex AI, BigQuery ML) is also built around the exact workflow an ML research team needs, from data preparation to model deployment.

**Services the client could use:**
- **Compute Engine with TPUs/GPUs** — high-performance compute for model training
- **Vertex AI** — managed platform for building, training, and deploying ML models
- **BigQuery** — serverless data warehouse for analyzing large training datasets

### Client D — Global E-Commerce Company (worldwide customers, high availability, auto-scaling)

**Recommended Platform: AWS**

AWS is recommended for a global e-commerce company because of its extensive worldwide region and Availability Zone coverage, which lets the client place infrastructure close to customers on every continent for low latency. AWS's auto-scaling and load-balancing services are mature and battle-tested at massive scale (Amazon's own retail platform runs on this same infrastructure), which directly matches the client's need for automatic scaling during traffic spikes like sales events.

**Services the client could use:**
- **Amazon EC2 Auto Scaling** — automatically adjusts compute capacity to match traffic
- **Amazon CloudFront** — global content delivery network for fast page loads worldwide
- **Amazon RDS (Multi-AZ)** — highly available managed database with automatic failover

---

## Checkpoint 6 — Multi-Cloud Decision Matrix

| Business Requirement | Recommended Platform | Justification |
|---|---|---|
| Startup Company | AWS | Pay-as-you-go pricing, free tier, and the widest range of services to grow into without switching providers |
| Enterprise Organization | AWS or Azure | AWS for breadth of services; Azure if already invested in Microsoft enterprise tools |
| Microsoft Environment | Azure | Native integration with Active Directory, Microsoft 365, and Windows Server |
| AI / Machine Learning | GCP | Purpose-built ML infrastructure (TPUs, Vertex AI) and strong data analytics tooling |
| Kubernetes Deployment | GCP | Created Kubernetes; GKE is the most mature managed Kubernetes offering |
| Global Web Application | AWS | Largest global region/AZ footprint and mature auto-scaling/CDN services for low-latency worldwide delivery |
