# Docker Architecture – Docker Client

The **Docker Client** is the interface that allows users and developers to interact with Docker.

When you execute Docker commands, the Docker Client sends those commands to the **Docker Daemon (`dockerd`)**, which performs the requested operations.

## Responsibilities

- Accepts Docker commands from the user.
- Sends commands to the Docker Daemon.
- Receives and displays the results.

## Common Docker Client Commands

```bash
docker pull
docker run
docker build
```

## Workflow

```text
User
  │
  ▼
Docker Client (CLI)
  │
  ▼
Docker Daemon (dockerd)
```

> **In short:** The Docker Client acts as the communication layer between the user and the Docker Daemon.