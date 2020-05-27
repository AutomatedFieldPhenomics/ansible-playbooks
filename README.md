# Ansible Playbooks for Raspberry Pi Zero W IoT Fleet Management

## Introduction to Ansible

A [quikstart video](https://www.ansible.com/resources/videos/quick-start-video)
epxlains what Ansible is: an agent-less system configuration and automation engine
based on yaml playbooks. Ansible runs entirely over SSH.

[Installing Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)
is straightforward with, for example:
- `sudo dnf install ansible` (RHEL, CentOS, or Fedora)
- `sudo apt install ansible` (Debian. Ubuntu)
- `pip install --user ansible` (macOS)

## Running simple commands

The available hosts are in the file `inventory/hosts`. You will need to have your
public SSH key on each of the nodes listed there. You may want to use `ssh-agent`
to avoid having to enter your password.

### Testing whether hosts are online
```
ansible -i inventory/hosts all -m ping
ansible -i inventory/hosts selkirk -m ping
ansible -i inventory/hosts wolseley -m ping
```
