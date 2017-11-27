# Ansible Role: Tomcat 8

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

OS specific defaults directory.
```
# /etc/sysconfig in Centos/RHEL
# This should be a choice based on OS.
tomcat8_system_defaults_dir: /etc/defaults
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

There are additional configuration options in [defaults/main.yml](defaults/main.yml)

## Dependencies

  None
  
## Example Playbook

    - hosts: webservers
      roles:
        - { role: Islandora-Devops.tomcat8 }

## License

MIT