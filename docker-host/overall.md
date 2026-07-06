# Understanding How Docker Works

When you run a Docker command, multiple components work together to create and manage containers.

## Docker CLI

The **Docker CLI** is the command-line interface used by users.

- Sends commands to the **Docker Daemon (`dockerd`)**.
- Examples:

```bash
docker build
docker run
docker pull
```

---

## Docker Daemon (`dockerd`)

The Docker Daemon receives Docker API requests from the CLI and delegates container operations.

- Processes Docker API requests.
- Uses **containerd** to manage the container lifecycle.

---

## containerd

**containerd** is a high-level container runtime responsible for managing containers.

### Responsibilities

- Manages containers.
- Manages storage and networking.
- Pulls and pushes container images.
- Handles the container lifecycle.

---

## runC

**runC** is a low-level container runtime.

Its job is simple:

- Creates containers.
- Runs containers.

Each container is started by a separate **runC** process.

---

## Workflow

```text
Docker CLI
      │
      ▼
Docker Daemon (dockerd)
      │
      ▼
containerd
      │
      ▼
runC
      │
      ▼
Running Containers
```

## Summary

- **Docker CLI** → Accepts user commands.
- **Docker Daemon** → Processes Docker API requests.
- **containerd** → Manages containers, storage, networking, and images.
- **runC** → Creates and runs containers.