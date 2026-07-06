# Docker Architecture – Connecting the Dots

The diagram below shows how all Docker components work together.

## Workflow

1. The **Docker Client** sends commands such as:

```bash
docker build
docker run
docker pull
```

2. The **Docker Daemon (`dockerd`)** receives these commands through the Docker API.

3. Depending on the command, the daemon:
   - Builds Docker images.
   - Creates and runs containers.
   - Manages networks and volumes.

4. If an image is not available locally, the daemon **pulls** it from a **Docker Registry** (e.g., Docker Hub).

5. If you build your own image, you can **push** it to the registry for storage and sharing.

## Overall Architecture

```text
           Docker Client
                 │
                 ▼
        Docker Daemon (dockerd)
          ├──────────────┐
          │              │
          ▼              ▼
     Containers       Images
          │              │
          └──────┬───────┘
                 ▼
          Docker Registry
            (Docker Hub)
```

## Summary

- **Docker Client** → Sends commands.
- **Docker Daemon** → Executes the commands.
- **Images** → Templates used to create containers.
- **Containers** → Running applications.
- **Docker Registry** → Stores Docker images for pulling and pushing.

> **In short:** The Docker Client communicates with the Docker Daemon, which manages images and containers and interacts with Docker Registry whenever images need to be pulled or pushed.