
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

## sudo apt install net-tools

````ubuntu@discipl:~$ sudo apt install net-tools
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following NEW packages will be installed:
  net-tools
0 upgraded, 1 newly installed, 0 to remove and 3 not upgraded.
Need to get 196 kB of archives.
After this operation, 864 kB of additional disk space will be used.
Get:1 http://eu-amsterdam-1-ad-1.clouds.archive.ubuntu.com/ubuntu focal/main amd64 net-tools amd64 1.60+git20180626.aebd88e-1ubuntu1 [196 kB]
Fetched 196 kB in 0s (2781 kB/s)
Selecting previously unselected package net-tools.
(Reading database ... 68756 files and directories currently installed.)
Preparing to unpack .../net-tools_1.60+git20180626.aebd88e-1ubuntu1_amd64.deb ...
Unpacking net-tools (1.60+git20180626.aebd88e-1ubuntu1) ...
Setting up net-tools (1.60+git20180626.aebd88e-1ubuntu1) ...
Processing triggers for man-db (2.9.1-1) ...
ubuntu@discipl:~$ ifconfig
docker0: flags=4099<UP,BROADCAST,MULTICAST>  mtu 1500
        inet 172.17.0.1  netmask 255.255.0.0  broadcast 172.17.255.255
        inet6 fe80::42:f3ff:feeb:b172  prefixlen 64  scopeid 0x20<link>
        ether 02:42:f3:eb:b1:72  txqueuelen 0  (Ethernet)
        RX packets 0  bytes 0 (0.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 7  bytes 746 (746.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

ens3: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9000
        inet 10.0.0.3  netmask 255.255.255.0  broadcast 10.0.0.255
        inet6 fe80::17ff:fe00:cd06  prefixlen 64  scopeid 0x20<link>
        ether 02:00:17:00:cd:06  txqueuelen 1000  (Ethernet)
        RX packets 35243  bytes 119626174 (119.6 MB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 23719  bytes 9114008 (9.1 MB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 3138  bytes 348874 (348.8 KB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 3138  bytes 348874 (348.8 KB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
````