# Laboratory 06 – The Cloud Deployment Engineer

## Mission Overview
Deployed a two-tier private cloud storage system (Nextcloud + MariaDB) at CloudNova
Technologies using Docker Compose, replacing manual container commands with
Infrastructure as Code.

## Objectives
- Explain multi-tier application architecture
- Understand the purpose and structure of a `docker-compose.yml` file
- Create configuration files with the nano text editor
- Deploy a multi-container application with Docker Compose
- Document the work in Markdown and add it to my GitHub portfolio

## Commands Executed
```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml
docker-compose up -d
docker-compose ps
docker-compose down
```

## Evidence
![Deployment](screenshots/compose-deployment.png)
![Nextcloud](screenshots/nextcloud-web.png)
![Teardown](screenshots/compose-teardown.png)

## Skills Learned
- Writing YAML configuration with correct indentation
- Defining multiple services in a single Compose file
- Deploying and tearing down a stack with one command each
- Passing configuration through environment variables
- Exposing a container port and accessing it from a browser
- Documenting infrastructure in Markdown
