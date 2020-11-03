# Dockerfile Centos7 Ansible

[![Docker Automated build](https://img.shields.io/docker/automated/libertxyz/docker-ansible-centos7.svg?maxAge=2592000)](https://hub.docker.com/r/libertxyz/docker-ansible-centos7)



[![Build Status](https://travis-ci.com/libert-xyz/docker-ansible-centos7.svg?branch=master)](https://travis-ci.com/libert-xyz/docker-ansible-centos7)

## How to Use

## Local

  1. Pull this image from Docker Hub:

  `docker pull libertxyz/docker-ansible-centos7:latest`

  2. Run a container from the image:

  `docker run -d --privileged --volume=/sys/fs/cgroup:/sys/fs/cgroup:ro --volume=`pwd`:/etc/ansible/roles/role_under_test:ro libertxyz/docker-ansible-centos7`

## Molecule Testing

You can add the Docker image as part of Molecule

```yaml
platforms:
  - name: instance
    image: libertxyz/docker-ansible-centos7:latest
    command: /sbin/init
    tmpfs:
      - /run
      - /tmp
    volumes:
      - /sys/fs/cgroup:/sys/fs/cgroup:ro
```

## Notes

This container is only intented to use to test Ansible Roles and Playbooks not intended for production use.

## Author
