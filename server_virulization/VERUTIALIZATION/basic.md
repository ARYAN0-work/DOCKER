# Introduction to Virtualization => split the hardware components intovirtual mean and it will give you the isolation you needed

Virtualization was introduced to solve the limitations of running multiple applications directly on a physical server.

It provides:

- **Isolation** – Each application runs in its own Virtual Machine (VM).
- **Flexibility** – Different operating systems and software stacks can run on the same physical server.
- **Portability** – Virtual Machines can be moved between physical machines.
- **Scalability** – New Virtual Machines can be created whenever more resources are needed.

---

## Traditional Physical Server

```text
App 1   App 2   App 3
----------------------
Operating System
----------------------
Physical Hardware
```

Problems:

- Applications share the same Operating System.
- Dependency conflicts.
- Weak isolation.
- Difficult deployment and scaling.

---

# Virtualization Architecture

A virtualization layer called the **Hypervisor** is introduced between the Operating System and the Virtual Machines.

```text
VM 1     VM 2     VM 3
------------------------
Hypervisor// new layer was introdced above which we started calling virtual machines
------------------------
Host Operating System
------------------------
Physical Hardware
```

The Hypervisor manages multiple Virtual Machines and allocates hardware resources to each VM. make each vm's

---

# Benefits of Virtualization [ it have the whole os provide everything]

Virtualization allows us to:

- Run multiple Virtual Machines on a single physical server.
- Run multiple Operating Systems simultaneously.
- Isolate applications from one another.
- Allocate CPU, RAM, Disk, and Network resources independently.
- Improve hardware utilization.

---

# Features of Virtual Machines

Each Virtual Machine has:

- Its own Operating System.
- Its own applications.
- Its own runtime and dependencies.
- Its own allocated CPU, RAM, Disk, and Network resources.

Since every VM is isolated, problems inside one VM do not directly affect another.

---

# Snapshot Support

Virtual Machines support **Snapshots**.

A snapshot is a backup of the VM's current state.

It can be used to:

- Restore a VM after a failure.
- Test software safely.
- Roll back to a previous working state.

---

> **Key Idea:** Virtualization solves many of the problems of traditional servers by introducing a **Hypervisor**, allowing multiple isolated Virtual Machines to run on a single physical server.

# Virtual Machine (VM) Resources

The **Hypervisor** is responsible for sharing the physical server's hardware resources among multiple Virtual Machines (VMs).

Each VM receives its own virtual hardware, making it behave like an independent computer.

Each Virtual Machine gets:

- **Virtual CPU (vCPU)** – Processing power allocated from the host CPU.
- **Virtual RAM (vRAM)** – Memory allocated from the host RAM.
- **Virtual Disk (vDisk)** – Virtual storage created from the host's physical disk.
- **Virtual Network Interface Card (vNIC)** – Virtual network adapter used for communication.

> **Key Idea:** Although all VMs share the same physical hardware, each VM sees its own dedicated virtual hardware.

---

> These Hypervisors allow multiple Virtual Machines to run on a single physical server.

---

# Limitations of Virtual Machines (VMs)

Although Virtual Machines solve many problems of traditional servers, they also introduce new challenges.

## Drawbacks

- **Heavyweight**
  - Every VM includes a complete Guest Operating System, making it large in size and slow to boot.

- **Limited Scalability**
  - Creating and starting new VMs takes more time compared to lightweight alternatives.

- **Poor Dev/Test/Production Parity**
  - Development, testing, and production environments may differ, leading to "it works on my machine" problems.

- **Redundant Operating System Overhead**
  - Every VM runs its own operating system, consuming additional CPU, RAM, and storage resources.

- **Inefficient Image Management**
  - VM images are large, difficult to store, transfer, and maintain.

> **Key Idea:** Virtual Machines provide excellent isolation but are resource-intensive because each VM contains a complete operating system. These limitations eventually led to the development of **Containers (Docker)**.