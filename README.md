# Ansible role to deploy PrivateBin server docker

[![](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl "License: AGPL-3")

This role allows you to deploy PrivateBin docker based on official [PrivateBin docker image](https://hub.docker.com/r/privatebin/nginx-fpm-alpine).

Prior to running this role, you would need to have docker installed on your server and a traefik proxy (which is the purpose of [this role](https://github.com/lefilament/ansible_role_docker_server))

In order to use this role, you would need to define the following variables for your server (in hostvars for instance) - Only the names of the variables are provided below (not the values) for these used by this role to properly configure everything, you may copy this file directly in hostvars and set the variable although we could only encourage you to use an Ansible vault and refer vault variables from there:

```json
## Ansible configuration for connecting to remote host
# IP address of server
ansible_ssh_host: 
# User to be used on server (to which Ansible server public key has been provided)
ansible_ssh_user: 
# Encryped password (for elevating rights / sudo)
ansible_ssh_sudo_pass: 
# Server SSHD port
ansible_ssh_port: 


## Privatebin configuration
# Privatebin URL
privatebin_url:

```

# Credits

## Contributors

* Remi Cazenave <remi-filament>


## Maintainer

[![](https://le-filament.com/img/logo-lefilament.png)](https://le-filament.com "Le Filament")

This role is maintained by Le Filament
