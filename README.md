# Linux Server Configuration & Automation using Ansible

##  Project Overview

This project demonstrates Linux server configuration, administration, and automation using Ansible.

The project uses one Ansible Control Node to manage multiple RHEL servers and automate common system administration tasks such as web server deployment, firewall configuration, user creation, backups, monitoring, and service health checks.

##  Architecture

Ansible Control Node
        |
        | SSH
        |
   ┌────┴────┐
   ↓         ↓
Server 2   Server 3
RHEL 10    RHEL 9

## Technologies Used

- Red Hat Enterprise Linux
- Ansible
- Ansible Roles
- Ansible Vault
- SSH
- Apache HTTP Server
- Firewalld
- Cron
- Git & GitHub
- Linux Shell

## ⚙️ Automation Features

### 1. User Management
- Automated Linux user creation using Ansible.

### 2. Web Server Configuration
- Install Apache HTTP Server
- Start and enable Apache
- Deploy custom website
- Configure firewall for HTTP traffic

### 3. Ansible Roles
- Created a reusable `webserver` role.
- Used tasks and handlers for Apache configuration.

### 4. Ansible Vault
- Used Ansible Vault to protect sensitive variables.
- Prevented `secrets.yml` from being committed using `.gitignore`.

### 5. Automated Backup
- Created automated `/etc` backups.
- Created backup scripts using Ansible.
- Scheduled daily backups using Cron.

### 6. Server Monitoring
- Monitor disk usage
- Monitor memory usage
- Check CPU load
- Check Apache service status

### 7. Service Health Check
- Automatically verifies whether Apache is running.
- Playbook reports failure if Apache is not active.

##  Project Structure

```text
linux-server-automation-ansible/
│
├── inventory
├── site.yml
├── create-user.yml
├── webserver.yml
├── website.yml
├── secure-webserver.yml
├── multi-webserver.yml
├── variable-website.yml
├── backup.yml
├── backup-cron.yml
├── monitoring.yml
├── service-check.yml
├── vault-test.yml
├── vars.yml
├── .gitignore
│
└── roles/
    └── webserver/
        ├── tasks/
        │   └── main.yml
        └── handlers/
            └── main.yml
