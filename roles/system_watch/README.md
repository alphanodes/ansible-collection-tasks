# Ansible Role: system-watch

Installs system-watch monitoring on Debian and Ubuntu servers.

## Example Playbook

```yaml
    - hosts: all

      vars:
        system_watch_repo: ssh://git@git.yourserver.com/log.git
        system_watch_git_status_repos:
          - name: project1
            path: /srv/project1
          - name: project2
            path: /srv/project2

      roles:
        - alphanodes.tasks.system_watch
```
