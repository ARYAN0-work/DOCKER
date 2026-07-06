 # Virtual Machines (VMs) vs. Containers (cont.)

| **Virtual Machines (VMs)** | **Containers** |
|----------------------------|----------------|
| Heavyweight (slow to start) | Lightweight (start in milliseconds) |
| Limited scalability | Faster scaling |
| Low portability | Excellent portability |
| Redundant OS overhead | Containers share the host OS kernel |
| Inefficient image management | Efficient image management |
| Poor Dev/Test/Prod parity | Containers are excellent for CI/CD |

# Popular Container Engines & Runtimes

- **Docker**
  - The most popular container engine used to build, ship, and run containers.

- **LXC (Linux Containers)**
  - A **system-level containerization framework** that provides lightweight Linux containers.

- **containerd**
  - A container runtime geared towards **Kubernetes** deployments.
  - Responsible for managing the complete container lifecycle.

- **CRI-O**
  - A lightweight container runtime specifically designed for **Kubernetes**.
  - Implements the Kubernetes **Container Runtime Interface (CRI)**.