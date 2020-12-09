# Ansible Role: ansible-apps_hackmd

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_hackmd.svg?branch=master)](https://travis-ci.com/lotusnoir/ansible-apps_hackmd)[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)[![Ansible Role](https://img.shields.io/badge/ansible%20role-apps__hackmd-blue)](https://galaxy.ansible.com/lotusnoir/ansible-apps_hackmd/)[![GitHub tag](https://img.shields.io/badge/version-latest-blue)](https://github.com/lotusnoir/ansible-apps_hackmd/tags)

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
