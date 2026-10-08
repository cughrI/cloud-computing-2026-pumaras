# Docker Compose Guide

## The Compose File
```yaml
version: '3'

services:
  database:
    image: mariadb:10.6
    environment:
      - MYSQL_ROOT_PASSWORD=cloudnova_root
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user

  app:
    image: nextcloud
    ports:
      - 8080:80
    environment:
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user
      - MYSQL_HOST=database
```

## What does the `services:` block do?
It lists every container that makes up the application. Each entry under it
(`database` and `app`) becomes one container, with its own image, ports, and
environment variables. Compose creates and starts all of them together.

## How did the Nextcloud app container find the database?
Through the `MYSQL_HOST=database` environment variable. `database` is the name of
the service in the Compose file. Compose puts all services on a shared network
where each service name works as a hostname, so Nextcloud reaches MariaDB at
`database` without needing an IP address.

## `docker run` vs `docker-compose up -d`
| | `docker run` | `docker-compose up -d` |
|---|---|---|
| Scope | One container per command | The whole multi-container stack |
| Configuration | Long flags typed manually | Defined in a YAML file (Infrastructure as Code) |
| Networking | Must be linked manually | Services share a network automatically |
| Repeatability | Easy to make typos or forget flags | Same file gives the same result every time |
| Version control | Commands live in shell history | The file can be committed to Git |

The `-d` flag runs the containers in detached mode, in the background.
