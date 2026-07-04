# Server Components => actualyy your pc isnt powerful to serve 10,0000 users for you e-commerce website and buy stuff from you so hosting ecommerce website is not on scale and that's when this comes in picture.

A server is basically a powerful computing device with:

- A good amount of memory (RAM)
- One or more CPU(s)
- One or more disk drives to persistently store:
  - Operating System
  - Applications
  - Data
- One or more network interfaces
- One or more GPU(s)
- An Operating System:
  - Windows
  - Linux
  - macOS

We can install one or more applications on a server.

# Scaling Servers =>  i mean its made for 1 lakh not 10 lakh users: os can't handle this many request in per min and thats when this topic come then we made datacentres for taht i mean where we have servers a lot of .

As the number of users or requests increases:

- A single server may no longer be able to handle all incoming traffic.
- Server performance can degrade due to increased CPU, memory, disk, or network usage.
- To maintain performance and availability, we need to **scale** the infrastructure.
- Scaling typically involves adding one or more servers to distribute the workload.
- A load balancer is commonly used to route incoming requests across multiple servers.

> **Goal:** Handle more users while maintaining good performance and minimizing downtime.

# Server Resource Optimization & Multiple Applications on a Server

To optimize resource utilization, multiple applications can run on the same physical server instead of dedicating one server to each application.

## Benefits

- Better utilization of CPU, memory, storage, and network resources.
- Reduces hardware and infrastructure costs.
- Makes it easier to manage and maintain fewer physical servers.
- Allows multiple applications to share the same operating system and hardware resources.

> **Goal:** Maximize resource usage while minimizing hardware costs.