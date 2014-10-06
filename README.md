# Node.js role for Ansible

Installs the latest version of Node.js from the chris-lea PPA.

## Requirements

Tested on Ubuntu 12.04 Server.

## Role Variables

The default variables are as follows:

    nodejs_global_packages: []
    nodejs_user: '{{ ansible_ssh_user }}'

## Example Playbook

    - hosts: 'servers'
      roles:
        - role: 'ssilab.nodejs'
          nodejs_user: 'hercules'
          nodejs_global_packages:
          	- 'forever'
          	- 'gulp'
          	- 'nodemon'
          nodejs_app_home: '/path/to/my/app'    # If defined, 'npm install' will be run here

# License

This playbook is provided 'as-is' under the conditions of the BSD license. No fitness for purpose is guaranteed or implied.