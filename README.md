Role Name
===========

Create a user and upload an ssh puplic key for remote authorization

Requirements
------------

No specific required Ansible 

Need a default ssh public key or a specific key needs to be called out in a variable

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------
#Define the user you would like to create
user_name: default
#Define a state present or absent
user_state: present

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

None

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

---
- hosts: all
  become: true
  tasks:
     - include_role:
         name: create_user
       vars:
         user_name: robert
         ssh_key: ~/.ssh/cloud_key.pub

License
-------

MIT

Author Information
------------------

info@myfoxit.com
