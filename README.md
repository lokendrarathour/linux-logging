# linux-logging
enable system level logging on any linux server via ansible
directory structure
linux-loggig/
├── inventory
├── playbook.yml
└── roles/
    └── system_setup/
        ├── tasks/main.yml
        ├── templates/logrotate.j2
        └── files/
# Ansible System Bootstrap & Log Rotation Setup

This Ansible project installs basic utilities and configures an enterprise-style log rotation policy.

## Features
- Installs nginx, tree, and vim
- Creates `/var/log/archive` for rotated logs
- Rotates logs when size exceeds **30GB**
- Keeps **30 days** retention
- Daily cron job triggers logrotate

## Usage

### 1. Edit `inventory` file
Replace `YOUR_SERVER_IP` with the target server IP.

### 2. Run the playbook
```bash
ansible-playbook -i inventory playbook.yml
