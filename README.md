# Ansible Collection - varegab.challenge

Documentation for the collection.

You are asked to:

    In a git repo, create an Ansible collection (name of your choosing) that will contain two roles. The collection should contain all the requirements so it can be uploaded to ansible-galaxy or a private Automation Hub. You're not asked to upload it tho.
    role #1: `local_accounts`;
    create a role capable of: configuring multiple (potentially tens of them) local user accounts, defined inside a list of dictionaries variable. For each account created, the following fields should be configurable: shell, userid, expiry date, groups it belongs to, path for its home dir.
    Using this logic, the following two accounts should be created:
        name: local_adm
            shell: /bin/bash
            userid: 38000087
            expiry_date: this account should not expire
            home: /home/local_adm
            groups: this user should only belong to its primary group
        name: local_log
            shell: /bin/sh
            userid: 38000088
            expiry_date: this account should expire end of 2022
            home: /home/local_log
            groups: this user should only belong to its primary group

    Additionally, this role must also allow configuring ssh access (passwordless, via public key) for the local users created above. Propose your own solution for achieving this and implement it.

    role #2: `ssh_config`;
    create a role that ensure the ssh daemon has this 3 options configured with the following values:
        PasswordAuthentication: yes
        PermitEmptyPasswords: no
        PermitRootLogin: no
    Make any modifications required to ensure both roles are idempotent.
    Bonus task: Make any modifications required to add dry-run (checkmode) support to both roles.

Notes:

    While developing, bear in mind the collection could be used by different customers, where each customer defines the variables in its own inventory.
    Use an Ansible version that supports collections (eg ansible-core 2.12), and for the modules used please use the FQCN. Also add all collections you used to complete the exercise to a `requirements.yml` file inside a folder named `collections` inside your git repo.
    You may test your roles in a test host, any small VM running RHEL or ubuntu should work as target.
    Make sure you don't upload any sensible information to git.