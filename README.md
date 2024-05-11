# Ansible Automation Project

Welcome to my Ansible automation project! This project demonstrates how Ansible can be used to automate server configuration and management tasks. 

## Project Overview

The main goal of this project is to automate tasks and configure multiple servers using Ansible playbooks. Here's a brief overview:

- **EC2 Servers:**
  - 1 master server
  - 3 other servers named `server-1`, `server-2`, and `server-3`

- **Task Automation:**
  - Configuration of Ansible hosts file
  - Creation of Ansible playbooks to automate various tasks

## Server Configuration

### Master Server

The master server is used for managing other servers. It's configured with Ansible to manage other servers.

- **Variables:**
  - SSH key login
  - Username
  - IP addresses of other servers

### Managed Servers

The managed servers (`server-1`, `server-2`, `server-3`) are configured to be managed by Ansible.

- **Variables:**
  - SSH key login
  - Username
  - IP addresses

## Playbooks

Here are the playbooks created for this project:

1. **date_play.yml:**
   - Displays date and uptime of all managed servers.

2. **nginx_install_play.yml:**
   - Installs, starts, and enables Nginx on `server-1` and `server-2`.

3. **deploy_static_page_play.yml:**
   - Installs, starts, and enables Nginx, and deploys a simple HTML page on `server-3`.

## Execution

To execute the playbooks, follow these steps:

1. Make sure you have Ansible installed.
2. Clone this repository to your local machine.
3. Update the `hosts` file with the IP addresses of your servers.
4. Run the playbooks using the following commands:

   ```bash
   ansible-playbook -i hosts date_play.yml
   ansible-playbook -i hosts nginx_install_play.yml
   ansible-playbook -i hosts deploy_static_page_play.yml

## Note

All servers are using the same private key for SSH authentication.
