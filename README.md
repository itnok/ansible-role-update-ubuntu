update-ubuntu
=============

[![Build Status](https://github.com/itnok/ansible-role-update-ubuntu/workflows/CI/badge.svg)](https://github.com/itnok/ansible-role-update-ubuntu/actions/workflows/main.yml) [![GitHub tag](https://img.shields.io/github/v/tag/itnok/ansible-role-update-ubuntu?sort=semver)](https://github.com/itnok/ansible-role-update-ubuntu/tags/) [![Ansible Role](https://img.shields.io/ansible/role/46971)](https://galaxy.ansible.com/itnok/update_ubuntu)


Performs the equivalent of `apt update && apt dist-upgrade -y` on an Ubuntu host.

Steps performed are:

  - Get updated facts about the current Ubuntu running state
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

- [itnok.is_ubuntu](https://galaxy.ansible.com/itnok/is_ubuntu) _(:octocat: [ansible-role-is-ubuntu](https://github.com/itnok/ansible-role-is-ubuntu))_

To install dependencies use:
```
    $ ansible-galaxy install <dependecy.name>
```

Installation of the required Ansible Roles can also be simply addressed with:
```
    $ ansible-galaxy install -r requirements.yml
```


:notebook: Example Playbook
---------------------------

Here an example of how to use this role in your playbooks:

```
---
- hosts: servers
  remote_user: ubuntu   # optional (your remote user)
  gather_facts: yes     # optional
  become: yes

  roles:
    - { role: itnok.update_ubuntu }
```

:guardsman: License
-------------------

MIT _([read more](LICENSE.md))_
