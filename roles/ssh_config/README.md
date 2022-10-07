Role Name
=========
sshd_config

Requirements
------------

No requirements

Role Variables
--------------

settings
(the list of keys we want to search for and their values)

path
(the path of the file where we want to perfom the search and replace)

Dependencies
------------

No dependencies

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

- hosts: server
  roles:
    - role: ssh_config
      settings:
        PasswordAuthentication: "yes"
        PermitEmptyPasswords: "no"
        PermitRootLogin: "no"
      path: /etc/ssh/sshd_config

License
-------

BSD

Author Information
------------------

Rego Varga
