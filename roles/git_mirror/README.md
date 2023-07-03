# Ansible Role: git-mirror

Mirror git repositories

## Installation

### Ansible 2+

Using ansible galaxy cli:

```shell
ansible-galaxy install alphanodes.git_mirror
```

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

## Dependencies

none

## Example Playbook

```yaml
- hosts: server-name
  vars:
    git_mirrors:
      # run git mirror (bare repo clone)
      - name: redmine
        repo: https://github.com/redmine/redmine.git
      # run git mirror and push it remote server
      - name: zabbix
        repo: https://git.zabbix.com/scm/zbx/zabbix.git
        push_to: git@github.com/yourname/your-repo.git
  roles:
    - alphanodes.git_mirror
```

## License

GPL Version 3

## Author Information

This role was created in 2022 by [AlphaNodes](https://alphanodes.com/).
