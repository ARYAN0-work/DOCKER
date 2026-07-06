# Docker Architecture – Docker Daemon (`dockerd`)

The **Docker Daemon (`dockerd`)** is the core service of Docker. It runs in the background on the host machine and is responsible for creating, managing, and monitoring Docker objects such as containers and images.

The Docker Client communicates with the Docker Daemon through the **Docker API**. Whenever you execute a Docker command, the client sends a request to the daemon, which performs the requested operation.

## Responsibilities

### 1. Listens to Docker API Requests

The daemon listens for requests sent by the **Docker Client** through the Docker API.

```
Docker Client
      │
      ▼
Docker API
      │
      ▼
Docker Daemon
```

---

### 2. Builds Docker Images

The daemon builds Docker images from a **Dockerfile** whenever the client runs:

```bash
docker build
```

---

### 3. Manages Docker Objects

The daemon creates and manages:

- Containers
- Images
- Networks
- Volumes

---

### 4. Interacts with Docker Registries

The daemon communicates with Docker registries (such as Docker Hub) to:

- Pull images

```bash
docker pull nginx
```

- Push images

```bash
docker push my-image
```

---

### 5. Manages the Container Lifecycle

The daemon is responsible for the complete lifecycle of containers.

It can:

- Start containers
- Stop containers
- Restart containers
- Remove containers

Example:

```bash
docker run nginx
docker stop <container-id>
docker rm <container-id>
```

## Workflow

```
User
   │
   ▼
Docker Client (CLI)
   │
   ▼
Docker API
   │
   ▼
Docker Daemon (dockerd)
   │
   ├── Builds Images
   ├── Creates Containers
   ├── Manages Networks
   ├── Manages Volumes
   └── Communicates with Docker Registries
```

## Summary

- Runs in the background on the host.
- Receives requests from the Docker Client.
- Builds Docker images.
- Creates and manages containers.
- Manages images, networks, and volumes.
- Pulls and pushes images to registries.
- Controls the entire container lifecycle.

> **In short:** The **Docker Daemon (`dockerd`)** is the heart of Docker. It performs all the actual work, while the Docker Client simply sends commands to it. 