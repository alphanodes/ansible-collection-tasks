# Ansible Role: system-task

Run system tasks for restart services and reboot server

[![Ansible Galaxy](https://img.shields.io/badge/galaxy-alphanodes.system--task-660198.svg)](https://galaxy.ansible.com/AlphaNodes/system-task)

## Dependencies

  none

## Installation

### Ansible 2+

Using ansible galaxy cli:

```shell
ansible-galaxy install alphanodes.system_task
```

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```yaml
system_task_name: ''
```

`system_task_name` can be set to `service_restart`, `goaccess`, `pgbadger_query`, `postgres_vacuum` or `reboot`.

```yaml
system_task_reboot_delay: 10
```

Seconds of deploy for reboot.

```yaml
system_task_reboot_timeout: 180
```

Maximum seconds to wait for machine to reboot and respond to a test command.
This timeout is evaluated separately for both network connection and test command success so the maximum execution time for the module is twice this amount.

```yaml
system_task_reboot_msg:
```

Message for reboot.

```yaml
system_task_service_name: ''
```

Name of service, which should be restarted.

```yaml
system_task_service_reload: false
```

Use reload instead of restart for service restart for `system_task_service_name`.

```yaml
system_task_supervisor_job: ''
```

Name of supervisor job, which should be restarted.

## Example Playbook for restart service

```yaml
- hosts: server-name
  vars:
    system_task_name: service_restart
    system_task_service_name: php7.2-fpm
  roles:
    - alphanodes.system_task
```

## Example Playbook for reboot

```yaml
- hosts: server-name
  vars:
    system_task_name: reboot
  roles:
    - alphanodes.system_task
```

## License

GPL Version 3

## Author Information

This role was created in 2018 by [AlphaNodes](https://alphanodes.com/).
