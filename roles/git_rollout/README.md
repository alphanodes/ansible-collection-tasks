# Ansible Role: git-rollout

Git rollout from a definition list

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

## Dependencies

git has to be installed.

## Example Playbook

```yaml
- hosts: all

  vars:
    git_rollout_instances:
      - name: myrepo
        repo: git@github.com:myname/myrepo.git
        dir: /srv/targetdir

  roles:
    - alphanodes.tasks.git_rollout
```
