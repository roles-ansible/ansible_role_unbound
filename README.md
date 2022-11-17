[![Ansible Galaxy](https://raw.githubusercontent.com/roles-ansible/ansible_role_unbound/main/.github/galaxy.svg?sanitize=true)](https://galaxy.ansible.com/do1jlr/unbound) [![MIT License](https://raw.githubusercontent.com/roles-ansible/ansible_role_unbound/main/.github/license.svg?sanitize=true)](https://github.com/roles-ansible/ansible_role_unbound/blob/main/LICENSE)

 Unbound DNS Resolver
======================

Ansible role to install and configure the `unbound` dns resolver.

Variables
---------

| variable | default | explaination |
| -------- | ------- | ------------ |
| ``unbound_listen_addresses`` | ``['127.0.0.1@53','::1@53']`` | define interfaces and ports where unbound should listen |
| ``unbound_access_control``  | ``['access-control: 127.0.0.1 allow', 'access-control: ::1 allow']`` | define access control |
| ``unbound__state`` | ``present`` | Package state. *(use ``latest`` for explicit update)*
| ``submodules_versioncheck`` | ``false`` | run basic versions check. ``true`` is recomended. |

For more options have a look into the defaults/main.yml file.

 Files
-------

* `unbound.conf`:
  Main unbound configuration file.


 References
------------

* [Unbound Configuration](https://nlnetlabs.nl/documentation/unbound/unbound.conf/)

## Testing
This role is tested with some linting tests. Sadly I don't know how to run this role in a docker container because systemd is involved... If you have ideas how to improve testing please dend me a message, open a issue or Pull Request.
If you want to find out more about our tests, please have a look at the github marketplace.

| test status | Github Marketplace |
| :---------  | :----------------  |
| [![Galaxy release](https://github.com/roles-ansible/ansible_role_unbound/actions/workflows/galaxy.yml/badge.svg)](https://github.com/roles-ansible/ansible_role_unbound/actions/workflows/galaxy.yml) | [publish-ansible-role-to-galaxy](https://github.com/marketplace/actions/publish-ansible-role-to-galaxy) |
| [![Yamllint GitHub Actions](https://github.com/roles-ansible/ansible_role_unbound/actions/workflows/yamllint.yaml/badge.svg)](https://github.com/roles-ansible/ansible_role_unbound/actions/workflows/yamllint.yaml) | [yamllint-github-action](https://github.com/marketplace/actions/yamllint-github-action) |
| [![Ansible Lint check](https://github.com/roles-ansible/ansible_role_unbound/actions/workflows/ansible-linting-check.yml/badge.svg)](https://github.com/roles-ansible/ansible_role_unbound/actions/workflows/ansible-linting-check.yml) | [ansible-lint action](https://github.com/marketplace/actions/ansible-lint)

