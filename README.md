### PROJECTWEBSTACK
**WEB STACK IMPLEMENTATION (LEMP STACK)**

**Deploying a LEMP Stack Application On AWS Cloud**

Deploying a LEMP stack application on the AWS Cloud is a robust and flexible way to host web applications. The LEMP stack, consisting of Linux as the operating system, Nginx as the web server, MySQL as the database system, and PHP for server-side scripting, is a popular choice for web developers. AWS offers a range of services and tools to streamline the deployment process.

Steps to Deploy:

1. Set Up AWS Account: If you don't have one, create an AWS account to access AWS services.

2. Launch an EC2 Instance: Use Amazon Elastic Compute Cloud (EC2) to launch a virtual server (EC2 instance) running a Linux-based operating system (e.g., Amazon Linux or Ubuntu).

3. Secure Your Instance: Configure security groups and key pairs to control access to your EC2 instance. SSH into the instance for further setup.

4. Update and Install LEMP Components: Update the package list and install the LEMP stack components.

**Creating an Ubuntu EC2 Instance**

Login to AWS Cloud Service console and create an Ubuntu EC2 instance. The virtual machine is a Linux operating system that is the backbone of the LEMP Stack web application.

![Projectlemp Ec2 instance](https://github.com/Ukdav/PROJECTWEBSTACK/assets/139593350/3be4774c-834c-4e05-8eda-6afbb5e2226e)

Login into the instance via ssh:

cd Downloads

*$ ssh -i lemp.pem Ubuntu@13.48.43.228*

![ssh initial connection to ec2](https://github.com/Ukdav/PROJECTWEBSTACK/assets/139593350/89c2f101-67e5-40c1-8bac-7d2f7c10b8d2)

**Installing the Nginx Web Server**

To install the Nginx web server on a Linux system, you can follow these general steps. The specific commands may vary slightly depending on your Linux distribution. Here, I'll provide instructions for two common Linux distributions: Ubuntu/Debian and CentOS/RHEL.

*$ sudo apt Update*

*$ sudo apt install nginx*

![sudo apt update](https://github.com/Ukdav/PROJECTWEBSTACK/assets/139593350/6f936da1-e23f-4810-a0bc-d923423de4aa)

![sudo apt install nginx](https://github.com/Ukdav/PROJECTWEBSTACK/assets/139593350/7a5c5c66-47bf-4145-bd07-4a8d0208feec)

check the status of Nginx to ensure it's running without errors; you will use this command

*$ sudo systemctl status nginx*

A green text color shows that the server is active

![sudo systemctl status nginx](https://github.com/Ukdav/PROJECTWEBSTACK/assets/139593350/759a09cf-c380-4d51-b887-db3333d8d176)

Accessing the default nginx web server block to see if everything works correctly. curl the local IP address of our local machine which in most case is 127.0.0.1 or the DNS name localhost on any web browser on our local machine.
curl http://127.0.0.1:80 or curl http://localhost:80

The below result shows nginx has been properly set up and we can deploy our web application.

![curl http](https://github.com/Ukdav/PROJECTWEBSTACK/assets/139593350/3e5dc227-68b0-4189-9fa4-5ff4e58add12)

Before we receive traffic from our web server, we need to open TCP port: 80 which is the default port that a web browser uses to open a website or access a webpage on the internet.

As we already know port 22 has already been opened by default on our EC2 machine to access it via SSH connection, so we need to add a rule to EC2 configuration to open an inbound connection of TCP PORT 80.

![create inound rules](https://github.com/Ukdav/PROJECTWEBSTACK/assets/139593350/8ee35398-af73-4f43-8bf8-622c35e8a6b2)

It appears our default nginx server is accessible locally on our local machine. To check if we can access the default server block over the internet on our local machine, insert the public IP address of the server on a browser.

![nginx web server](https://github.com/Ukdav/PROJECTWEBSTACK/assets/139593350/99e01fbe-58bc-47ca-b65e-94e22eff721b)

**Installing MySQL**

We have succeeded in setting up our nginx webserver and ensured its accessible over the internet. Next is to install mySQL which is a relational database management server to help store data and manage content on our web application.

Run *$ sudo apt install mysql-server*

![sudo apt install mysql server](https://github.com/Ukdav/PROJECTWEBSTACK/assets/139593350/15543f3b-7b43-4069-9157-75e1fb2e4ed3)

Provide added security to our MySQL server by running *$ sudo mysql-secure_installation*. This script will remove some insecure default settings and lock down access to our database system.

![sudo security pwd](https://github.com/Ukdav/PROJECTWEBSTACK/assets/139593350/7d317b2e-6dd6-4c41-b36f-36dae7954aeb)

On each prompt that comes press Y, add a password, and save.

With mysql_server successfully configured, login into the mysql server and To exit from the web server we enter exit

*$ sudo mysql*

This will connect to the MYSQL server as the administrative database user root, which is inferred by the use of sudo command.

![sudo mysql](https://github.com/Ukdav/PROJECTWEBSTACK/assets/139593350/9f957bb3-5e72-4d4a-bcd4-503333ceb06c)

![sudo security pwd](https://github.com/Ukdav/PROJECTWEBSTACK/assets/139593350/3f7db0bf-90f4-4e22-892b-e1986aa4908a)

























