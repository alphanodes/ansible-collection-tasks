# Ansible Role: git-mirror

Mirror git repositories

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

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
    - alphanodes.tasks.git_mirror
```
