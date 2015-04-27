Maven
=====

This [Ansible](http://www.ansible.com/home) role installs and configures [Maven](https://maven.apache.org/) - the popular software project management and comprehension tool for Java projects.

## Prerequisites

* Add the role to the project's Ansible galaxy requirements file and install it via the ansible-galaxy command
* Use one of the Git tag versions if you want to stick to a certain version of this role (stable versus head)

## Supported Platforms

* CentOS 6
* CentOS 7

## How to use

* Add the following line to your Ansible's playbook role section if you want to use the Maven role with its defaults:
```
roles:
    - ansible-maven
```
* If you want to pass custom values for the available variables, add something similar to the line below:
```
roles:
    - { role: ansible-maven, maven_version: "3.3.1" }
```

## Configuration

### Variables

| Variable | Description | Default value | Mandatory |
|----------|-------------|---------------|-----------|
| maven_version | The explicit maven version to be installed | 3.3.1 | No |
| maven_mirror_url_binaries | The URL pointing to the web location where the binaries can be found | See defaults/main.yml | No |
| maven_install_dir | The default install dir | /opt/maven | No |
| maven_bin_path | The path used to create a symlink to the installed maven version | /usr/local/bin | No |
