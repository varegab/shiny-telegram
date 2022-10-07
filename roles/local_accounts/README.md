Role Name
=========

Create remote accounts and copy their public keys.

Requirements
------------

No requirements

Role Variables
--------------

accounts 
# a list of dictionaries which contains the user parameters.

Dependencies
------------

No dependencies

Example Playbook
----------------

- hosts: server
  roles:
    - role: local_accounts
      accounts:
        - name: 'user'
          shell: '/bin/bash'
          uid: 38000090
          expires: -1 # supported on GNU/Linux and FreeBSD
          home: '/home/user'

License
-------

BSD

Author Information
------------------

Rego Varga
