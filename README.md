# Cloud-computing-
Concepts of cloud computing, basics, related topics details 

![Screenshot_2024_0918_123427](https://github.com/user-attachments/assets/9b54d9e2-5cb2-4a28-a145-9a5e9fb7490a)

# Cloud Computing:- 

Cloud computing is the delivery of computing services—including servers, storage, databases, networking, software, analytics, and intelligence—over the Internet ("the cloud"). This allows for faster innovation, flexible resources, and economies of scale.

![Screenshot_2024_0918_123503](https://github.com/user-attachments/assets/5301d869-b3ae-46c5-9d6c-8bc54028f445)

# Docker:- 

Docker is a software platform that allows you to build, test, and deploy applications quickly. Docker packages software into standardized units called containers that have everything the software needs to run including libraries, system tools, code, and runtime. Using Docker, you can quickly deploy and scale applications into any environment and know your code will run.

![Screenshot_2024_0918_124023](https://github.com/user-attachments/assets/03fdbbef-5f0d-4a17-8797-f8e8ca8a5f58)
 
 # Key features of Docker include:-;

# 1.Containerization: 
Applications run in isolated environments, which makes them portable and easy to manage.

# 2. Images and Dockerfile: 
Docker uses images as blueprints for containers. A Dockerfile is a script that contains instructions to build an image.

# 3. Docker Hub:
A cloud-based registry where users can share and distribute Docker image

# How Docker works:- 

Docker works by providing a standard way to run your code. Docker is an operating system for containers. Similar to how a virtual machine virtualizes .containers virtualize the operating system of a server. Docker is installed on each server and provides simple commands you can use to build, start, or stop containers.

![Screenshot_2024_0918_123713](https://github.com/user-attachments/assets/332ee150-9a0a-4ca4-911e-91eec2471109)

# What is the structure of a Docker image?:- 

A Docker image is composed of multiple layers stacked on top of each other. Each layer represents a specific modification to the file system (inside the container), such as adding a new file or modifying an existing one. Once a layer is created, it becomes immutable, meaning it can't be changed.16 May 2023

![Screenshot_2024_0918_124113](https://github.com/user-attachments/assets/57b191a7-c6aa-40d8-ae5b-336b9d8a8029)


# HOW TO INSTALL DOCKER:- 

To install Docker on a remote server using PuTTY, you'll first need to ensure you have access to a Linux server (like Ubuntu, CentOS, etc.) via SSH. Here's a step-by-step guide:

## Step 1:Connect to Your Server


## Step 2: Update Your Package Index

Before installing Docker, it’s a good idea to update the package index:

```bash
sudo apt update
```


## Step 3:Install Prerequisites

For Ubuntu, install the required packages:

```bash
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```

For CentOS, run:

```bash
sudo yum install -y yum-utils
```

## Step 4: Add Docker’s Official GPG Key

For Ubuntu:

```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

For CentOS:

```bash
sudo rpm --import https://download.docker.com/linux/centos/gpg
```

## Step 5: Set Up the Stable Repository
For Ubuntu:

```bash
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```


For CentOS:

```bash
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
```

## Step 6: Install Docker

For Ubuntu:

```bash
sudo apt update
```

```bash
sudo apt install docker-ce
```

For CentOS:

```bash
sudo yum install docker-ce
```

## Step 7: Start Docker

Enable and start the Docker service:


```bash
sudo systemctl start docker
```

```bash
sudo systemctl enable docker
```

## Step 8: Verify the Installation

Check if Docker is running:

```bash
sudo systemctl status docker
```

You can also run a test container:

```bash
sudo docker run hello-world
```

## Step 9: (Optional) Manage Docker as a Non-Root User

If you want to run Docker commands without sudo, add your user to the 

Docker group:

```bash
sudo usermod -aG docker $USER
```

After running this command, log out and back in for the changes to take effect.

# Conclusion

You’ve successfully installed Docker using PuTTY! If you have any questions or run into issues, feel free to ask.

# container:-

A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another. A Docker container image is a lightweight, standalone, executable package of software that includes everything needed to run an application: code, runtime, system tools, system libraries and settings.

(in other and simple words )

Containers are an abstraction at the app layer that packages code and dependencies together. Multiple containers can run on the same machine and share the OS kernel with other containers, each running as isolated processes in user space. Containers take up less space than VMs (container images are typically tens of MBs in size), can handle more applications and require fewer VMs and Operating systems

![Screenshot_2024_0918_124201](https://github.com/user-attachments/assets/6f6cd7ae-eee7-4b0b-b614-313b4e8000bd)

# NGINX:-

NGINX is a high-performance web server and reverse proxy server that is widely used for serving web applications, handling HTTP and HTTPS requests, and load balancing traffic. It is known for its speed, efficiency, and ability to handle a large number of concurrent connections with low resource usage.

![Screenshot_2024_0918_140523](https://github.com/user-attachments/assets/ff5971c8-d6b8-434e-b93a-8476dc5a8f83)

# HOW TO INSTALL NGINX :-
In this tutorial, we’ll show you how to install NGINX on Linux.

## Open your Linux machine and run an update using the command below:

```bash
sudo apt-get update
```

Next, run this command:

```bash
sudo apt-get install nginx
```

## Then, enable your firewall with the following:

```bash
sudo ufw enable
```

## To verify NGINX is installed, run the following:

```bash
nginx -v
```

## You can run the command below to find out if NGINX is running:

```bash
sudo ufw status
```

After running this command, you should see the following:

status: active

## To check whether your NGINX server is working fine, run the following:

```bash
sudo systemctl status nginx
```

# using EC2 in aws:-

First open aws search EC2 then Launch Instance and there select keypair in putty then download it

after that Launch it and run putty and paste public id on HOST NAME and open that downloaded key pair for putty in SSH then Auth then Credentials and open there

## after that run it and write username as ubuntu as selected os and then type following commands

```bash
sudo apt update
```


```bash
sudo apt install apache2
```

## to install a web server on ip then

```bash
sudo su
```

## for convert $ into # for getting admin role then

```bash
cd /var/www/html/
```

##then

```bash
ls
```

## for list of html file in it

## then copy that html file name and write

```bash
rm index.html
```

```bash
rm means remove command
```

```bash
vi index.html
```

## this will open a notepad like and write html code there like (vi is editor) -

## then press ctrl+c then shift+colon then write wq and enter

## now copy your public ip and paste it on browser you will see the texts written by you (by using html above)

# congratulations you got it 👏🏻 🎉 


# USING CONTAINER IN VM and adding nginx server by Docker:- 

First open aws search EC2 then Launch Instance and there select keypair in putty then download it

after that edit network setting and click on add security group rule and select TCP,UDP,ALL TRAFFIC AND SELECT EVERYWHERE SOURCE TYPE IN THEM then Launch it and run putty and paste public id on HOST NAME and open that downloaded key pair for putty in SSH then Auth then Credentials and open there

after that run it and write username as ubuntu as selected os and then type following commands

```bash
curl -sL https://github.com/ShubhamTatvamasi/docker-install/raw/master/docker-install.sh | bash
```

## this will install and run docker in your vm

```bash
newgrp docker
```

## this command will help us to use docker

```bash
docker ps
```

## this will list docker

```bash
docker --version
```

## this will display the version of docker installed

## now installing nginx

```bash
docker pull nginx
```

## You can download Nginx from a pre-built Docker image, with a default Nginx configuration, by above command. This downloads all the necessary components for the container.

```bash
docker run --name docker-nginx -p 80:80 nginx
```

## Nginx installed, you can configure the container so that it’s publicly accessible as a web server.

## run is the command to create a new container

## The --name flag is how you specify the name of the container. If left blank, a generated name like nostalgic_hopper will be assigned.

## -p specifies the port you are exposing in the format of -p local-machine-port:internal-container-port. In this case, you are mapping port :80 in the container to port :80 on the server.

## nginx is the name of the image on Docker Hub.

## now this will show this on your public ip

![Screenshot_2024_0923_210801](https://github.com/user-attachments/assets/12ed503f-9c71-4c80-bcb3-468c989c0258)

## In your terminal, enter CTRL+C to stop the container from running.

```bash
docker ps -a
```

## verify the container status with this command

```bash
docker rm docker-nginx
```

## Remove the existing container

```bash
docker run --name docker-nginx -p 80:80 -d nginx
```

## Create a new, detached Nginx container,By attaching the -d flag, you are running this container in the background.

```bash
docker ps
```
## this will obtain info about your container

```bash
docker stop docker-nginx
```

## Stop the container

```bash
docker rm docker-nginx
```

## remove the container

# Building a Web Page to Serve on Nginx

```bash
mkdir -p ~/docker-nginx/html
```

## Create a new directory for your website content within the home directory

```bash
cd ~/docker-nginx/html
```

## by this you navigate into this

```bash
vi index.html
```

## now press i and write your code in html like 


![Screenshot_2024_0923_211405](https://github.com/user-attachments/assets/7cd1afd2-b42e-43c1-94ed-86a1f1ebedf9)

## then press ctrl+c then shift+colon then write wq and enter

```bash
docker run --name docker-nginx -p 80:80 -d -v ~/docker-nginx/html:/usr/share/nginx/html nginx
```

Linking the Container to the Local Filesystem

## open your public ip in browser you will see as the content as your html code

# here you go 👏🏻

# Using Your Own Nginx Configuration File

```bash
cd ~/docker-nginx
```


```bash
docker cp docker-nginx:/etc/nginx/conf.d/default.conf default.conf
```

## Copy the Nginx config directory into your project folder

```bash
docker stop docker-nginx
```

```bash
docker rm docker-nginx
```

## to rebuild the container stop the container then remove it

```bash
docker run --name docker-nginx -p 80:80 -v ~/docker-nginx/html:/usr/share/nginx/html -v ~/docker-nginx/default.conf:/etc/nginx/conf.d/default.conf -d nginx
```

## This command links the custom website pages to the container.

```bash
docker restart docker-nginx
```

## you need to restart your container to reflect changes on the associated pages.

# Orchestration:- 

In cloud computing, orchestration is the process of coordinating and automating the management of applications, tools, and infrastructure across multiple clouds
 
![Screenshot_2024_0923_184155](https://github.com/user-attachments/assets/08cd23e3-bead-46aa-a5be-68cd56fea693)

![Screenshot_2024_0923_184219](https://github.com/user-attachments/assets/75b648c0-2fc1-46c1-b8d0-8ecfb0bd2299)

![Screenshot_2024_0923_183854](https://github.com/user-attachments/assets/6756ddf2-6d9d-4b0d-a4d1-a7aee4ef3afd)

# Kubernestes :- 

Kubernetes (sometimes shortened to K8s with the 8 standing for the number of letters between the “K” and the “s”) is an open source system to deploy, scale, and manage containerized applications anywhere.

Kubernetes has built-in commands to handle a lot of the heavy lifting that goes into application management, allowing you to automate day-to-day operations. You can make sure applications are always running the way you intended them to run.

![Screenshot_2024_0923_215514](https://github.com/user-attachments/assets/33116348-3bf9-48cb-8403-51f9696905d7)

# Minikube:-

Minikube is a tool that sets up a Kubernetes environment on a local PC or laptop. This tool  provides an easy means of creating a local Kubernetes environment on any Linux, Mac, or Windows system, where you can experiment with and test Kubernetes deployments.

![Screenshot_2024_0923_215611](https://github.com/user-attachments/assets/bbcf6b38-9f8b-4e7e-a768-601033a8df1c)

![Screenshot_2024_0923_215736](https://github.com/user-attachments/assets/c792b3bb-9bda-4b5c-8d80-aa31b3c5b450)

# USING MINIKUBE IN AWS

##First open aws search EC2 ,and download your passkey then Launch Instance and select 22.04 AMI then select t2.xlarge instance type then select keypair then configure storage to 30 GB then enable all traffic in network and Launch.

##Launch PuTTY and add the IP address from instance and add key pair file and open the PuTTY terminal.

## Now connect it with putty and login into it by writing ubuntu

## Now put some commands


```bash
curl -sL https://github.com/ShubhamTatvamasi/docker-install/raw/master/docker-install.sh | bash
```

## it will install docker


```bash
sudo usermod -aG docker $USER
```

```bash
newgrp docker
```

## it will Add your local user to docker group so that your local user run docker commands


```bash
sudo snap install kubectl --classic
```

## it will intall kubernetes


```bash
kubectl version --client
```

## it checks the version

# Installing Minikube

```bash
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
```


```bash
sudo install minikube-linux-amd64 /usr/local/bin/minikube
```

```bash
minikube version
```

## it checks its version

## Starting Minikube with Docker Driver

```bash
minikube start --driver=docker
```

# If you encounter root privileges error, run:


```bash
minikube start --driver=docker --force
```

```bash
minikube status
```

## it checks its status


```bash
kubectl cluster-info
```

## it checks cluster info


```bash
kubectl config view
```

## it will show the config


```bash
kubectl get nodes
```

## it will display nodes in it

```bash
kubectl get pods
```

## it will show pods in it

```bash
kubectl create deployment nginx-web --image=nginx
```

```bash
kubectl expose deployment nginx-web --type NodePort --port=80
```
kubectl get deployment,pod,svc

## it will deploy a sample nginx deployment


```bash
minikube addons list
```


```bash
It will display all addons
```


```bash
minikube addons enable dashboard
```

```bash
minikube addons enable ingress
```

## this enables these addons

```bash
minikube dashboard --url**
```

# it will get the url and run the dashboard of MiniKube


```bash
kubectl proxy --address='0.0.0.0' --disable-filter=true &
```


## This will enable port :8001 to access it on your public ip


```bash
http://server_ip:8001/api/v1/namespaces/kubernetes-dashboard/services/http:kubernetes-dashboard:/proxy/#/workloads?namespace=default
```

# in browser replace server ip with public ip

# Now go to above link and replace server_ip with your public ip and it will show you like :

![Screenshot_2024_0923_213426](https://github.com/user-attachments/assets/16ca5aa7-e6db-47d4-b005-2794b6c4289b)

# KVM:- Kernel-based Virtual Machine

It is a technology that allows you to run multiple operating systems on a single physical machine. It turns the Linux kernel into a hypervisor, enabling virtual machines (VMs) to operate as if they were separate computers. 

![Screenshot_2024_1104_185025](https://github.com/user-attachments/assets/aea55019-b763-4d9d-b8e1-05dec28115e5)

# Openstack :-

OpenStack is an open-source platform that lets you create and manage cloud computing services. It allows users to control computing power, storage, and networking in a data center through a web interface. Essentially, it helps organizations build their own private or public clouds, making it easier to deploy and manage applications.

![Screenshot_2024_1104_185043](https://github.com/user-attachments/assets/c0c86085-1b3c-4cd3-8276-11adebfbba49)

# QEMU

QEMU is an open-source emulator and virtualization tool that allows you to run different operating systems on a host machine.

![Screenshot_2024_1104_185120](https://github.com/user-attachments/assets/0a1473de-99d1-4119-b9dd-236278fd6341)


# VPC

•Go to VPC and create a VPC then we 
 have to create 4 subnets , where 2     subnets are private and other two are  public .

![Screenshot_2024_1104_181237](https://github.com/user-attachments/assets/25f8774d-56f0-426e-8cf2-eee68511767e)


![Screenshot_2024_1104_181126](https://github.com/user-attachments/assets/0512bbc2-f00c-4f5e-b853-63032d26e6e1)

## create  gateways:- 

 1st  create INTERNET GATWAY , whic is  to be connected to your VPC which is   created earliy.

![Screenshot_2024_1104_181831](https://github.com/user-attachments/assets/a3bb96a9-b738-4031-a65b-d169b25fd263)


•2nd we have to create VPG virtual      privaye gate, and connect to VPC .

## create route tables 

•Now we have to go to the route table   and create 2 route table , one for     IGW and another for VGW .

![Screenshot_2024_1104_181847](https://github.com/user-attachments/assets/77c3730e-5cf4-4a0d-a78d-ac070f231688)

•Now we have to connect two public      subnet in myigw and on other we have   to add the private subnets .

![Screenshot_2024_1104_182425](https://github.com/user-attachments/assets/555833f8-2889-4028-b563-89596c844143)

## create instances

• now we have to create two instnaces    where we have to enable the public     IPv4 .

•then on both instance we have to       downlaod the web server here i have    downlaoded the apache2 server

-- after that i chech that my             instances are working or not .

![Screenshot_2024_1104_182258](https://github.com/user-attachments/assets/c913fb61-bc91-43d2-bd2a-47fdba5e508e)

## now we have to create the load         balancer

--where we have to give vpc, aviablity   zone of the ec2 instance

•then we have to create the target      group where we have to select the two  insatance we have create then we have  to go to helath check edited option    which was present below the load       balancer is create ,then edit it as    given below image


![Screenshot_2024_1104_182902](https://github.com/user-attachments/assets/0ae0ab8a-9196-486b-ad41-b9e27c901240)

•after that come to load balancer       where we have to select the target     group which we have created then make  the load balancer , it will look like  the given image below .

![Screenshot_2024_1104_183106](https://github.com/user-attachments/assets/a891ba72-6a20-4f33-89c2-cbe07cd88904)

![Screenshot_2024_1104_183126](https://github.com/user-attachments/assets/1c5a8cf9-ff8d-4565-8968-7d1c0df5920a)

*now put on any one instance write following commands in putty -*

* ```
  htop
  ```
  ```
  seq 999999999999999999999999999999999999999999999999999999999 > /dev/null &
  ```
  ```
  htop
  ```

  ![Screenshot_2024_1104_183758](https://github.com/user-attachments/assets/bae13bf3-7e99-4944-86fb-156efc303382)

### book link for reference of VPC given below (page 55 )

{ https://www.scribd.com/document/454176546/AWS-lab-practice-guide-by-www-server-computer-com-v1
}


![Screenshot_2024_1105_055750](https://github.com/user-attachments/assets/268cad3b-5081-4e9b-9f17-a5aa70d6de41)


# NETWORKING 

![Screenshot_2024_1105_055827](https://github.com/user-attachments/assets/e060004d-ad36-482b-9128-ad60ad5ee88a)


## Network Devices:-

### 1. network adaptor/ interface 
   • connects a device to network. 
   • has a Mac address by manufacturer 
   • second layer device 

### 2. switch 
   •it is a very multiport network         bridge that uses MAC address to        forward data
   •link layer device 

### 3. Router 
   •it is a device that forwards          data between computer networks
   • 3rd layer device 

### 4. HUB 
   •network device that used to            connect multiple computers in a        network 
   • all information send to the hub       is automatically send to each port     to every device 

### 5. TAP
  (WORKS ON LAYER 2 -- ethernet frame )

used to create a user space network bridge.

### 6. TUN 
 ( WORKS ON LAYER 3 -- IP packets )

 create a tunnel network to reach       another network .
   
## Basic terms for understanding networking better:- 

### NAT :- 

it is a process in which one or more local IP addresses are translated into one or more global IP addresses and vice versa

### veth :-

these are pair of virtual network interfaces that are used to connect network namespaces together.

### DPDK :- Data Plane Development Kit

it is a set of libraries and drivers that accelerates packet processing and their ability to create packet forwarders without the need of costly custom switches and routers

 ### NIC :- network interface card 

 It allows one device to connect to     network

 ### DPU :- Data Processing Unit 

 it is a new programmable processor that helps move data around data centres. it ensures right data goes to right place in right format quickly .

### CSI :- Container Storage Interface 


### OVS :- Open virtual switch 

it is used with hypervisors to interconnect virtual machines within a host and between different hosts accross networks.

### QEMU :- Quick emulator 

free open source machine it can run various guest operating systems (OS's ) and architecture on a single host system.

### Docker :- 

it is like a container that holds everything your application needs to run including the code, libraries.

### Kubernets :- 

it is like a manager for containers .it helps to deploy, scale and manage a group of containers making sure they run smoothly.

### web assembly:- (WASM)

technology that allows you to run code written in different programming languages. It is a way to build high speed, responsive web applications that can handle data and communicate over networks.

### Firewall :- 
security system that controls incoming and outgoing network traffic based on pre- determined security rules.

### VxLAN :- 
It is tunneling report that tunnel Ethernet traffic (layer 2) over an IP network(layer 3).

  #### VTEP:- 
   it is a device that's responsible      for encapsulating and de-capsulating
   layer 2 traffic.

### LINUX Bridge :- 

it is a kernel module that behaves like a network switch .It is usually used for forwarding packages on routes or gateways or between virtual machines.

### Pktgen :- 
it is a tool for high speed package generation and testing. It  in the Linux kernel.

#### netns :- network namespace 
 feature of Linux kernel that provides a way to create isolated network environment.

***TAP is often used to connect VM or containers to a physical network***

## KVM :- kernel virtual machine 
( typer 1 hypervisor)


## CNI :- Container Networking Bridge 

it is responsible for setting up the network ( assigning IP address, create network bridge) for containers ,enabling communication between containers and outside world

***examples***
VLAN , IPvLAN , CALICO , FLANNEL , VMware. etc 

### Flannel :- 
it acts as a layer that allows containers to send and receive data seamlessly accross various hosts .
 
  ### working:- 
  it runs a small single binary agent    on every host.
  this networking tool gives every       host an IP subnet.

  

## Packet Switching:- 

when we send email or web page the data does not travel as single continuous stream instead is broken down into smaller chunks called packets .

## key functions of network core :-

## 1. Forwarding :- 
  
• it is a local action of moving and     arriving packets from a router's       input to appropriate router output     link.

## 2. Routing :- 
 • global process of determining the      full paths packets take from source    to destination

## Network Protocols:- 
set of rules that determine how the packet is to be transferred and received and in which format .

### 1. TCP 
 
  it ensures reliable order delivery of data between applications . It handles things like breaking data into packets

### 2. IP 

 responsible for addressing and routing packets across the internet. 
 
### 3. HTTP 

 it is a protocol that powers the world wide web defining how messages are formatted and transmitted between web browsers and servers.

## NETWORK STACK 

 ### TCP /IP 
 provide reliable transmission of       data. 

 ### UDP 
  provides faster but less reliable      transmission of data.
  



