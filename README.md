# AWS Linux Server Automation with Ansible

A hands-on DevOps project demonstrating Linux server
automation on AWS EC2 using Ansible.

## Technologies
- AWS EC2
- Amazon Linux 2023
- Ansible
- Linux
- Git
- Nginx

## Architecture
- Ansible Controller
- Web Server
- Database Node (inventory only)

## Features
- SSH connectivity validation
- Automated Nginx installation
- Nginx service management
- Website deployment using Ansible
- Ansible handlers
- Reusable inventory examples

## Project Structure
- install-nginx.yml: Installs and starts Nginx
- deploy-website.yml: Deploys an HTML page
- hosts.example: Example Ansible inventory
- ansible.example.cfg: Example Ansible configuration

## Usage
1. Configure your own inventory and SSH credentials.
2. Verify connectivity:
   ansible all -m ping
3. Deploy Nginx:
   ansible-playbook install-nginx.yml
4. Deploy the website:
   ansible-playbook deploy-website.yml

## Security
Private SSH keys, real inventory files and local
configuration files are excluded from Git.

## Learning Outcomes
- Linux server administration
- Infrastructure automation
- Configuration management
- Git version control
- AWS EC2 administration
## Ansible Roles

The project uses an Nginx role to automate:

- Nginx installation
- Service startup and enablement
- Static website deployment
- Nginx restart when website content changes

## Run the Deployment

From the project root:

```bash
ansible-playbook -i hosts playbooks/site.yml
