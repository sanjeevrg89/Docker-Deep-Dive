Docker Introduction:
=====================

History of Docker:
------------------

* Docker was released in 2013 by a hosting company called Dot Cloud (Company no longer exists)
* It’s been 5 years since Docker was released and now it’s a revolution
* Huge shift in infrastructure [Mainframe to PC, Bare metal to Virtualization, Data Center to Cloud, Containers]

Overview of Docker:
-------------------

* Docker is an open source platform for developing, shipping, and running applications.
* Docker is an open-source project that automates the deployment of applications inside software containers, by providing an additional layer of abstraction and automation of operating system-level virtualization on Linux
* Docker packages an application and all its dependencies in a ‘virtual container’ so that it can be run on any Linux system or distribution
* Docker enables you to separate your applications from your infrastructure so you can deliver software quickly.
* Docker provides the ability to package and run an application in a loosely isolated environment called a container

What is Virtualization?
-----------------------
* Virtualization refers to the creation of a virtual resource such as a server, desktop, operating system, file, storage or network
* Server virtualization uses a software layer called a HYPERVISOR to emulate the underlying hardware
* Virtualization software allows you to set up one operating system within another

Hypervisor:
-----------
* Hypervisor decouples the virtual machines from the host and dynamically allocates computing resources to each virtual machine

Virtual Machines versus Containers:
-----------------------------------
![VM's vs containers](https://github.com/devops2201/Docker-Deep-Dive/blob/master/ContainersvsVMs.png)

VMs:
----
* Virtual machines (VMs) are an abstraction of physical hardware turning one server into many servers
* Virtual machines are emulation of a specific computer system type
* The physical, "real-world" hardware running the VM is generally referred to as the 'HOST', and the virtual machine emulated on that machine is generally referred to as the 'GUEST'. A HOST can emulate several GUESTS, each of which can emulate different operating systems and hardware platforms
* A virtual machine is	isolated from the hardware	and	has to communicate with	the hardware through a Hypervisor
* The hypervisor allows multiple VMs to run on a single machine. Each VM includes a full copy of an operating system, the application, necessary binaries and libraries - taking up tens of GBs
* VMs can also be slow to boot

Containers:
-----------
* Containers are an abstraction at the app layer that packages code and dependencies together
* Multiple containers can run on the same machine and share the OS kernel with other containers, each running as isolated processes in user space
* Containers take up less space than VMs (container images are typically tens of MBs in size), can handle more applications and require fewer VMs and Operating systems
* Containers are light weight
* Containers do not have their own kernel
* Containers share the host machine’s kernel, making them much smaller in size compared to virtual machines
* Containers use process level isolation, allowing processes inside a container to be isolated from other containers


Docker Components:
------------------
* Docker Daemon
* Docker Client
* Docker.io Registry
