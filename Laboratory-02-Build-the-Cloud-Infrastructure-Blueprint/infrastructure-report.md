# Infrastructure Report

## Operating System

* **Operating System:** Ubuntu-based Linux environment
* **Kernel Version:** 6.8.0-136-generic

> Note: The `/etc/os-release` file was not available in the environment, so the exact Ubuntu version could not be determined.

## CPU

* **CPU Model:** Intel Xeon E312xx (Sandy Bridge, IBRS update)
* **Number of CPU Cores:** 1 vCPU

## Memory

* **Total RAM:** 1.96 GiB

## Storage

* **Root Disk:** `/dev/vda1`
* **Total Disk Capacity:** 19 GiB
* **Used:** 5.4 GiB
* **Available:** 13 GiB
* **Usage:** 30%

### Mounted File Systems

| File System         | Total | Used | Available | Usage |
| ------------------- | ----: | ---: | --------: | ----: |
| `/dev/vda1`         |   19G | 5.4G |       13G |   30% |
| `/dev/vda16`        |  881M | 117M |      703M |   15% |
| `/dev/vda15`        |  105M | 6.2M |       99M |    6% |
| `/run` (tmpfs)      |  191M |    — |         — |     — |
| `/dev/shm` (tmpfs)  |  952M |    — |         — |     — |
| `/run/lock` (tmpfs) |  5.0M |    — |         — |     — |

## Network

* **Hostname:** `ubuntu`
* **Primary IP Address:** `172.30.1.2/24`
* **Network Interface:** `enp1s0`
* **Docker Bridge:** `172.17.0.1/16`
* **Loopback Address:** `127.0.0.1/8`

## Virtualization

The environment is running as a virtual machine using KVM virtualization.

## Linux Commands Used

```bash
cat /etc/os-release
uname -r
lscpu
nproc
free -h
df -h
findmnt
hostname
hostname -I
```

## Summary

The KillerCoda environment is an Ubuntu-based virtual machine running kernel version `6.8.0-136-generic`. It provides 1 vCPU, approximately 2 GiB of RAM, and a 19 GiB root disk. Its primary network address is `172.30.1.2/24`, while Docker uses the `172.17.0.0/16` bridge network. The exact operating system version could not be determined because `/etc/os-release` was not available.

