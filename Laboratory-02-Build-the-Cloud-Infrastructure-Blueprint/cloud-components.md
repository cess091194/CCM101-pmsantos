## Compute Resources
**Purpose:** Compute resources run the processes and application logic 
of a system — the "brain" that performs actual processing using the 
CPU and RAM.

**Why it's important in cloud computing:** In the cloud, compute 
capacity determines how much workload a system can handle at once. It 
is highly scalable — cores and RAM can be increased or decreased on 
demand without needing to purchase new physical hardware.

**Relationship to the Linux environment provided by KillerCoda:** This 
server has only **1 CPU core** (from `nproc`) and a CPU model of 
**Intel Xeon E312xx (Sandy Bridge, IBRS update)** (from `/proc/cpuinfo`). 
This model name itself reveals that the CPU is **virtualized/emulated** 
— meaning it is not a physical processor but rather a "slice" of 
compute power provided by a hypervisor, similar to how real cloud 
providers like AWS or Azure allocate compute to their VM instances.

## Storage Resources
**Purpose:** Storage resources persist data — files, logs, and 
databases — beyond a single session or even after the machine restarts.

**Why it's important in cloud computing:** Cloud storage must be 
durable, scalable, and sometimes distributed across locations to 
prevent data loss and to keep up with growing amounts of data.

**Relationship to the Linux environment provided by KillerCoda:** Based 
on `df -h`, the server's main disk (`/dev/vda1`) has a total capacity 
of **19G**, with **5.4G** used and **13G** still available, mounted at 
the root (`/`). Additional partitions such as `/boot` (881M) and 
`/boot/efi` (105M) also exist to support boot-related files.

## Networking Resources
**Purpose:** Networking resources connect compute and storage to each 
other and to external users or clients.

**Why it's important in cloud computing:** Networking enables 
communication between resources, load balancing, and security 
boundaries (firewalls, VPCs) that protect cloud environments.

**Relationship to the Linux environment provided by KillerCoda:** This 
server has the hostname **`ubuntu`** and IP address **172.30.1.2** as 
its primary address (from `hostname -I`). A second IP, 172.17.0.1, also 
appears, which looks like it comes from a Docker bridge interface — 
indicating the server has an internal network layer in addition to its 
external-facing connection.

## Operating System
**Purpose:** The operating system manages hardware resources and 
provides the platform on which applications run.

**Why it's important in cloud computing:** Cloud images/instances are 
built on top of an OS — choosing the right one affects compatibility, 
licensing, and security across the deployment.

**Relationship to the Linux environment provided by KillerCoda:** This 
server runs **Ubuntu 24.04.4 LTS (Noble Numbat)**, using kernel version 
**6.8.0-136-generic** (from `cat /etc/os-release` and `uname -r`). 
Ubuntu LTS is one of the most commonly used operating systems in cloud 
environments because of its long-term support and broad compatibility.
