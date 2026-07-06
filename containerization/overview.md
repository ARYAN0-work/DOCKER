# Containerization Overview

**Containerization** is the process of packaging an application along with everything it needs to run (code, dependencies, runtime, libraries, and configuration) into a **container**. To build, ship, and run these containers, we need a **container runtime/engine**, such as **Docker**.

## How Containerization Works

Before containers can run, a **container engine** must be installed on the host operating system.

The container engine:

- Creates and manages containers.
- Shares the **host operating system's kernel** among all containers.
- Provides isolation so that each container runs independently.
- Starts, stops, and removes containers when required.

Unlike virtual machines, containers **do not include a full operating system**. Instead, they share the host OS kernel, making them lightweight and fast.

## Container Architecture

```
+--------------------------------+
|      Application 1             |
|      Binaries / Libraries      |
+--------------------------------+
|      Application 2             |
|      Binaries / Libraries      |
+--------------------------------+
|       Docker Engine            |
+--------------------------------+
|      Host Operating System     |
+--------------------------------+
|          Hardware              |
+--------------------------------+
```

### Layers Explained

### 1. Hardware
The physical machine that provides resources like CPU, RAM, storage, and networking.

### 2. Host Operating System
The operating system installed directly on the hardware (Linux, Windows, etc.). Containers share this OS kernel.

### 3. Docker Engine
The software responsible for creating, running, and managing containers. It acts as the bridge between the operating system and the containers.

### 4. Containers
Each container contains:
- The application
- Required binaries and libraries
- Runtime
- Configuration

Containers are isolated from one another but share the same Docker Engine and OS kernel.

## Docker

Docker is the **most popular container engine** used for containerization.

Docker is available in:

- **Community Edition (CE)** – Free and open-source.
- **Enterprise Edition (EE)** – Paid version with enterprise features and support.

> **In short:** Containerization packages an application with all its dependencies into an isolated container, while the Docker Engine manages these containers on top of a shared host operating system.