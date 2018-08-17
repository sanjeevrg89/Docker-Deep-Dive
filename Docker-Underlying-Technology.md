Underlying Technology:
======================

* Docker is written in Go programming language
* Docker uses several features of the Linux kernel to deliver its functionality

Namespaces:
===========
* Docker uses a technology called namespaces to provide the isolated workspace called the container
* When you run a container, Docker creates a set of namespaces for that container.
* Namespaces provide **isolation** so that other pieces of the system remain unaffected by whatever is within that namespace

Types:
------
1. pid -> Process isolation (Process ID)
2. mnt -> Managing filesystem mount points (Mount)
3. ipc -> Managing access to IPC resources (InterProcess Communication)
4. net -> Managing network interfaces (Network)
5. user
6. uts -> Isolating kernel and version identifiers (Unix Timesharing System)

Control Groups:
===============
* Also reffered to as 'cgroups'
* Provide resource limitation and reporting capability within container space
* Allows granular control over what host resources are allocated to containers and when they are allocated
* Control groups allow Docker Engine to share available hardware resources to containers and optionally enforce limits and constraints
* Common cgroups: CPU, Memory, Network bandwidth, Disk, priority


Docker uses which file system??
-------------------------------
**Union File System**

* Called as Layered file system
* Union File system operates by creating layers, making them very lightweight and fast
* Docker Engine uses Union FS to provide the building blocks for containers
* Variants: **DeviceMapper**, **AUFS**, **BTRFS** & **VFS**

Container Format:
-----------------
* Docker Engine combines the namespaces, control groups, and UnionFS into a wrapper called a container format
* Default is: **libcontainer**