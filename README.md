This project involves building a setup to simulate a real-world cloud environment the kind used by companies to host websites, apps, and services. Here's the purpose behind each step:

## 1. Launch an EC2 Instance + Custom Security Group
# Purpose:
EC2 instance = the virtual server on the cloud.
Security group = acts like a firewall to control traffic into and out of the server.

## 2. Install a Web Server (Apache)
# Purpose:
This makes the EC2 instance serve web pages (like a basic website or app).
Turning the EC2 into a real, working web server that anyone on the internet can access.


## 3. Create an Auto Scaling Group with a Load Balancer
## Purpose:
The Auto Scaling Group launches more EC2 instances automatically when there's high traffic.
The Load Balancer shares traffic evenly across those instances.
This ensures your website or app is:

Scalable (can handle growth)

Reliable (stays online even if one instance fails)

Efficient (only uses resources when needed)

## Why This Project Matters
This setup taught me core skills for cloud computing and real-world IT environments

# Skill and Real-World Relevance
EC2 + Web Server for Hosting apps, websites, backend services

Security Groups for Cybersecurity, firewall config   

Load Balancer for Distributing traffic across servers   

Auto Scaling for Handling peak traffic, cost optimization
