# Cloud-computing-
Concepts of cloud computing, basics, related topics details 

![Screenshot_2024_0918_123427](https://github.com/user-attachments/assets/9b54d9e2-5cb2-4a28-a145-9a5e9fb7490a)

# Cloud Computing:- 

Cloud computing is the delivery of computing services—including servers, storage, databases, networking, software, analytics, and intelligence—over the Internet ("the cloud"). This allows for faster innovation, flexible resources, and economies of scale.

![Screenshot_2024_0918_123503](https://github.com/user-attachments/assets/5301d869-b3ae-46c5-9d6c-8bc54028f445)

# Docker:- 

Docker is a software platform that allows you to build, test, and deploy applications quickly. Docker packages software into standardized units called containers that have everything the software needs to run including libraries, system tools, code, and runtime. Using Docker, you can quickly deploy and scale applications into any environment and know your code will run.

![Screenshot_2024_0918_124023](https://github.com/user-attachments/assets/03fdbbef-5f0d-4a17-8797-f8e8ca8a5f58)

# How Docker works:- 

Docker works by providing a standard way to run your code. Docker is an operating system for containers. Similar to how a virtual machine virtualizes .containers virtualize the operating system of a server. Docker is installed on each server and provides simple commands you can use to build, start, or stop containers.

![Screenshot_2024_0918_123713](https://github.com/user-attachments/assets/332ee150-9a0a-4ca4-911e-91eec2471109)

# What is the structure of a Docker image?:- 

A Docker image is composed of multiple layers stacked on top of each other. Each layer represents a specific modification to the file system (inside the container), such as adding a new file or modifying an existing one. Once a layer is created, it becomes immutable, meaning it can't be changed.16 May 2023
![Screenshot_2024_0918_124113](https://github.com/user-attachments/assets/57b191a7-c6aa-40d8-ae5b-336b9d8a8029)
# container:-

A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another. A Docker container image is a lightweight, standalone, executable package of software that includes everything needed to run an application: code, runtime, system tools, system libraries and settings.

(in other and simple words )

Containers are an abstraction at the app layer that packages code and dependencies together. Multiple containers can run on the same machine and share the OS kernel with other containers, each running as isolated processes in user space. Containers take up less space than VMs (container images are typically tens of MBs in size), can handle more applications and require fewer VMs and Operating systems

![Screenshot_2024_0918_124201](https://github.com/user-attachments/assets/6f6cd7ae-eee7-4b0b-b614-313b4e8000bd)


# using EC2 in aws:-

First open aws search EC2 then Launch Instance and there select keypair in putty then download it

after that Launch it and run putty and paste public id on HOST NAME and open that downloaded key pair for putty in SSH then Auth then Credentials and open there

after that run it and write username as ubuntu as selected os and then type following commands

sudo apt update
sudo apt install apache2
to install a web server on ip then

sudo su
for convert $ into # for getting admin role then

cd /var/www/html/
then

ls
for list of html file in it

then copy that html file name and write

rm index.html
rm means remove command

vi index.html
this will open a notepad like and write html code there like (vi is editor) -

Screenshot 2024-09-10 225017

then press ctrl+c then shift+colon then write wq and enter

now copy your public ip and paste it on browser you will see the texts written by you (by using html above)

# USING CONTAINER IN VM and adding nginx server by Docker:- 

First open aws search EC2 then Launch Instance and there select keypair in putty then download it

after that edit network setting and click on add security group rule and select TCP,UDP,ALL TRAFFIC AND SELECT EVERYWHERE SOURCE TYPE IN THEM then Launch it and run putty and paste public id on HOST NAME and open that downloaded key pair for putty in SSH then Auth then Credentials and open there

after that run it and write username as ubuntu as selected os and then type following commands

curl -sL https://github.com/ShubhamTatvamasi/docker-install/raw/master/docker-install.sh | bash
this will install and run docker in your vm

newgrp docker
this command will help us to use docker

docker ps
this will list docker

docker --version
this will display the version of docker installed

now installing nginx
docker pull nginx
You can download Nginx from a pre-built Docker image, with a default Nginx configuration, by above command. This downloads all the necessary components for the container.

docker run --name docker-nginx -p 80:80 nginx
Nginx installed, you can configure the container so that it’s publicly accessible as a web server.

run is the command to create a new container

The --name flag is how you specify the name of the container. If left blank, a generated name like nostalgic_hopper will be assigned.

-p specifies the port you are exposing in the format of -p local-machine-port:internal-container-port. In this case, you are mapping port :80 in the container to port :80 on the server.

nginx is the name of the image on Docker Hub.

now this will show this on your public ip
Screenshot 2024-09-17 185925

In your terminal, enter CTRL+C to stop the container from running.
docker ps -a
verify the container status with this command

docker rm docker-nginx
Remove the existing container

docker run --name docker-nginx -p 80:80 -d nginx
Create a new, detached Nginx container,By attaching the -d flag, you are running this container in the background.

docker ps
this will obtain info about your container

docker stop docker-nginx
Stop the container

docker rm docker-nginx
remove the container

# Building a Web Page to Serve on Nginx
mkdir -p ~/docker-nginx/html
Create a new directory for your website content within the home directory

cd ~/docker-nginx/html
by this you navigate into this

vi index.html
now press i and write your code in html like

Screenshot 2024-09-10 225017

then press ctrl+c then shift+colon then write wq and enter

docker run --name docker-nginx -p 80:80 -d -v ~/docker-nginx/html:/usr/share/nginx/html nginx
Linking the Container to the Local Filesystem

open your public ip in browser you will see as the content as your html code


