docker_privatebin
=================

This role deploys PrivateBin in a Docker based on official [PrivateBin docker image](https://hub.docker.com/r/privatebin/nginx-fpm-alpine).
The main repo for this role is on [Le Filament GitLab](https://sources.le-filament.com/lefilament/ansible-roles/docker_privatebin.git)

Requirements
------------

None

Role Variables
--------------

Variables from default directory :
* privatebin_url: URL on which PrivateBin will be listening

* Backups (for backups to be deployed, host needs to be in maintenance_contract group)
  * swift parameters for 2 object storage instances where backups should be pushed daily
  * privatebin_backup_pass : Passphrase for encryption of backups

Dependencies
------------

This role requires the following Ansible collection :
* community.docker

This Docker role supposes that Traefik is deployed as an inverseproxy in front of the deployed Dockers.
The following role is used by Le Filament for deploying Traefik : docker_server (https://sources.le-filament.com/lefilament/ansible-roles/docker_server)

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: docker_privatebin }
      vars:
         - { privatebin_url: "bin.example.org" }

License
-------

AGPL-3

Author Information
------------------

Le Filament (https://le-filament.com)
