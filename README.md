# ansible-apps_hackmd

## Description

[![Galaxy Role](https://img.shields.io/badge/galaxy-apps_hackmd-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_hackmd)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_hackmd.svg)](https://github.com/lotusnoir/ansible-apps_hackmd/releases/latest)
[![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_hackmd?color=orange&style=flat)](https://galaxy.ansible.com/lotusnoir/apps_hackmd)
[![downloads](https://img.shields.io/ansible/role/d/56093)](https://galaxy.ansible.com/lotusnoir/apps_hackmd)
[![Ansible Quality Score](https://img.shields.io/ansible/quality/56093)](https://galaxy.ansible.com/lotusnoir/apps_hackmd)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)

Deploy [hackmd](https://github.com/hackmdio/codimd) markdown web collaborative tool.

## Requirements

You need to install nodejs - geerlingguy.nodejs

## Role variables

See [variables](/defaults/main.yml) for more details.

## Examples

        ---
        - hosts: apps_hackmd
          become: true
          become_method: sudo
          gather_facts: true
          roles:
            - role: ansible-apps_hackmd


## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.

