# Ansible NSO Collection Playbooks
This repo contains example playbooks for use with the ansible-nso collection (https://galaxy.ansible.com/cisco/nso).

## Installation
```
ansible-galaxy collection install cisco.nso
```

## Prerequisites
Enter your NSO hostname and credentials into the `creds.yml.example` file and save a copy of the file called `creds.yml` in the root of the repo. A device will be added to your NSO instance,  the device hostname must be specified in the `group_vars/all` variable file.  

## Running
```
ansible-playbook pb_all_modules.yml
```
> If running the individual modules,  the device must first be created in NSO with `ansible-playbook pb_nso_config.yml` or an existing device must be specified in `group_vars/all`. 