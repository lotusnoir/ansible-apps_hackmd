# Ansible Role: ansible-apps_hackmd

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_hackmd.svg?branch=master?style=flat)](https://travis-ci.com/lotusnoir/ansible-apps_hackmd)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)
[![Ansible Role](https://img.shields.io/badge/galaxy-apps_hackmd-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_hackmd)
![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_hackmd?color=orange&style=flat)
![Ansible Quality Score](https://img.shields.io/ansible/quality/52300)
[![downloads](https://img.shields.io/ansible/role/d/52300)](https://galaxy.ansible.com/lotusnoir/apps_hackmd)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_hackmd.svg)](https://github.com/lotusnoir/ansible-apps_hackmd/releases/)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_hackmd&metric=alert_status)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_hackmd)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_hackmd&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_hackmd)
[![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_hackmd&metric=reliability_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_hackmd)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_hackmd&metric=security_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_hackmd)

Deploy [hackmd](https://github.com/hackmdio/codimd) markdown web collaborative tool.

## Role variables

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `hackmd_version` | "2.2.0" | hackmd version |
| `hackmd_install_dir` | /opt/hackmd | install directory | 
| `hackmd_db_host` | localhost | postgresl host | 
| `hackmd_db_user` | hackmd | bdd username | 
| `hackmd_db_pass` | strongpass | bdd password | 
| `hackmd_db_bdd` | hackmd | bdd name | 
| `hackmd_allow_anonymous` | "false" | allow anonymous user to connect | 
| `hackmd_use_cdn` | "false" |  | 
| `hackmd_auto_version_check` | "false" | check new version | 
| `hackmd_allow_origin` | "example.net" | domain origin to allow | 
| `hackmd_pdf_export` | "true" | allow pdf export | 
| `hackmd_email` | "false" | register / connect with email | 
| `hackmd_allow_email_register` | "false" |  | 
| `hackmd_ldap_url` | ldap://example.net:389 | ldap url | 
| `hackmd_ldap_binddn` | uid=test,dc=example, dc=net | ldap bindn | 
| `hackmd_ldap_bindpass` | "" | ldap binddn password  | 
| `hackmd_ldap_search` | "" |  | 
| `hackmd_ldap_search_filter` | "(uid={{ '{{' }}username{{ '}}' }})" |  | 
| `hackmd_oauth_clientid` | hackmd |  | 
| `hackmd_oauth_secret` | "" |  | 
| `hackmd_oauth_url_auth` | "" |  | 
| `hackmd_oauth_url_token` | "" |  | 
| `hackmd_oauth_url_user` | "" |  | 
| `hackmd_oauth_url_base` | "" |  | 
| `hackmd_oauth_user_name` | name |  | 
| `hackmd_oauth_user_display` | cn |  | 
| `hackmd_oauth_user_mail` | mail |  | 

## Examples

	---
	- hosts: apps_hackmd
	  become: yes
	  become_method: sudo
	  gather_facts: yes
	  roles:
	    - role: ansible-apps_hackmd
	  environment: 
	    http_proxy: "{{ http_proxy }}"
	    https_proxy: "{{ https_proxy }}"
	    no_proxy: "{{ no_proxy }}

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.
