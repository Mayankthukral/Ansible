# Ansible Project
================

This repository contains an Ansible project demonstrating best practices for infrastructure automation.

## Purpose

The project showcases structured organization of Ansible roles, playbooks, and configuration files, making it easy to manage and maintain your infrastructure.

## Directory Structure

* `ansible.cfg`: Ansible configuration file, where you can set global settings and defaults.
* `inventories/`: Directory containing inventory files, which define the hosts and groups in your infrastructure.
* `group_vars/`: Directory containing group-specific variables, which can be used to customize settings for specific groups of hosts.
* `host_vars/`: Directory containing host-specific variables, which can be used to customize settings for individual hosts.
* `roles/`: Directory containing reusable Ansible roles, which are pre-defined sets of tasks and handlers that can be applied to hosts.
* `playbooks/`: Directory containing YAML playbooks for orchestration, which define the tasks and roles to be applied to hosts.

## Usage

1. Ensure Ansible is installed on your system.
2. Customize `ansible.cfg` with appropriate settings, such as the inventory file location and default roles path.
3. Define inventory files in `inventories/`, specifying the hosts and groups in your infrastructure.
4. Customize variables in `group_vars/` and `host_vars/`, which can be used to tailor your playbooks to specific environments.
5. Define tasks and handlers in `roles/`, which can be reused across multiple playbooks.
6. Create playbooks in `playbooks/` to orchestrate roles and apply them to hosts.
7. Execute playbooks using `ansible-playbook`, specifying the playbook file and any necessary options.

## Running Ansible Commands

### Running Ansible Playbooks

To run Ansible playbooks, use the `ansible-playbook` command followed by the playbook file.

### Commands


# Running the Site Playbook
# This command applies the roles defined in site.yml to all hosts specified in the inventory.
cd /path/to/your/ansible/project
ansible-playbook playbooks/site.yml

# Running the Webservers Playbook
# This command applies the webserver role to the hosts in the webservers group.
cd /path/to/your/ansible/project
ansible-playbook playbooks/webservers.yml

# Specifying an Inventory
# This command uses the production inventory file instead of the default inventory.
cd /path/to/your/ansible/project
ansible-playbook -i inventories/production/hosts playbooks/site.yml

# Running with Tags
# This command runs only the tasks tagged with "install" in the site playbook.
cd /path/to/your/ansible/project
ansible-playbook playbooks/site.yml --tags "install"

# Dry Run (Check Mode)
# This command performs a dry run of the site playbook, showing what changes would be made without actually applying them.
cd /path/to/your/ansible/project
ansible-playbook playbooks/site.yml --check

# Running with Extra Variables
# This command passes an extra variable "nginx_port=8080" to the site playbook, which can be used to customize the playbook's behavior.
cd /path/to/your/ansible/project
ansible-playbook playbooks/site.yml -e "nginx_port=8080"