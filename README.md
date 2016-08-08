# Ansible Rancher Agent

Ansible role to register your machine to a Rancher server

> Note: This only works for `v1` of Rancher API

# Setup

Add it to your `requirements.yml` file and install it, like:

```
- name: rancher-agent
  src: https://github.com/moltin/ansible-rancher-agent
```

+

```
ansible-galaxy install -f -r requirements.yml
```

And then use it on your `playbook`, like:

```
vars:
  cattle_access_key: your_cattle_access_key
  cattle_secret_key: your_cattle_secret_key
  cattle_host_labels: your_cattle_host_labels
  rancher_fqdn: my.rancher.fqdn.com
  rancher_environment_name: your_rancher_environment_name
roles:
  - rancher-agent
```
