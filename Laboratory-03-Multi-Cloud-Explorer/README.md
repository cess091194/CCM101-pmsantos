### Server Specifications
- **Operating System:** Ubuntu 24.04.4 LTS (Noble Numbat)
- **CPU:** 1 vCPU — Intel Xeon E312xx (Sandy Bridge), 2.0GHz
- **Memory:** 1.9 GiB total RAM (1.5 GiB available), 1 GiB swap
- **Disk Space:** 19 GB root partition (13 GB available, 30% used)
---

### Migration Question
**If this Linux server were migrated to the cloud, which AWS, Azure, and GCP services could host it?**

Based on the specs gathered — 1 vCPU, about 2GB of RAM, and a ~19GB disk — this server fits comfortably into the entry-level/burstable-performance instance tiers offered by each provider, rather than needing a large compute-optimized instance.

**AWS:** This server could be hosted on **Amazon EC2** using a burstable instance type such as **t3.small** or **t3.micro** (1–2 vCPUs, 1–2GB RAM), since it's designed for workloads with low, intermittent CPU usage like this one. For the root volume, **Amazon EBS (Elastic Block Store)** with a 20GB General Purpose SSD (gp3) volume would match the current disk size.

**Azure:** On Azure, an **Azure Virtual Machine** using the **B-series** (burstable) size, such as **B1s** or **B1ms** (1 vCPU, 1–2GB RAM), would fit — Azure's cost-efficient tier for light, non-continuous workloads. For storage, an **Azure Managed Disk** (Standard SSD) sized around 20–30GB would work well.

**GCP:** On Google Cloud, a **Compute Engine** instance with the **e2-small** or **e2-micro** machine type (1–2 vCPUs, 1–2GB RAM) fits, as part of GCP's cost-optimized general-purpose family. For storage, **Persistent Disk (Standard or Balanced)** sized to match the ~20GB root volume would be appropriate.

**Summary:** Comparing all three providers, this server's low CPU and memory footprint means it belongs in each provider's cheapest general-purpose/burstable tier (AWS t3.micro/small, Azure B1s/B1ms, GCP e2-micro/small) rather than any compute- or memory-optimized instance family — keeping cloud hosting costs minimal for a workload this size.

**Operating System Info**

<img width="823" height="285" alt="killercoda-terminal" src="https://github.com/user-attachments/assets/58bd54f4-222f-4f2b-a4de-4f41ac43cde6" />

---

**CPU Information**

<img width="1043" height="762" alt="killercoda-terminal1" src="https://github.com/user-attachments/assets/f63cc338-43a6-47a3-8527-288d22079a01" />

---

**Memory & Disk Space**

<img width="615" height="187" alt="killercoda-terminal2" src="https://github.com/user-attachments/assets/3d7fa462-c29c-485f-9417-8baae29e205a" />

