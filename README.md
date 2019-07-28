[![Build Status](https://travis-ci.com/calvinbui/ansible-haproxy-docker.svg?branch=master)](https://travis-ci.com/calvinbui/ansible-haproxy-docker)
![GitHub release](https://img.shields.io/github/release/calvinbui/ansible-haproxy-docker.svg)
![Ansible Quality Score](https://img.shields.io/ansible/quality/42347.svg)
![Ansible Role](https://img.shields.io/ansible/role/d/42347.svg)

# Ansible HAProxy

HAProxy in Docker

##  Requirements

N/A

## Role Variables

`haproxy_name`: Name of container

`haproxy_image`: Docker image to use

`haproxy_ports`: List of ports to expose

`haproxy_config_directory`: Directory to HAProxy config

`haproxy_config_template`: Config template to use. Can be replaced with one in your playbook. The template packaged with this role is meant to be very generic and serve a variety of use cases. However, many people would like to have a much more customized version, and so you can override this role's default template with your own, adding any additional customizations you need. To do this:

- Create a templates directory at the same level as your playbook.
- Create a `templates\myhaproxy.cfg.j2` file (just choose a different name from the default template).
- Set the variable like: `haproxy_config_template: myhaproxy.cfg.j2` (with the name of your custom template).

`haproxy_docker_additional_options`: [Additional parameters](https://docs.ansible.com/ansible/latest/modules/docker_container_module.html) to add to docker container

## Dependencies

N/A

## Example Playbook

```yaml
- hosts: servers
  become: true
  roles:
   - role: calvinbui.ansible_haproxy_docker
```

## License

GPLv3

## Author Information

http://calvin.me
