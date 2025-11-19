# Ansible_example

## First, copy the application:

```bash
git clone git@github.com:gooodh/Ansible_example.git
```
## Install dependencies:
```bash
uv sync
```

## Specify the host and user in inventory/hosts.yml

``` yml
all:
  vars:
    ansible_ssh_private_key_file: /home/nikulin/.ssh/id_rsa
  hosts:
    vm:
      ansible_host: 192.168.56.101
      ansible_user: vboxuser
```

## Start playbook command:

```bash
ansible-playbook playbooks/start_settings.yml -i inventory/hosts.yml -k -K
ansible-playbook playbooks/start_settings.yml -i inventory/hosts.yml -k -K -vvv
```
