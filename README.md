# [ansible-roles-sublime-text](#ansible-roles-sublime-text)

Install Sublime Text on your system.

|GitHub|GitLab|Quality|Downloads|Version|Issues|Pull Requests|
|------|------|-------|---------|-------|------|-------------|
|[![github](https://github.com/buluma/ansible-role-ansible-roles-sublime-text/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-ansible-roles-sublime-text/actions)|[![gitlab](https://gitlab.com/buluma/ansible-role-ansible-roles-sublime-text/badges/master/pipeline.svg)](https://gitlab.com/buluma/ansible-role-ansible-roles-sublime-text)|[![quality](https://img.shields.io/ansible/quality/)](https://galaxy.ansible.com/buluma/ansible-roles-sublime-text)|[![downloads](https://img.shields.io/ansible/role/d/)](https://galaxy.ansible.com/buluma/ansible-roles-sublime-text)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-ansible-roles-sublime-text.svg)](https://github.com/buluma/ansible-role-ansible-roles-sublime-text/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-ansible-roles-sublime-text.svg)](https://github.com/buluma/ansible-role-ansible-roles-sublime-text/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-ansible-roles-sublime-text.svg)](https://github.com/buluma/ansible-role-ansible-roles-sublime-text/pulls/)|

## [Example Playbook](#example-playbook)

This example is taken from `molecule/default/converge.yml` and is tested on each push, pull request and release.
```yaml
---
- name: Converge
  hosts: all
  become: yes
  gather_facts: yes
  vars:
    sublime_packages:
      - https://github.com/math2001/FileManager
      - https://github.com/titoBouzout/SideBarEnhancements

  roles:
    - role: ansible-roles-sublime-text
```

The machine needs to be prepared. In CI this is done using `molecule/default/prepare.yml`:
```yaml
---
- name: Prepare
  hosts: all
  gather_facts: no
  become: yes

  roles:
    - name: buluma.bootstrap
    - name: buluma.git
```


## [Role Variables](#role-variables)

The default values for the variables are set in `defaults/main.yml`:
```yaml
---
# defaults file for sublime-text

# Set the version for Sublime-Text
sublime_version: 4

sublime_package_control: true

sublime_packages: []
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-ansible-roles-sublime-text/blob/main/requirements.txt).


## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-ansible-roles-sublime-text/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|debian|all|
|ubuntu|focal, bionic|

The minimum version of Ansible required is 2.10, tests have been done to:

- The previous version.
- The current version.
- The development version.



If you find issues, please register them in [GitHub](https://github.com/buluma/ansible-role-ansible-roles-sublime-text/issues)

## [Changelog](#changelog)

[Role History](https://github.com/buluma/ansible-role-ansible-roles-sublime-text/blob/master/CHANGELOG.md)

## [License](#license)

Apache-2.0

## [Author Information](#author-information)

[buluma](https://buluma.github.io/)
