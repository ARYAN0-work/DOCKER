# Docker Architecture – Docker Containers

A **Docker Container** is an isolated environment where an application runs.

- A container is a **running instance of a Docker image**.
- It runs as an **isolated process** on the host.
- It packages the application along with its libraries and dependencies into a single executable unit.

> **In short:** A container is the runtime version of a Docker image.

# Docker Architecture – Docker Registry

A **Docker Registry** is a repository used to store and distribute Docker images.

## Docker Hub

- **Docker Hub** is the default public Docker registry.
- Anyone can pull public images from Docker Hub.

## Image Operations

- **Pull** – Download an image from a registry.

```bash
docker pull nginx
```

- **Push** – Upload a locally built image to a registry.

```bash
docker push username/my-image
```

> **In short:** A Docker Registry stores Docker images, allowing users to **pull** existing images or **push** their own images.