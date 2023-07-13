# Ansible Role: jekyll-rollout

Rollout jekyll repositories

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

## Dependencies

ruby, bundle and git has to be installed.

## Example Playbook

```yaml
- hosts: all

  vars:
    jekyll_instances:
      - name: prise-abenteuer-jekyll
        repo: git@github.com:myname/myrepo.git
        repo_version: main

  roles:
    - alphanodes.tasks.jekyll_rollout
```
