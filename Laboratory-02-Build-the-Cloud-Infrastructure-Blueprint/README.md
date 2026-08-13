# Laboratory Activity 2: Build the Cloud Infrastructure Blueprint

## Mission Overview

As a newly onboarded cloud engineer at CloudNova Technologies, this lab simulates the planning phase of a cloud deployment. Using a Linux server provisioned through the KillerCoda Playground, I investigated the underlying infrastructure, identified its compute, storage, networking, and identity components, compared how the three major public cloud providers implement those same components, and produced technical documentation suitable for handing off to senior engineers before any real deployment.

## Objectives

- Explain the major components of cloud infrastructure.
- Investigate the hardware and software resources available in a Linux environment.
- Differentiate compute, storage, networking, and identity resources.
- Interpret the relationship between cloud infrastructure components.
- Create professional technical documentation using Markdown.
- Continue building a structured GitHub Cloud Computing Portfolio.

## Cloud Infrastructure Components

| Component | Role Observed in This Lab |
|---|---|
| Compute | CPU cores and RAM allocated to the KillerCoda container, investigated with `lscpu`, `nproc`, `free -h` |
| Storage | Root filesystem and mounted volumes, investigated with `df -h`, `mount` |
| Networking | Hostname and IP addressing, investigated with `hostname`, `ip addr` |
| Operating System | Linux distribution and kernel managing the above resources, investigated with `cat /etc/os-release`, `uname -r` |

Full details are documented in `infrastructure-report.md` and `cloud-components.md`.

## Tools Used

- KillerCoda Playground (Linux terminal environment)
- Git and GitHub (portfolio version control)
- Markdown (documentation)
- Draw.io *(or your chosen diagramming tool)* for the architecture diagram

## Linux Commands Executed

| Command | Purpose |
|---|---|
| `cat /etc/os-release` | Identify the operating system and version |
| `uname -r` | Identify the kernel version |
| `lscpu` | Identify CPU model and core count |
| `nproc` | Count available CPU cores |
| `free -h` | Check total and available RAM |
| `df -h` | Check disk capacity and usage |
| `mount` / `df -hT` | List mounted file systems |
| `hostname` | Identify the server hostname |
| `ip addr show` | Identify the assigned IP address |

## Skills Learned

- Reading system information from a Linux command line to build an infrastructure inventory.
- Mapping raw Linux resource data (CPU, RAM, disk, network) to cloud infrastructure concepts (compute, storage, networking).
- Comparing equivalent services across AWS, Azure, and GCP.
- Producing structured technical documentation in Markdown, including tables and diagrams.
- Maintaining a version-controlled GitHub portfolio.

## Challenges Encountered

<!-- Personalize this section: e.g., interpreting `df -h` output for containerized filesystems, choosing a diagramming tool, understanding IAM differences across providers, etc. -->
