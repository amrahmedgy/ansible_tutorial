# Ansible Tutorial Project

Welcome to the **Ansible Tutorial Project**! 🚀 This project is designed to help you learn and practice Ansible automation by managing multiple server configurations.

## 📌 Project Overview
This repository contains Ansible playbooks to automate server setup, package installation, and configuration management across different Linux distributions (Ubuntu & CentOS). Whether you're a beginner or an experienced DevOps engineer, this tutorial will help you grasp key Ansible concepts through hands-on examples.

## 📂 Repository Structure

```
ansible_tutorial/
│── inventory             # Inventory file with server groups
│── ansible.cfg           # Ansible configuration file
│── playbook_install.yml  # Playbook for installing Apache & PHP
│── playbook_remove.yml   # Playbook for removing Apache & PHP
│── playbook_setup.yml    # Playbook for system updates & software installation
│── default_site.html     # Sample HTML file for web servers
└── README.md             # Project documentation
```

## 🛠️ Prerequisites
Before running the playbooks, ensure you have the following:

- Ansible installed on your control machine (`pip install ansible`)
- SSH access to managed nodes with key-based authentication
- Basic understanding of Ansible playbooks and inventory files

## ⚙️ Configuration
Edit the `inventory` file to define your managed servers:
```ini
[web_servers]
192.168.110.130

[db_servers]
192.168.110.131

[file_servers]
192.168.110.132

[workstations]
192.168.110.129
```

Ensure your `ansible.cfg` file points to the correct inventory:
```ini
[defaults]
inventory = inventory
private_key_file = ~/.ssh/ansible
```

## 🚀 Playbooks

### 1️⃣ Install Apache & PHP
This playbook installs Apache and PHP on Ubuntu and CentOS servers.
```sh
ansible-playbook playbook_install.yml
```

### 2️⃣ Remove Apache & PHP
This playbook removes Apache and PHP from Ubuntu servers.
```sh
ansible-playbook playbook_remove.yml
```

### 3️⃣ System Setup & Software Installation
This playbook updates all servers and installs essential software like Terraform.
```sh
ansible-playbook playbook_setup.yml
```

## 🏗️ Future Enhancements
- Add support for Nginx configuration
- Implement Ansible roles for better modularity
- Include database configuration automation
- Enhance security with user and firewall management

## 📜 License
This project is open-source and available under the MIT License.

## 🤝 Contributing
Contributions are welcome! Feel free to open an issue or submit a pull request.

---
🔥 **Let's automate with Ansible!** 🔥

