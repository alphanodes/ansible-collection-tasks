# Ansible Role: nextcloud-task

Run console task for nextcloud on Debian / Ubuntu.

## Installation

### Ansible 2+

Using ansible galaxy cli:

```shell
ansible-galaxy install alphanodes.nextcloud-task
```

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

## Dependencies

Installed nextcloud.

## Example Playbook for cron run

```yaml
- hosts: server-name
  vars:
    nextcloud_task_name: cron
  roles:
    - alphanodes.nextcloud_task
```

## Example Playbook for console run

```yaml
- hosts: server-name
  vars:
    nextcloud_task_name: console
    nextcloud_console_command: maintenance:mimetype:update-db

  roles:
    - alphanodes.nextcloud_task
```

## License

GPL Version 3

## Author Information

This role was created in 2022 by [AlphaNodes](https://alphanodes.com/).
