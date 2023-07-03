# Ansible Role: matomo-task

Run Matomo tasks for an installed matomo

- run console tasks
- run config.ini.php sync for cluster mode
- run import dump
- run geoip database update

## Dependencies

An installed redmine.

## Installation

### Ansible 2+

Using ansible galaxy cli:

```shell
ansible-galaxy install alphanodes.matomo_task
```

## Example Playbook

```yaml
    - hosts: server-name
      vars:
        matomo_domain: https://my.url-to-matomo.com
        matomo_console_name: core:archive
      roles:
        - alphanodes.matomo_task
```

## License

GPL Version 3

## Author Information

This role was created in 2019 by [AlphaNodes](https://alphanodes.com/).
