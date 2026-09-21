# Types of Cloud Storage

| Storage Type | Description (How does it store data?) | Primary Use Case (What is it best used for?) | Cloud Provider Example |
|---|---|---|---|
| **Block Storage** | Breaks data into fixed-size blocks, each with its own address. Blocks are stored separately and reassembled by the OS/application when read, similar to how a traditional hard drive is partitioned into sectors. Requires an OS to be attached to and formatted before use. | High-performance, low-latency workloads that need to behave like a raw disk — databases, boot volumes for virtual machines, transactional applications. | AWS EBS (Elastic Block Store) |
| **File Storage** | Organizes data in a hierarchical structure of files and folders, accessed through a shared file system protocol (like NFS or SMB). Multiple servers/users can mount and access the same file system at once. | Shared access scenarios where many users or applications need to read/write the same files — home directories, content management systems, shared application data. | AWS EFS (Elastic File System) |
| **Object Storage** | Stores data as discrete, self-contained "objects" (the data itself, metadata, and a unique identifier) inside a flat address space instead of a folder hierarchy. Objects are accessed via a simple HTTP API (GET/PUT) rather than a file system. | Storing massive amounts of unstructured data that doesn't change often — images, videos, backups, logs, static website assets. | AWS S3 (Simple Storage Service) |

## Why Object Storage is Best for the Client's Use Case

Object storage is the right choice for a photo-sharing application because it is built to scale horizontally to handle millions (or billions) of files without the performance bottlenecks that block or file storage would hit at that volume. Each photo is stored as an independent object with rich metadata (upload date, user ID, file type), which makes it easy to retrieve, tag, and serve directly over HTTP/HTTPS without mounting a drive or managing a file system. Because object storage is accessed over a simple web API, it's also inherently durable, redundant, and accessible from anywhere — exactly what's needed for user-uploaded content that must be available globally and never lost.

