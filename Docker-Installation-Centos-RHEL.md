Docker CE Edition Installation:
====================

CentOS/RHEL(yum based):
=======================

Add yum utils:
--------------

* yum install -y yum-utils device-mapper-persistent-data lvm2

![Adding utilities](https://github.com/devops2201/Docker-Deep-Dive/blob/master/images/DockerInstall1.png)

Add Docker CE repo:
-------------------

* yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo

![Adding Repo](https://github.com/devops2201/Docker-Deep-Dive/blob/master/images/DockerInstall2.png)

Install Docker:
---------------

* yum install -y docker-ce

![Install Docker](https://github.com/devops2201/Docker-Deep-Dive/blob/master/images/DockerInstall3.png)

![Install Docker](https://github.com/devops2201/Docker-Deep-Dive/blob/master/images/DockerInstall4.png)

Enable Docker and Start Docker:
-------------------------------

* systemctl enable docker && systemctl start docker

![Enable and Start Docker](https://github.com/devops2201/Docker-Deep-Dive/blob/master/images/DockerInstall5.png)


To run docker commands as a non-root user:
------------------------------------------

* First navigate to this location as root
  * cd /var/run
  * ls -al docker.sock
  * You will see root can run docker commands

* Add a non-root user to Docker group:
  * usermod -aG docker <username>


![Non-Root User](https://github.com/devops2201/Docker-Deep-Dive/blob/master/images/DockerInstall6.png)
![Non-Root User](https://github.com/devops2201/Docker-Deep-Dive/blob/master/images/DockerInstall7.png)