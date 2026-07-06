# Docker Containers Flow

A Docker container is created in three main steps:

```
Dockerfile  ──►  Docker Image  ──►  Docker Container
                 (docker build)      (docker run)
```

## 1. Dockerfile

A **Dockerfile** is a text file that contains instructions for building a Docker image.

It defines:
- Base operating system/image
- Application dependencies
- Commands to install packages
- Files to copy
- Startup command

Example:

```dockerfile
FROM ubuntu
RUN apt-get update
CMD ["echo", "Hello"]
```

Think of a Dockerfile as a **recipe** for creating an image.

---

## 2. Docker Image

A **Docker image** is a read-only template created from a Dockerfile.

It contains everything required to run an application:

- Application code
- Libraries
- Dependencies
- Runtime
- Configuration

The image is built using:

```bash
docker build
```

An image is reusable—you can create multiple containers from the same image.

---

## 3. Docker Container

A **container** is a running instance of a Docker image.

It is created using:

```bash
docker run
```

Once started, the application runs inside the container in an isolated environment while sharing the host OS kernel.

---

## Complete Workflow

1. Write a **Dockerfile** describing your application.
2. Run **`docker build`** to create a Docker image.
3. Run **`docker run`** to start a container from that image.
4. The application now runs consistently on any machine with Docker installed.

## Summary

```
Dockerfile
      │
      ▼
docker build
      │
      ▼
Docker Image
      │
      ▼
docker run
      │
      ▼
Running Container
```

> **Simple analogy:** A **Dockerfile** is the recipe, a **Docker image** is the prepared meal, and a **Docker container** is someone actually eating the meal (the running instance).