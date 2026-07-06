# Docker Roadmap

- Physical Servers vs Virtual Machines vs Containers
- Create a free AWS account and a Virtual Machine (VM) to practice
- What Docker is and Docker Architecture
- Docker commands and how to use them
- Docker Images and how they are used to create containers
- Dockerfile and creating your own Docker Images
- Docker Registry – Build and Publish your Images
- Docker Networking
- Docker Compose
- Persisting Container Data using Volumes and Bind Mounts
- Capstone Project//

## Why Docker?

- **Environment Reproducibility**
  - Everyone gets the exact same development environment.
  - Eliminates the "works on my machine" problem.

- **Dependency Management**
  - Packages and dependencies are isolated inside containers.
  - Avoids conflicts between different projects and operating systems.

- **Portability**
  - Run the same container on any machine:
    - Development laptop
    - Testing server
    - Cloud instance
    - Production server

- **Version Control for Environments**
  - Dockerfiles are plain text.
  - They can be stored and version-controlled using Git.
  - Easily recreate the same environment at any time.