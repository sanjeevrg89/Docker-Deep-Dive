Docker CE Edition Installation:
====================

Ubuntu(apt based):
=======================

Add utils:
--------------
As root:

* apt-get install apt-transport-https ca-certificates curl software-properties-common

![Adding utilities](https://github.com/devops2201/Docker-Deep-Dive/blob/master/images/DockerInstall8.png)

Add Docker CE repo:
-------------------

* add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"

![Adding Repo](https://github.com/devops2201/Docker-Deep-Dive/blob/master/images/DockerInstall9.png)


Add GPG key:
------------

* curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

![GPG Key](https://github.com/devops2201/Docker-Deep-Dive/blob/master/images/DockerInstallkey.png)

Install Docker:
---------------

* apt-get install -y docker-ce

![Install Docker](https://github.com/devops2201/Docker-Deep-Dive/blob/master/images/DockerInstall10.png)

Check Docker Status:
-------------------------------

* systemctl status docker

![Status Docker](https://github.com/devops2201/Docker-Deep-Dive/blob/master/images/DockerInstall11.png)