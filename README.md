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

# Step 1:Connect to Your Server


# Step 2: Update Your Package Index

Before installing Docker, it’s a good idea to update the package index:

sudo apt update

# Step 3:Install Prerequisites

For Ubuntu, install the required packages:

sudo apt install apt-transport-https ca-certificates curl software-properties-common

For CentOS, run:

sudo yum install -y yum-utils

# Step 4: Add Docker’s Official GPG Key

For Ubuntu:

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

For CentOS:

sudo rpm --import https://download.docker.com/linux/centos/gpg

# Step 5: Set Up the Stable Repository
For Ubuntu:

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

For CentOS:

sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo

# Step 6: Install Docker

For Ubuntu:

sudo apt update

sudo apt install docker-ce

For CentOS:

sudo yum install docker-ce

# Step 7: Start Docker

Enable and start the Docker service:


sudo systemctl start docker

sudo systemctl enable docker

# Step 8: Verify the Installation

Check if Docker is running:

sudo systemctl status docker

You can also run a test container:

sudo docker run hello-world

# Step 9: (Optional) Manage Docker as a Non-Root User

If you want to run Docker commands without sudo, add your user to the 

Docker group:

sudo usermod -aG docker $USER

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

# Open your Linux machine and run an update using the command below:

sudo apt-get update

Next, run this command:

sudo apt-get install nginx

Then, enable your firewall with the following:

sudo ufw enable

To verify NGINX is installed, run the following:

nginx -v

You can run the command below to find out if NGINX is running:

sudo ufw status

After running this command, you should see the following:

status: active

To check whether your NGINX server is working fine, run the following:

sudo systemctl status nginx

# using EC2 in aws:-

-First open aws search EC2 then Launch Instance and there select keypair in putty then download it

-after that Launch it and run putty and paste public id on HOST NAME and open that downloaded key pair for putty in SSH then Auth then Credentials and open there

-after that run it and write username as ubuntu as selected os and then type following commands

sudo apt update


sudo apt install apache2

[to install a web server on ip then]

sudo su

