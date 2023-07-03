# Ansible Role: sphinx-rollout

Rollout sphinx repositories

## Installation

### Ansible 2+

Using ansible galaxy cli:

```shell
ansible-galaxy install alphanodes.sphinx_rollout
```

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

## Dependencies

sphinx and git has to be installed.

## Example Playbook

```yaml
- hosts: server-name
  vars:
    sphinx_instances:
      - name: docs
        repo: git@github.com:myname/myrepo.git
        dirs:
          - name: dir1
          - name: dir2
      - name: manuals
        repo: git@github.com:myname/myrepo.git
        dirs:
          - name: dir1
          - name: dir2
    sphinx_rollout_instance: docs
  roles:
    - alphanodes.sphinx_rollout
```

## License

GPL Version 3

## Author Information

This role was created in 2022 by [AlphaNodes](https://alphanodes.com/).
