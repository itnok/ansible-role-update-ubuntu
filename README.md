update-ubuntu
=============

Performs the equivalent of `apt update && apt dist-upgrade -y` on an Ubuntu host.

Steps performed are:

  - Update apt package cache
  - Get list of available updates
  - Perform upgrade of all upgradable packages to the latest version
  - Check if reboot is required
  - Reboot of the machine if needed


:exclamation: Requirements
--------------------------

None.


:abcd: Role Variables
---------------------

None.


:link: Dependencies
-------------------

None.


:notebook: Example Playbook
---------------------------

Here an example of how to use this role in your playbooks:

```
- hosts: servers
  remote_user: ubuntu   # optional (your remote user)
  gather_facts: yes     # optional
  become: yes

  roles:
    - { role: itnok.update-ubuntu }
```

:guardsman: License
-------------------

MIT _([read more](LICENSE.md))_
