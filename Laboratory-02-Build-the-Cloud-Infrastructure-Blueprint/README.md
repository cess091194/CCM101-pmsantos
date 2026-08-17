## Mission Overview
Congratulations, your onboarding has been successfully completed, and 
your Cloud Computing Portfolio has been approved by your supervisor.

CloudNova Technologies has now assigned you to your first official 
project. Before deploying cloud services, every cloud engineer must 
understand the infrastructure that powers modern cloud computing. This 
mission was to investigate the components of cloud infrastructure, 
identify how compute, storage, networking, and identity services work 
together, and document the findings as if preparing technical 
documentation for a client.

Using the KillerCoda Playground, Linux tools, official cloud 
documentation, and the GitHub Cloud Computing Portfolio, a series of 
engineering tasks were completed to simulate the planning phase of a 
cloud deployment.

*"Great cloud engineers build systems—but exceptional cloud engineers 
document and justify every design decision."*

## Objectives
At the end of this laboratory activity, the goal was to be able to:
- Explain the major components of cloud infrastructure.
- Investigate the hardware and software resources available in a Linux 
  environment.
- Differentiate compute, storage, networking, and identity resources.
- Interpret the relationship between cloud infrastructure components.
- Create professional technical documentation using Markdown.
- Continue building a structured GitHub Cloud Computing Portfolio.

## Cloud Infrastructure Components
Four main components were investigated on the KillerCoda Linux server:

| Component | What Was Found |
|---|---|
| **Operating System** | Ubuntu 24.04.4 LTS (Noble Numbat), kernel 6.8.0-136-generic |
| **Compute** | 1 CPU core, Intel Xeon E312xx (Sandy Bridge, IBRS update) — a virtualized CPU |
| **Storage** | 19G total disk (`/dev/vda1`), 5.4G used, 13G available |
| **Networking** | Hostname `ubuntu`, primary IP `172.30.1.2`, secondary IP `172.17.0.1` (Docker bridge) |

Full details and explanations of each component's purpose and importance 
are documented in [`cloud-components.md`](./cloud-components.md), and 
provider-level comparisons are documented in 
[`cloud-provider-comparison.md`](./cloud-provider-comparison.md).

## Tools Used
- **KillerCoda Playground** — provided the live Linux server environment
- **Linux terminal** — used to run investigation commands
- **Draw.io (diagrams.net)** — used to create the cloud architecture diagram
- **GitHub** — used to build and maintain the Cloud Computing Portfolio
- **Markdown** — used for all technical documentation

## Linux Commands Executed
| Purpose | Command |
|---|---|
| Operating System | `cat /etc/os-release` |
| Kernel Version | `uname -r` |
| CPU Model | `cat /proc/cpuinfo \| grep "model name"` |
| Number of CPU Cores | `nproc` |
| Total RAM | `free -h` |
| Disk Capacity | `df -h` |
| Mounted File Systems | `mount \| column -t` |
| Hostname | `hostname` |
| IP Address | `hostname -I` |

## Skills Learned
- How to inspect a Linux server's compute, storage, and networking 
  configuration directly from the terminal.
- How to identify when a CPU is virtualized versus physical based on the 
  reported model name.
- How to build comparison tables and structured documentation using 
  Markdown.
- How to design a basic cloud architecture diagram showing the 
  relationship between a user, the internet, a network, compute, and 
  storage.
- How to organize a multi-file technical report inside a GitHub 
  repository following a required folder structure.

## Challenges Encountered
- The `lscpu` command was not available in the minimal KillerCoda Ubuntu 
  container, which initially returned no output. This was resolved by 
  using `cat /proc/cpuinfo | grep "model name"` instead, which is the 
  equivalent way to retrieve the CPU model on a system without `lscpu` 
  installed.
- Formatting long terminal outputs (like `mount` and `df -h`) required 
  care to keep them inside Markdown code blocks so they would render 
  correctly on GitHub instead of appearing as unformatted text.
- Designing the cloud architecture diagram required deciding how to best 
  represent the relationship and data flow between the User, Internet, 
  Network, Compute, and Storage components in a clear and readable way.
