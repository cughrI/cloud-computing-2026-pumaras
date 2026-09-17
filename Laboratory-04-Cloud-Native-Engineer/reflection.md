# Mission 4 Reflection

The difference between deploying a Docker container and setting up a full Virtual Machine is night and day. Installing an operating system on a VM involves downloading an ISO, allocating virtual hardware, running through an OS installer, and then configuring the environment before an application can even be installed — a process that easily takes fifteen minutes or more. Deploying Nginx in a container, by contrast, took a single `docker run` command and was serving traffic within seconds, because the container skips the OS boot entirely and reuses the host's kernel.

Port mapping (`-p 8080:80`) is necessary because a container's internal network is isolated from the host by default. Nginx inside the container listens on port 80, but that port is not automatically reachable from outside the container. Mapping host port 8080 to container port 80 creates a bridge so that a request to `localhost:8080` on the host machine is forwarded into the container, letting the web server actually be reached.

When `docker rm` is used, the container's writable layer — and any data that was created or changed inside it — is permanently deleted, since that layer only exists as long as the container does. Any data that wasn't stored in a persistent volume is lost for good, which is why production workloads typically pair containers with volumes for anything that needs to survive removal.

Containerization changes DevOps by giving developers and operations teams a shared, portable unit of deployment. A developer can build and test an image locally with confidence that it will behave identically in staging and production, removing a huge source of "it works on my machine" friction and letting operations focus on orchestration and scaling rather than environment configuration.

*(Personalize the closing section on how your GitHub portfolio is evolving based on your own repository and experience.)*
