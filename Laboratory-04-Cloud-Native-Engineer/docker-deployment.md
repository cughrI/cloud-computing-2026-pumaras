# Docker Deployment Log

## Checkpoint 3 — Verify Docker Installation

```bash
docker --version
```
Confirms Docker is installed and shows the installed version.

```bash
docker info
```
Shows the current status and configuration of the Docker environment (containers running, images stored, storage driver, etc.).

*(Screenshot saved as `screenshots/docker-version.png`)*

## Checkpoint 4 — Deploy the Nginx Container

**1. Pull the official Nginx image:**
```bash
docker pull nginx
```

**2. Run the container in detached mode, mapping host port 8080 to container port 80:**
```bash
docker run -d -p 8080:80 --name nginx-server nginx
```

**3. Verify the web server is running:**
```bash
curl http://localhost:8080
```
This returns the "Welcome to nginx!" HTML page, confirming the container is serving traffic.

*(Screenshot saved as `screenshots/nginx-running.png`)*

## Checkpoint 5 — Container Lifecycle

| Command | What It Does |
|---|---|
| `docker ps` | Lists all currently running containers, showing their ID, image, status, and port mappings. |
| `docker stop nginx-server` | Gracefully stops the running Nginx container. |
| `docker ps -a` | Lists all containers, including stopped ones, to confirm `nginx-server` has an "Exited" status. |
| `docker rm nginx-server` | Permanently removes the stopped container and its writable layer from the host. |

*(Screenshot saved as `screenshots/container-lifecycle.png`)*
