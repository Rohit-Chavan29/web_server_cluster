# Web Server Cluster Deployment with Ansible
This repository automates the deployment of a scalable web server cluster using Ansible. It sets up HAProxy as a load balancer and NGINX as web servers on multiple nodes. This configuration is designed to handle high web traffic efficiently, ensuring load distribution and high availability.

Features:

Automated deployment using Ansible.

HAProxy load balancer for distributing traffic.

NGINX web servers to serve static content.

Scalable and easy-to-manage infrastructure

Requirements

Ansible installed on your control machine.

Install it using:

`sudo apt update`
 
`sudo apt install ansible -y`

Target Machines:

Create 1 AWS EC2 instance which will act as HAProxy server (for load balancing).

Create 2 or more AWS EC2 instances which will act as NGINX servers (for serving web content).

Access to Servers:

SSH access to all target servers.

Public/private key setup for passwordless SSH.

Setup Instructions

Clone the Repository:

`git clone https://github.com/Rohit-Chavan29/web_server_cluster.git`
 
`cd web-server-cluster`

Update the Inventory File:

Edit inventory.ini with the IP addresses of your HAProxy and NGINX servers:

Run the Playbook:

Execute the playbook to deploy the load balancer and web servers:

`ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook -i inventory.ini playbook.yml`

Access Your Setup:

Open your AWS account and navigate to the HAProxy server's IP to see the load-balanced NGINX servers in action.
