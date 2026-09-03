# Laboratory 03 – Multi-Cloud Explorer

## Mission Overview

This laboratory activity explores and compares three major cloud computing platforms: Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP). The goal is to understand their services, advantages, infrastructure, and suitable business applications.

## Linux Investigation

A Linux server was investigated using a KillerCoda Linux Playground.

### Operating System

Command used:

```bash
cat /etc/os-release
```

The command was used to identify the operating system installed on the Linux server.

### CPU Information

Command used:

```bash
lscpu
```

The command was used to identify the processor, CPU architecture, number of CPUs, and other CPU information.

### Memory

Command used:

```bash
free -h
```

The command was used to check the total, used, and available memory of the Linux server.

### Disk Space

Command used:

```bash
df -h
```

The command was used to check the available and used disk space.

## Linux Cloud Migration

If this Linux server were migrated to the cloud, it could be hosted using virtual machine services from AWS, Azure, or GCP.

| Cloud Provider  | Service                |
| --------------- | ---------------------- |
| AWS             | Amazon EC2             |
| Microsoft Azure | Azure Virtual Machines |
| Google Cloud    | Compute Engine         |

### AWS

Amazon EC2 can host the Linux server as a virtual machine. It allows users to choose the operating system, CPU, memory, storage, and network configuration.

### Microsoft Azure

Azure Virtual Machines can run Linux operating systems in the cloud. It provides configurable virtual machines that can be scaled according to workload requirements.

### Google Cloud

Google Compute Engine can host Linux virtual machines. It provides customizable computing resources and can be used for applications, development, and enterprise workloads.

## Screenshots

### Operating System

![Linux Operating System](screenshots/linux-os.png)

### CPU
<img width="1325" height="785" alt="image" src="https://github.com/user-attachments/assets/f2cb1c11-e483-4b7b-842b-5ee6b503c4c6" />

![Linux CPU](screenshots/linux-cpu.png)

### Memory
<img width="667" height="77" alt="image" src="https://github.com/user-attachments/assets/e997fca4-9666-48da-8c14-ff6ed936ec47" />

![Linux Memory](screenshots/linux-memory.png)

### Disk Space

![Linux Disk](screenshots/linux-disk.png)
<img width="463" height="161" alt="image" src="https://github.com/user-attachments/assets/426e05f7-a6d0-49ce-bfb9-a8ae357dcd5f" />