[for convert $ into # for getting admin role then]

cd /var/www/html/

then

ls

[for list of html file in it]

then copy that html file name and write

rm index.html

[rm means remove command]

vi index.html

[this will open a notepad like and write html code there like (vi is editor) -]

then press ctrl+c then shift+colon then write wq and enter

now copy your public ip and paste it on browser you will see the texts written by you (by using html above)

# congratulations you got it 👏🏻 🎉 


# USING CONTAINER IN VM and adding nginx server by Docker:- 

--First open aws search EC2 then Launch Instance and there select keypair in putty then download it

--after that edit network setting and click on add security group rule and select TCP,UDP,ALL TRAFFIC AND SELECT EVERYWHERE SOURCE TYPE IN THEM then Launch it and run putty and paste public id on HOST NAME and open that downloaded key pair for putty in SSH then Auth then Credentials and open there

--after that run it and write username as ubuntu as selected os and then type following commands

curl -sL https://github.com/ShubhamTatvamasi/docker-install/raw/master/docker-install.sh | bash

[this will install and run docker in your vm]

newgrp docker

[this command will help us to use docker]

docker ps

[this will list docker]

docker --version

[this will display the version of docker installed]

[now installing nginx]

docker pull nginx

--You can download Nginx from a pre-built Docker image, with a default Nginx configuration, by above command. This downloads all the necessary components for the container.

docker run --name docker-nginx -p 80:80 nginx

--Nginx installed, you can configure the container so that it’s publicly accessible as a web server.

(run is the command to create a new container)

[The --name flag is how you specify the name of the container. If left blank, a generated name like nostalgic_hopper will be assigned.]

[-p specifies the port you are exposing in the format of -p local-machine-port:internal-container-port. In this case, you are mapping port :80 in the container to port :80 on the server.]

--nginx is the name of the image on Docker Hub.

--now this will show this on your public ip

![Screenshot_2024_0923_210801](https://github.com/user-attachments/assets/12ed503f-9c71-4c80-bcb3-468c989c0258)

--In your terminal, enter CTRL+C to stop the container from running.

docker ps -a

[verify the container status with this command]

docker rm docker-nginx

[Remove the existing container]

docker run --name docker-nginx -p 80:80 -d nginx

--Create a new, detached Nginx container,By attaching the -d flag, you are running this container in the background.

docker ps

[this will obtain info about your container]

docker stop docker-nginx

[Stop the container]

docker rm docker-nginx

[remove the container]

# Building a Web Page to Serve on Nginx

mkdir -p ~/docker-nginx/html

-Create a new directory for your website content within the home directory

cd ~/docker-nginx/html

[by this you navigate into this]

vi index.html

[now press i and write your code in html like ]


![Screenshot_2024_0923_211405](https://github.com/user-attachments/assets/7cd1afd2-b42e-43c1-94ed-86a1f1ebedf9)

-then press ctrl+c then shift+colon then write wq and enter

docker run --name docker-nginx -p 80:80 -d -v ~/docker-nginx/html:/usr/share/nginx/html nginx

Linking the Container to the Local Filesystem

open your public ip in browser you will see as the content as your html code
# here you go 👏🏻

# Using Your Own Nginx Configuration File

cd ~/docker-nginx

docker cp docker-nginx:/etc/nginx/conf.d/default.conf default.conf

--Copy the Nginx config directory into your project folder

docker stop docker-nginx 

docker rm docker-nginx

--to rebuild the container stop the container then remove it

docker run --name docker-nginx -p 80:80 -v ~/docker-nginx/html:/usr/share/nginx/html -v ~/docker-nginx/default.conf:/etc/nginx/conf.d/default.conf -d nginx

--This command links the custom website pages to the container.

docker restart docker-nginx

--you need to restart your container to reflect changes on the associated pages.

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

--First open aws search EC2 ,and download your passkey then Launch Instance and select 22.04 AMI then select t2.xlarge instance type then select keypair then configure storage to 30 GB then enable all traffic in network and Launch.

--Launch PuTTY and add the IP address from instance and add key pair file and open the PuTTY terminal.

--Now connect it with putty and login into it by writing ubuntu

--Now put some commands


curl -sL https://github.com/ShubhamTatvamasi/docker-install/raw/master/docker-install.sh | bash

--it will install docker


sudo usermod -aG docker $USER

newgrp docker

--it will Add your local user to docker group so that your local user run docker commands


sudo snap install kubectl --classic

--it will intall kubernetes


kubectl version --client

--it checks the version

#Installing Minikube

curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64


sudo install minikube-linux-amd64 /usr/local/bin/minikube

minikube version

--it checks its version

#Starting Minikube with Docker Driver

minikube start --driver=docker

# If you encounter root privileges error, run:


minikube start --driver=docker --force

minikube status

--it checks its status


kubectl cluster-info

--it checks cluster info


kubectl config view

--it will show the config


kubectl get nodes

--it will display nodes in it

kubectl get pods

--it will show pods in it

kubectl create deployment nginx-web --image=nginx

kubectl expose deployment nginx-web --type NodePort --port=80

kubectl get deployment,pod,svc

--it will deploy a sample nginx deployment


minikube addons list

--It will display all addons


minikube addons enable dashboard

minikube addons enable ingress

--this enables these addons

minikube dashboard --url**

# it will get the url and run the dashboard of MiniKube


'''bash
kubectl proxy --address='0.0.0.0' --disable-filter=true &
'''


--This will enable port :8001 to access it on your public ip


http://server_ip:8001/api/v1/namespaces/kubernetes-dashboard/services/http:kubernetes-dashboard:/proxy/#/workloads?namespace=default

# in browser replace server ip with public ip

# Now go to above link and replace server_ip with your public ip and it will show you like :

![Screenshot_2024_0923_213426](https://github.com/user-attachments/assets/16ca5aa7-e6db-47d4-b005-2794b6c4289b)





```bash
yuihf
```
