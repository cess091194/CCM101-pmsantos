### Server Specifications

- **Operating System:** Ubuntu 24.04.4 LTS (Noble Numbat)
- **CPU:** 1 vCPU — Intel Xeon E312xx (Sandy Bridge), 2.0GHz
- **Memory:** 1.9 GiB total RAM (1.5 GiB available), 1 GiB swap
- **Disk Space:** 19 GB root partition (13 GB available, 30% used)

### Migration Question
**If this Linux server were migrated to the cloud, which AWS, Azure, and GCP services could host it?**

Given the server's small footprint — 1 vCPU, ~2GB RAM, and a ~19GB disk — this workload fits comfortably into the entry-level/burstable-performance instance tiers offered by each provider, rather than a large compute-optimized instance.

**AWS:** This server could be hosted on **Amazon EC2** using a burstable instance type such as **t3.small** or **t3.micro** (1–2 vCPUs, 1–2GB RAM), which is designed for workloads with low, intermittent CPU usage. Its root volume could be provisioned using **Amazon EBS (Elastic Block Store)** with a 20GB General Purpose SSD (gp3) volume to match the current disk size.

**Azure:** The equivalent host would be an **Azure Virtual Machine** using the **B-series** (burstable) size, such as **B1s** or **B1ms** (1 vCPU, 1–2GB RAM), which is Azure's cost-efficient tier for light, non-continuous workloads. Storage would map to an **Azure Managed Disk** (Standard SSD) sized around 20–30GB.

**GCP:** On Google Cloud, this maps to a **Compute Engine** instance using the **e2-small** or **e2-micro** machine type (1–2 vCPUs, 1–2GB RAM), part of GCP's cost-optimized general-purpose family. The disk would use **Persistent Disk (Standard or Balanced)** sized to match the ~20GB root volume.

**Summary:** Across all three providers, this server's low CPU and memory footprint means it belongs in each provider's cheapest general-purpose/burstable tier (AWS t3.micro/small, Azure B1s/B1ms, GCP e2-micro/small) rather than any compute- or memory-optimized instance family — keeping cloud hosting costs minimal for a workload this size.

**Operating System Info**

<img width="823" height="285" alt="killercoda-terminal" src="https://github.com/user-attachments/assets/58bd54f4-222f-4f2b-a4de-4f41ac43cde6" />

---

**CPU Information**

<img width="1043" height="762" alt="killercoda-terminal1" src="https://github.com/user-attachments/assets/f63cc338-43a6-47a3-8527-288d22079a01" />

---

**Memory & Disk Space**

<img width="615" height="187" alt="killercoda-terminal2" src="https://github.com/user-attachments/assets/3d7fa462-c29c-485f-9417-8baae29e205a" />

