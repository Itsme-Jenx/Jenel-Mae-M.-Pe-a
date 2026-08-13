# Cloud Infrastructure Components

## 1. Compute Resources

### Purpose

Compute resources provide the processing power needed to run applications, commands, and services. They mainly include the CPU and memory (RAM) of a computer or cloud server.

### Importance in Cloud Computing

Compute resources are important because cloud applications need processing power to perform tasks. Cloud computing allows organizations to increase or decrease computing resources depending on their workload without having to purchase physical servers.

### KillerCoda Environment

The KillerCoda environment provides **1 vCPU** using an **Intel Xeon E312xx (Sandy Bridge, IBRS update)** processor. It also has approximately **1.96 GiB of RAM**. These resources allow the Linux virtual machine to execute commands and run applications.

---

## 2. Storage Resources

### Purpose

Storage resources provide space for saving the operating system, applications, files, and other data.

### Importance in Cloud Computing

Storage is important because cloud applications need a reliable place to store and retrieve data. Cloud storage also allows organizations to store large amounts of information without depending entirely on physical storage devices.

### KillerCoda Environment

The KillerCoda environment has a **19 GiB root filesystem** located at `/dev/vda1`. It has approximately **5.4 GiB used** and **13 GiB available**. Other mounted filesystems, such as `/dev/vda15` and `/dev/vda16`, are also available in the environment.

---

## 3. Networking Resources

### Purpose

Networking resources allow computers, servers, applications, and other devices to communicate with each other.

### Importance in Cloud Computing

Networking is important because cloud services need to communicate with users, applications, databases, and other services. Proper networking also helps control how resources communicate and provides connectivity to cloud-based systems.

### KillerCoda Environment

The KillerCoda server has a primary network interface called **enp1s0** with the IP address **172.30.1.2/24**. It also has a Docker bridge interface called **docker0** with the address **172.17.0.1/16**. These network resources allow the virtual machine and its services to communicate within their network environment.

---

## 4. Operating System

### Purpose

An operating system manages computer hardware and provides an environment where applications and commands can run.

### Importance in Cloud Computing

The operating system is important because it manages resources such as CPU, memory, storage, and networking. It also provides the tools and environment that cloud engineers use to manage and maintain servers.

### KillerCoda Environment

The KillerCoda environment is an **Ubuntu-based Linux virtual machine** running kernel version **6.8.0-136-generic**. The exact Ubuntu version could not be determined because the `/etc/os-release` file was not available. Linux provides the command-line environment used to inspect and manage the cloud server.

---

## Relationship Between the Components

The four components work together to provide a functional cloud environment. The **operating system** manages the available **compute, storage, and networking resources**, while the compute resources process applications, storage keeps data and files, and networking allows the server and its services to communicate. In the KillerCoda environment, these components work together inside a virtual machine to provide a basic cloud computing environment.

