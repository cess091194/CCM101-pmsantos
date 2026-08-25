# Cloud Platform Recommendations

### Client A – Startup Company
**Scenario:** A startup wants to launch a new mobile application with a limited budget but expects rapid growth over the next few years.

**Recommended Platform:** Google Cloud Platform (GCP)

GCP is well suited to startups because of its competitive pricing model, generous free-tier credits, and per-second billing, which keeps early costs low. Its serverless and auto-scaling services (like Cloud Run and GKE Autopilot) let the app scale automatically as user growth accelerates, without the team needing to manage infrastructure manually. GCP's Firebase platform also integrates directly with GCP services, making it a natural fit for building and scaling a mobile app backend.

**Services to use:** Firebase (mobile backend), Cloud Run (serverless scaling), Cloud Firestore (database), Cloud Storage.

---

### Client B – University
**Scenario:** A university already uses:
- Windows Server
- Microsoft 365
- Active Directory

The university wants to migrate some services to the cloud.

**Recommended Platform:** Microsoft Azure

Since the university already runs on Windows Server and Active Directory, Azure offers the smoothest migration path with minimal disruption. Microsoft Entra ID can extend the university's existing Active Directory into the cloud for unified identity management, and Azure's tight Microsoft 365 integration means staff and student accounts, email, and file storage can migrate with far less reconfiguration than switching to a different provider.

**Services to use:** Microsoft Entra ID (extend Active Directory), Azure Virtual Machines (Windows Server workloads), Azure Files, Azure Migrate.

---

### Client C – AI Research Company
**Scenario:** A research company develops AI and Machine Learning applications that require high-performance computing.

**Recommended Platform:** Google Cloud Platform (GCP)

GCP is the strongest choice for AI/ML-focused work because of its purpose-built Vertex AI platform and access to custom TPU (Tensor Processing Unit) hardware, which is optimized specifically for training large machine learning models faster and often more cost-effectively than general-purpose GPUs. GCP's deep ties to open-source tools like TensorFlow, which Google originally developed, further reduce friction for research teams.

**Services to use:** Vertex AI, Cloud TPUs, BigQuery (for large dataset analysis), Google Kubernetes Engine (for scaling training/inference workloads).

---

### Client D – Global E-Commerce Company
**Scenario:** A multinational online shopping company serves customers worldwide and requires highly available infrastructure with automatic scaling.

**Recommended Platform:** Amazon Web Services (AWS)

AWS has the largest global infrastructure footprint of any provider, with the most Regions and Availability Zones, which is critical for serving a worldwide customer base with low latency. Its mature auto-scaling and load-balancing tools (EC2 Auto Scaling, Elastic Load Balancing) combined with the broadest content-delivery network (CloudFront) make it the most proven option for large-scale, highly available e-commerce platforms.

**Services to use:** Amazon EC2 with Auto Scaling, Elastic Load Balancing, Amazon CloudFront (CDN), Amazon RDS (or DynamoDB for global tables).

---

