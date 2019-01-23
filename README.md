[![Build Status](https://travis-ci.com/calvinbui/ansible-haproxy.svg?branch=master)](https://travis-ci.com/calvinbui/ansible-haproxy)

# Ansible HAProxy in Docker

Run HAProxy in a Docker container. This role's purpose is for simple proxying.

##  Requirements

N/A

## Role Variables

`haproxy_docker_image_tag`: Tag found at https://hub.docker.com/_/haproxy/
`haproxy_docker_folder`: Folder to put the configuration file
`haproxy_docker_config`: Configuration options for backend and frontend. Only 80 and 443 frontend ports supported.

## Dependencies

- Docker

## Example Playbook

```yaml
- hosts: servers
  become: true
  roles:
    - role: calvinbui.ansible_docker
    - role: calvinbui.ansible_haproxy_docker
```

## License

GPLv3

## Author Information

http://calvin.me
