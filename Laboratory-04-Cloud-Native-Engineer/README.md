# Laboratory Activity 4: The Cloud-Native Engineer

## Mission Overview
This lab covers the transition from traditional Virtual Machines to containerized applications. Using the KillerCoda Playground, I explored the architectural differences between VMs and containers, executed core Docker CLI commands, and deployed a live Nginx web server in a container.

## Objectives
- Differentiate between traditional Virtual Machines (VMs) and Containers.
- Access a Docker-enabled cloud environment using KillerCoda.
- Execute fundamental Docker CLI commands.
- Pull, run, manage, and terminate a containerized application (Nginx).
- Create professional technical documentation of container operations using Markdown.
- Continue developing a well-organized GitHub Cloud Computing Portfolio.

## Docker Commands Executed
```bash
docker --version
docker info
docker pull nginx
docker run -d -p 8080:80 --name nginx-server nginx
curl http://localhost:8080
docker ps
docker stop nginx-server
docker ps -a
docker rm nginx-server
```

## Skills Learned
- How to verify and inspect a Docker environment from the CLI.
- How to pull an image from Docker Hub and run it as a detached container.
- How port mapping (`-p host:container`) exposes a containerized service to the host machine.
- How to manage the full lifecycle of a container: list, stop, verify, and remove.
- How containerization compares to traditional VM-based deployment in speed and resource use.

## Challenges Encountered
- No major issues came up during this activity. Docker was already installed and running in the KillerCoda Playground, so verification, pulling the Nginx image, running the container, and testing it with curl all worked on the first try. The container lifecycle commands (docker ps, docker stop, docker ps -a, docker rm) behaved exactly as expected, with each command's output confirming the state change before moving to the next step.
