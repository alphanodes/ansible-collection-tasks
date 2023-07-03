# Ansible Role: jekyll-rollout

Rollout jekyll repositories

## Installation

### Ansible 2+

Using ansible galaxy cli:

```shell
ansible-galaxy install alphanodes.jekyll_rollout
```

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

## Dependencies

ruby, bundle and git has to be installed.

## Example Playbook

```yaml
- hosts: server-name
  vars:
    jekyll_instances:
      - name: prise-abenteuer-jekyll
        repo: git@github.com:myname/myrepo.git
        repo_version: main
  roles:
    - alphanodes.jekyll_rollout
```

## License

GPL Version 3

## Author Information

This role was created in 2022 by [AlphaNodes](https://alphanodes.com/).
