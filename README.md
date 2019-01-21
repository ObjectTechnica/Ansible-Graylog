Graylog-Server
=========

A very efficient approach to deploying a single instance of Graylog-Server 2.3  Single instances are great for proof of concepts and small-business environments. Use case could be POC or for small environments.   

Requirements
------------

Ansible 2.3
Updated inventory file
Updated defaults.yml with the following:

You MUST set a secret to secure/pepper the stored user passwords here. Use at least 64 characters.
Generate one by using for example: pwgen -N 1 -s 96

You MUST specify a hash password for the root user (which you only need to initially set up the system and in case you lose connectivity to your authentication backend)
Generate one by using for example: echo -n yourpassword | shasum -a 256

There is also a generic configuration for https:// - please change this.

Role Variables
--------------

Please review the defaults/main.yml for vars getting passed in.

Dependencies
------------

None

Example Playbook
----------------

The structure of this playbook is such that it could be combined with other playbooks.  I also based this playbook off deploying in AWS, so this playbook was geared towards that.  The Graylog-Server.yml file is set to centos user and inventory works with a pem key if needed.
Feel free to change what you like.

# Example Run

ansible-playbook -i inventory/hosts.yml Graylog-Server.yml


Pending
----------------

More performance tuning.

License
-------

MIT

Author Information
==================

Adam A. Valenzuela - Brevity is the Soul of Wit.
# Ansible
