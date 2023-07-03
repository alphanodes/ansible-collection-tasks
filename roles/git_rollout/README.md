# Ansible Role: git-rollout

Git rollout from a definition list

## Installation

### Ansible 2+

Using ansible galaxy cli:

```shell
ansible-galaxy install alphanodes.git_rollout
```

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

## Dependencies

git has to be installed.

## Example Playbook

```yaml
- hosts: server-name
  vars:
    git_rollout_instances:
      - name: myrepo
        repo: git@github.com:myname/myrepo.git
        dir: /srv/targetdir
  roles:
    - alphanodes.git_rollout
```

## License

GPL Version 3

## Author Information

This role was created in 2022 by [AlphaNodes](https://alphanodes.com/).
