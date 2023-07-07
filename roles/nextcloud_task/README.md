# Ansible Role: nextcloud-task

Run console task for nextcloud on Debian / Ubuntu.

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
    - alphanodes.tasks.nextcloud_task
```

## Example Playbook for console run

```yaml
- hosts: server-name
  vars:
    nextcloud_task_name: console
    nextcloud_console_command: maintenance:mimetype:update-db

  roles:
    - alphanodes.tasks.nextcloud_task
```
