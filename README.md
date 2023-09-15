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

![sudo systemctl status nginx](https://github.com/Ukdav/PROJECTWEBSTACK/assets/139593350/759a09cf-c380-4d51-b887-db3333d8d176)










