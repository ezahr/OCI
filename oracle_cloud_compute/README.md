
# ssh ubuntu@ 158.101.192.41 






## cloud-init.txt

[azure](https://github.com/ezahr/Waardepapieren-AZURE-ACI/wiki/virtual-machines-linux-ubuntu-docker-compose-stack-discipl.westeurope.cloudapp.azure.com-quickstart)

#include https://get.docker.com



https://console.eu-amsterdam-1.oraclecloud.com/compute/instances/ocid1.instance.oc1.eu-amsterdam-1.anqw2ljr3khhbricc3cn6ymqsrh35w7zmbnb7dpskpyquanygo35svohdx6q/work-requests




Internal FQDN:
 discipl.subnet.vcn.oraclevcn.com

 Public IP Address:
 158.101.192.41 

 ## ssh ubuntu@ 158.101.192.41 

 ````
boscp08@kubernetes-worker2:~$ ssh ubuntu@158.101.192.41
Welcome to Ubuntu 20.04 LTS (GNU/Linux 5.4.0-1009-oracle x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  System information as of Fri Jun 12 15:19:48 UTC 2020

  System load:  0.01              Processes:                123
  Usage of /:   4.5% of 44.97GB   Users logged in:          0
  Memory usage: 40%               IPv4 address for docker0: 172.17.0.1
  Swap usage:   0%                IPv4 address for ens3:    10.0.0.3

 * MicroK8s gets a native Windows installer and command-line integration.

     https://ubuntu.com/blog/microk8s-installers-windows-and-macos

8 updates can be installed immediately.
8 of these updates are security updates.
To see these additional updates run: apt list --upgradable


Last login: Fri Jun 12 14:18:16 2020 from 86.86.102.241
ubuntu@discipl:~$ 

 ````


## ubuntu@discipl:~$ sudo apt install docker-compose

## ubuntu@discipl:~$ docker-compose --version
docker-compose version 1.25.0, build unknown

##  ubuntu@discipl:~$ git --version
git version 2.25.1



## sudo usermod -aG docker ubuntu

## docker run hello-world

````
ubuntu@discipl:~$ docker run hello-world

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/

````

