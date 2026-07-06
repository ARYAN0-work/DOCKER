# Containers Overview

A **container** is a **lightweight, isolated process** that runs on a shared operating system kernel. It packages everything an application needs to run, including:

- Application code
- Libraries & dependencies
- Runtime
- Environment variables
- Configuration files

This allows applications to run consistently across different environments.

## 📦 Shipping Container Analogy

Think of a Docker container like a **shipping container**.

A shipping container can carry different goods, but everything needed for transportation is packed inside one box. Whether it's moved by a ship, truck, or train, the contents remain the same.

Similarly, a Docker container packages an application along with all its dependencies into a single unit. It can run on any machine with Docker installed without worrying about missing libraries or configuration differences.

## 📦 What's Inside a Container?

A container typically includes:

- 📝 **Code** – The application itself.
- 📚 **Dependencies** – Required libraries and packages.
- ⚙️ **Runtime** – Software needed to execute the application (e.g., Node.js, Python).
- 🔧 **Configuration** – Environment variables and configuration files.

## Key Points

- Containers are **lightweight** and **isolated**.
- They **share the host OS kernel**, making them faster than virtual machines.
- Containers ensure applications behave the same in development, testing, and production.