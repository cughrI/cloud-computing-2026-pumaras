Deployment Engineer

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
![Deployment](<img width="956" height="907" alt="image" src="https://github.com/user-attachments/assets/9b5e70be-cbf1-40ba-93f7-633a0cbaced0" />
)
![Nextcloud](<img width="1917" height="1020" alt="image" src="https://github.com/user-attachments/assets/3cbac8a1-5ab1-44f9-8477-6945703c9abe" />
)
![Teardown](<img width="952" height="906" alt="image" src="https://github.com/user-attachments/assets/d9beef51-e455-4525-a45b-54d409e24fac" />
)

## Skills Learned
- Writing YAML configuration with correct indentation
- Defining multiple services in a single Compose file
- Deploying and tearing down a stack with one command each
- Passing configuration through environment variables
- Exposing a container port and accessing it from a browser
- Documenting infrastructure in Markdown
