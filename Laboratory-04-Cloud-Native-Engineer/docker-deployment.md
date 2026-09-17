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

*(<img width="337" height="30" alt="image" src="https://github.com/user-attachments/assets/195b494a-69bd-42f2-a17c-f125bb914acf" />
)*

## Checkpoint 4 — Deploy the Nginx Container

**1. Pull the official Nginx image:**
```bash
docker pull nginx
```
*(<img width="590" height="88" alt="image" src="https://github.com/user-attachments/assets/406e3e30-ebc3-496f-99c0-2e4e73bff38b" />
)*

**2. Run the container in detached mode, mapping host port 8080 to container port 80:**
```bash
docker run -d -p 8080:80 --name nginx-server nginx
```
*(<img width="545" height="197" alt="image" src="https://github.com/user-attachments/assets/96e94bb4-8516-44af-99d8-cf069368a172" />
)*

**3. Verify the web server is running:**
```bash
curl http://localhost:8080
```
*(<img width="542" height="422" alt="image" src="https://github.com/user-attachments/assets/1d18d449-7510-4006-958e-a3ce4ddeb717" />
)*
This returns the "Welcome to nginx!" HTML page, confirming the container is serving traffic.

*(<img width="546" height="373" alt="image" src="https://github.com/user-attachments/assets/6f58286b-5315-46a5-ac13-818d11705cd5" />
)*

## Checkpoint 5 — Container Lifecycle

| Command | What It Does |
|---|---|
| `docker ps` | Lists all currently running containers, showing their ID, image, status, and port mappings. |
| `docker stop nginx-server` | Gracefully stops the running Nginx container. |
| `docker ps -a` | Lists all containers, including stopped ones, to confirm `nginx-server` has an "Exited" status. |
| `docker rm nginx-server` | Permanently removes the stopped container and its writable layer from the host. |

<img width="658" height="210" alt="image" src="https://github.com/user-attachments/assets/c667bfe0-4dcc-4e3a-a5ee-96dce2a25b12" />

