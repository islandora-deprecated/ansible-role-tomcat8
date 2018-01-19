# Ansible Role: Tomcat 8 [![Build Status](https://travis-ci.org/Islandora-Devops/ansible-role-tomcat8.svg?branch=master)](https://travis-ci.org/Islandora-Devops/ansible-role-tomcat8)

An Ansible role that installs Tomcat 8 on:

* Centos/RHEL 7.x
* Ubuntu Xenial

## Role Variables

Available variables are listed below, along with default values:

Tomcat packages to install
```
tomcat8_packages:
  - tomcat8
```

Tomcat admin packages to install
```
tomcat8_admin_packages:
  - tomcat8-admin
```

Directory to install Tomcat into
```
tomcat8_home: /var/lib/tomcat8
```

Whether to install the Tomcat administrative interface
```
tomcat8_admin_install: yes
```

Tomcat roles
```
tomcat8_roles: []
```

Tomcat users
```
tomcat8_users: []
```

User and group to run Tomcat as
```
tomcat8_server_user: tomcat8
tomcat8_server_group: tomcat8
```

Some OS-specific variables are set in vars/* but can be overridden
```
tomcat8_home: /opt/tomcat
```

Including these only used by CentOS/RH
```
tomcat8_version: 8.5.27
tomcat_binary_url:  "http://www-eu.apache.org/dist/tomcat/tomcat-8/v{{ tomcat8_version }}/bin/apache-tomcat-{{ tomcat8_version }}.tar.gz"
tomcat_target_dir:  "/opt/apache-tomcat-{{ tomcat8_version }}"
```

## Dependencies

  None

## Example Playbook

    - hosts: webservers
      roles:
        - { role: islandora.tomcat8 }

## License

MIT
