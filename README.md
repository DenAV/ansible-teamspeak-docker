## ansible teamspeak docker 

## Pre-requisites

* You must have [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) installed on your computer.

## Quick start

Config the teamspeak server with Ansible:

Ansible code one that deploys everything you need to run service - docker and related.
```
sudo ansible-playbook playbooks/pl_setup_ts_docker.yml
```

## Container shell access

The `docker exec` command allows you to run commands inside a Docker container. The following command line will give you a shell inside your `teamspeak` container:

```shell
$ docker exec -it teamspeak bash
```

The TeamSpeak server log is available through Docker's container log:

```shell
$ docker logs teamspeak
```
