# Ansible Role: matomo-task

Run Matomo tasks for an installed matomo

- run console tasks
- run config.ini.php sync for cluster mode
- run import dump
- run geoip database update

## Dependencies

An installed redmine.

## Example Playbook

```yaml
    - hosts: server-name
      vars:
        matomo_domain: https://my.url-to-matomo.com
        matomo_console_name: core:archive
      roles:
        - alphanodes.tasks.matomo_task
```
