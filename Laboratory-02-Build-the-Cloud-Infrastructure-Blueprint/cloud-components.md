# Cloud Infrastructure Components

This document identifies the core infrastructure components observed in the KillerCoda Linux environment and relates each to its role in cloud computing generally.

## 1. Compute Resources

**Purpose:** Compute is the processing power that runs applications, executes code, and handles workloads — the CPU cores and memory allocated to a virtual machine or container.

**Why it matters in cloud computing:** Compute is the resource customers pay for most directly. Cloud providers let you scale compute up or down (vertically) or add more instances (horizontally) on demand, instead of buying and maintaining physical servers.

**Relation to the KillerCoda environment:** The KillerCoda Playground itself is a compute resource — a container/VM with an allocated number of CPU cores (found via `lscpu`/`nproc`) and RAM (`free -h`). This mirrors how a real cloud compute instance (an AWS EC2 instance, Azure VM, or GCP Compute Engine instance) is just a slice of a provider's underlying physical hardware, sized to a chosen CPU/RAM tier.

## 2. Storage Resources

**Purpose:** Storage holds data persistently — the operating system, application files, logs, and any data written to disk.

**Why it matters in cloud computing:** Cloud storage is designed to be durable, scalable, and often decoupled from compute, so data can persist independently of any single server and can be resized without downtime.

**Relation to the KillerCoda environment:** The root filesystem and any mounted volumes shown by `df -h` / `mount` represent the storage attached to the playground's container. This is analogous to a block storage volume (like an AWS EBS volume or Azure Managed Disk) attached to a cloud VM.

## 3. Networking Resources

**Purpose:** Networking connects compute instances to each other and to the outside world — it includes IP addressing, routing, and firewall/security rules that control traffic.

**Why it matters in cloud computing:** Cloud networking (VPCs/VNets, subnets, security groups) determines what can reach a server and what a server can reach, which is central to both functionality and security of any cloud deployment.

**Relation to the KillerCoda environment:** The hostname and IP address (from `hostname` and `ip addr`) show how the playground container is addressed on its network. In a production cloud environment, that same instance would sit inside a Virtual Private Cloud (VPC) or Virtual Network (VNet), with its IP and open ports controlled by security groups/firewall rules.

## 4. Operating System

**Purpose:** The operating system (found via `cat /etc/os-release` and `uname -r`) manages hardware resources and provides the runtime environment for applications — process scheduling, file systems, and user permissions.

**Why it matters in cloud computing:** The OS and kernel version affect compatibility, security patching, and available tooling. Cloud providers offer many pre-built OS images (AMIs on AWS, VM images on Azure/GCP) so engineers can choose an OS suited to their workload.

**Relation to the KillerCoda environment:** The Linux distribution and kernel running the playground is the same kind of base image a cloud provider would offer when provisioning a new VM — the starting point on which compute, storage, and networking are configured.
