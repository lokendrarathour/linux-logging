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
